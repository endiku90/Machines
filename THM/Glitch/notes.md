![[Pasted image 20240606081112.png]]

## token
toke = this_is_not_real

## directory enumeration
/api/access
/api/items (POST GET HEAD)

## Exploit

ffuf -w $list -u http://IP/api/items?FUZZ=test -X POST -c -fc...

**Dinamic Code evaluation - eval()**: https://owasp.org/www-community/attacks/Direct_Dynamic_Code_Evaluation_Eval%20Injection


https://blog.appsecco.com/nodejs-and-a-simple-rce-exploit-d79001837cc6
https://medium.com/@sebnemK/node-js-rce-and-a-simple-reverse-shell-ctf-1b2de51c1a44


directory firefox -> credentials
https://github.com/lclevy/firepwd
v0id'    'love_the_void'



find / -perm -4000 2>/dev/null:
/usr/bin/doas -u root /bin/bash