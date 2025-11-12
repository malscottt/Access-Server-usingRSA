# Flag Command (very easy)

<figure><img src="../../../.gitbook/assets/Screenshot 2025-11-10 222106.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Screenshot 2025-11-10 222254.png" alt=""><figcaption></figcaption></figure>

first, i viewed the page source from the main page.

<figure><img src="../../../.gitbook/assets/Pasted image 20251110223224.png" alt=""><figcaption></figcaption></figure>

as we can see, there's another HTML `<script>` tags.

```javascript
  <script src="/static/terminal/js/commands.js" type="module"></script>
  <script src="/static/terminal/js/main.js" type="module"></script>
  <script src="/static/terminal/js/game.js" type="module"></script>
```



* **http\[:]//83\[.]136\[.]255\[.]235\[:]44748/static/terminal/js/commands.js**

<figure><img src="../../../.gitbook/assets/Pasted image 20251110223926.png" alt=""><figcaption></figcaption></figure>

this is the javascript code from `commands.js` file. the entire purposes is to manage the game's end state which is winning or losing.



* **http\[:]//83\[.]136\[.]255\[.]235\[:]44748/static/terminal/js/game.js**

<figure><img src="../../../.gitbook/assets/Pasted image 20251110223332 (1).png" alt=""><figcaption></figcaption></figure>

this is the javascript code from `game.js`. the purposes is to define and export all the text that will need to display in the game.



* **http\[:]//83\[.]136\[.]255\[.]235\[:]44748/static/terminal/js/main.js**

```javascript
async function CheckMessage() {
    fetchingResponse = true;
    currentCommand = commandHistory[commandHistory.length - 1];

    if (availableOptions[currentStep].includes(currentCommand) || availableOptions['secret'].includes(currentCommand)) {
        await fetch('/api/monitor', {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json'
            },
            body: JSON.stringify({ 'command': currentCommand })
        })
```

this snippet shows it has a secret command to reveal the flag in `availableOptions['secret']`. which means we must lurking for the secret word or command to reveal the flag.

```javascript
const fetchOptions = () => {
    fetch('/api/options')
        .then((data) => data.json())
        .then((res) => {
            availableOptions = res.allPossibleCommands;

        })
        .catch(() => {
            availableOptions = undefined;
        })
}
```

from this snippet, the vulnerability from this flag is from `/api/options`. this code above fetches a JSON file from `/api/options`and stores all possible commands in the `availableOptions`.



* **http\[:]//83\[.]136\[.]255\[.]235\[:]44748/api/options**

from the url, we got the secret word in `/api/options`.

<figure><img src="../../../.gitbook/assets/Pasted image 20251110224831.png" alt=""><figcaption></figcaption></figure>

```javascript
    "secret": [
      "Blip-blop, in a pickle with a hiccup! Shmiggity-shmack"
    ]
```

we paste the secret word to the game to print the flag.

<figure><img src="../../../.gitbook/assets/Pasted image 20251110225149.png" alt=""><figcaption></figcaption></figure>

&#x20;**`HTB{D3v3l0p3r_t00l5_4r3_b35t__t0015_wh4t_d0_y0u_Th1nk??}`**

{% hint style="danger" %}
The core vulnerability in this challenge is **Broken Access Control**. This flaw allows any user to bypass the intended game progression and capture the flag by submitting a hidden **`secret`** command.

This critical issue stems from two related root causes:

1. Sensitive Information Exposure: The server improperly exposes all game logic, including the hidden **`secret`** commands, via the **`/api/options`** JSON path. This file acts as a cheat sheet, sending confidential data directly to the client's browser.
2. Client-Side Enforcement of Security: Instead of validating commands on the server, the application relies on client-side JavaScript (**`main.js`**). The code explicitly checks if a user's input is in the **`availableOptions['secret']`** list, effectively creating a bypass that is visible to anyone who can read the source code.

The server should never have sent the secret commands to the client. By doing so, it provided all the information necessary to bypass the client-side security check.
{% endhint %}



