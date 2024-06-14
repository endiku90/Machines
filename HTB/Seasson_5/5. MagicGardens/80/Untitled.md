``` 
whatweb http://magicgardens.htb/

http://magicgardens.htb/ [200 OK] Bootstrap, Country[RESERVED][ZZ], HTTPServer[nginx/1.22.1], IP[10.10.11.9], Title[Magic Gardens], UncommonHeaders[x-content-type-options,referrer-policy,cross-origin-opener-policy], X-Frame-Options[DENY], nginx[1.22.1]
```

```bash
┌─[endiku@parrot]─[~/HTB/Seasson_5/MagicGardens]
└──╼ $ gobuster dir -u magicgardens.htb -w /usr/share/seclists/Discovery/Web-Content/raft-medium-directories.txt 
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://magicgardens.htb
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/seclists/Discovery/Web-Content/raft-medium-directories.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.6
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/admin                (Status: 301) [Size: 0] [--> /admin/]
/search               (Status: 301) [Size: 0] [--> /search/]
/logout               (Status: 301) [Size: 0] [--> /logout/]
/login                (Status: 301) [Size: 0] [--> /login/]
/register             (Status: 301) [Size: 0] [--> /register/]
/catalog              (Status: 301) [Size: 0] [--> /catalog/]
/cart                 (Status: 301) [Size: 0] [--> /cart/]
/profile              (Status: 301) [Size: 0] [--> /profile/]
/subscribe            (Status: 301) [Size: 0] [--> /subscribe/]
/check                (Status: 301) [Size: 0] [--> /check/]
/restore              (Status: 301) [Size: 0] [--> /restore/]
```
