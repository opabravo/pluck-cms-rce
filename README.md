# pluck-cms-rce

This is a simple exploit POC to automate module installation that leads to RCE in Pluck CMS.

## Info

I've tried [Pluck v4.7.18 - Remote Code Execution (RCE)](https://www.exploit-db.com/exploits/51592) in a lab environment but it didn't work. 

So, I've decided to write a working version of the exploit.

## Usage

```bash
git clone https://github.com/opabravo/pluck-cms-rce
cd pluck-cms-rce
```

```bash
usage: exploit.py [-h] -u URL -p PASSWORD -f WEBSHELL_FP

Pluck CMS module install to RCE (Authenticated)

options:
  -h, --help            show this help message and exit
  -u URL, --url URL     Base URL
  -p PASSWORD, --password PASSWORD
                        Password
  -f WEBSHELL_FP, --webshell-fp WEBSHELL_FP
                        PHP web shell to upload

Example : python exploit.py -u http://pluck.local -p 'anti_sysadmin' -f phpinfo.php
```

## Demo

![image](https://i.imgur.com/y8NGxxp.png)