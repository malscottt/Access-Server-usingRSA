# Access Server using RSA 

## Concepts
As we know, RSA is a type of asymmetric encryption that involves `private key` and `public key`. We will put a `public key` in our server and `private key` for us to share with others.

So, when we want to access the server by using remote connection, we will use a `private key` and if it is matched with server's `public key`, we will gain access to the server.

## Step by Step Implementation

### Step 1 : Change custom SSH port number

By default, the SSH port number is `port 22` but we want to change that port to anything we want. In this case, I want to make `port 8888` as my SSH port. So, we must configure `sshd_config` file to customize it.

```sh
vim /etc/ssh/sshd_config
```

![image](https://github.com/user-attachments/assets/63d3159f-b452-4fef-ac29-794dec712e0f)

In line 21, uncomment the `Port 22` line and change it into `Port 8888`.

![image](https://github.com/user-attachments/assets/59a1da0b-6b17-42b8-b1ee-865957d10662)

In line 40, uncomment the `PermitRootLogin` line and set is as `yes`.

![image](https://github.com/user-attachments/assets/0d387dad-6171-4a3a-ab40-f76947efcff5)

Scroll down until line 65. Uncomment the `PasswordAuthentication` line and set is as `yes`.

> [!NOTE]
> Don't forget to save the configuration file and exit by clicking `Esc` button and using `:wq!` command.


Restart the sshd service after configuring the file.

**`service sshd restart`** or **`systemctl restart sshd`** <br><br><br>


### Step 2 : Disable SELinux

This part is crucial. As we know, `SELinux` is a security layer for Linux that enforces strict access controls to protect the system by restricting what users, processes, and applications can do based on predefined security policies.

But, why must we disabled it?

Disabling `SELinux` may be necessary for RSA authentication between the server and PuTTY because `SELinux` can block access to required files, ports, or services needed for SSH key-based authentication. Temporarily disabling SELinux helps ensure the connection works, but it's recommended to adjust `SELinux` policies rather than leaving it disabled for security reasons.


-  **`sestatus`**

![image](https://github.com/user-attachments/assets/914f65af-65df-4c45-92c3-821c77c3b786)

Check the `SELinux` status. As we can see, `SELinux` status is enabled. So, we must disabled it by configuring the `/etc/selinux/config` file.

-  **`vim /etc/selinux/config`**

![image](https://github.com/user-attachments/assets/2a8fde23-f320-4f17-8e90-8933e106b159)

In line 22, set the `SELINUX` to **disabled**.

> [!NOTE]
> Don't forget to save the configuration file and exit by clicking `Esc` button and using `:wq!` command.

Next, switch the `SELinux` into permissive mode by using this command.

-  **`setenforce 0`**

> [!NOTE]
> Don't forget to reboot the server after disable the `SELinux`. 

We will go to the next step. <br><br><br>

### Step 3: Add the custom port to the firewall

Add our custom SSH port into the firewall. In this case, we will put `port 8888` to the firewall.

-  **`firewall-cmd –permanent –add-port=8888/tcp`**

After that, reload the firewall.

-  **`firewall-cmd –-reload`**

List the firewall to double check if our custom port is added to the firewall.

-  **`firewall-cmd –list-all`**

![image](https://github.com/user-attachments/assets/2bbb50b7-9eb4-4b5f-8271-588c4d2af705)

As we can see, `port 8888` is added to the firewall. <br><br><br>

### Step 4: Add users to sudoers list

In this step, we want to add user in the `sudoers` list so that the user can login direct as root without putting any sudo password.

-  **`vim /etc/sudoers`**

![image](https://github.com/user-attachments/assets/3eb833f4-fd0a-4604-bbbe-99e88330b1ac)

In line 121, add the user into the sudoers list as shown below. In this case, my username is `rocky`. 

-  *`rocky		ALL=(ALL)		NOPASSWD: ALL`*

Make a new line and put this line below `includedir`.

> [!NOTE]
> Don't forget to save the configuration file and exit by clicking `Esc` button and using `:wq!` command.

Let's go to the very **CRUCIAL** steps. <br><br><br>

### Step 5: Disable root and password login

For this step, we want to login into our server by skipping the username and password login. We are only using `private key` and `public key` pair to login into our server.

Configure the `sshd_config` file again to disable the root login and password login.

-  **`vim /etc/ssh/sshd_config`**

![image](https://github.com/user-attachments/assets/5264fb64-4273-488b-90c4-cec98cc448b5)

At `PermitRootLogin` line, set as `no`.

![image](https://github.com/user-attachments/assets/c76ff987-eb2d-42b9-8510-6f1f79e4379e)

At `PasswordAuthentication` line, set as `no`. Save the configuration file and exit. Restart the service.

Try to log out the `PuTTY` session and make a new session. But **DO NOT TERMINATE THE SESSION!** 

![image](https://github.com/user-attachments/assets/1b4874bf-200a-4002-8b99-0701701b75c4)

We will notice that we cannot login as root and password is disable. The next steps will show how to login our server using `PuTTY` by using `private key` and `public pair` key. <br><br><br>

### Step 6: Generate private key and public key pair

In `/root/.ssh` directory, generate `private key` and `public key` pair by using this command.

-  **`ssh-keygen`**

There will be a passphrase after enter this command. Just click `Enter` to skip the passphrase.

![image](https://github.com/user-attachments/assets/ec0682e6-22e6-4355-a4b8-fce786f66ae2)

As we can see, `private key` and `public key` pair will be generated.

Open the private key file which is `id_rsa`.

-  **`cat id_rsa`**

![image](https://github.com/user-attachments/assets/1822565a-7305-4c67-8f0f-779d2f3f5740)

Copy the `private key` and paste it in the notepad.

Open the public key file which is `id_rsa.pub`.

![image](https://github.com/user-attachments/assets/2f9053ce-ec51-4bc7-b2d1-24307e84e14b)

Just copy it and paste it in the notepad because we want to paste this public key into another directory.

In `/home/your-username/` directory, make a new directory and name it as `.ssh`.

-  **`mkdir .ssh`**

Make a new file in `/.ssh` and name it as `authorized_keys`.

-  **`touch authorized_keys`**

> [!NOTE]
> Make sure to name a file based on the above without any mispelling. Or else, it didn't work.

Open the `authorized_keys` file and paste the `public key` into the file.

-  **`vim authorized_keys`**

Now, our server has a `public key` so that we can login into our server by using the `private key`. <br><br><br>

### Step 7: Set up the private key by using PuTTYgen

Save the `private key` that we pasted in the **Notepad** earlier in any directory in **Windows**. I prefer just save it in **Desktop** and save it as `.txt` file.


Open `PuTTYgen` and click `Load`.

![image](https://github.com/user-attachments/assets/38d0b615-fc7a-4c89-865c-e6873a898bb3)

Choose the `file.txt` we save earlier and proceed.


`PuTTYgen` will sync with our **public** and **private key**. Click `Save private key` option to proceed to the next step.

![image](https://github.com/user-attachments/assets/af9b147a-d9f3-49c8-8540-fc56ef533909)

This icon will be showed up after we save the `private key`.

![image](https://github.com/user-attachments/assets/082da8cb-e611-415e-94b4-e615fcec9faf) <br><br><br>

### Step 8: Log in into the server by using the private key

In `PuTTY`, put the `IP address` of our server and put the port same as our custom port. In this case, I put `port 8888`.

![image](https://github.com/user-attachments/assets/acb1df7a-ab98-43cc-9dce-b589efb040ae)

Click `SSH > Auth > Credentials`. Browse our `private key` to login server by using `private key`.

![image](https://github.com/user-attachments/assets/4d30140c-f317-46f7-a9e5-4dfcd58d7094)

And, **VOILA!** **BOOM!** **ADIOS!** We can login to our server without password and by using `private key` only.

![image](https://github.com/user-attachments/assets/98ee4bae-a361-4b8e-aa37-551e082456f4)
