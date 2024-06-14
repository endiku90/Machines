```bash 
PORT    STATE SERVICE VERSION
22/tcp  open  ssh     OpenSSH 8.2p1 Ubuntu 4ubuntu0.11 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 07:b0:58:b5:8e:02:d0:35:4e:bf:09:42:a6:4c:cb:92 (RSA)
|   256 b0:8d:04:28:52:ce:7b:42:46:cf:52:bb:66:d4:56:56 (ECDSA)
|_  256 3c:b1:66:c0:d1:3a:1b:29:55:6e:99:96:84:93:e9:4e (ED25519)
25/tcp  open  smtp    Postfix smtpd
|_smtp-commands: mail.filepath.lab, PIPELINING, SIZE 10240000, VRFY, ETRN, STARTTLS, ENHANCEDSTATUSCODES, 8BITMIME, DSN, SMTPUTF8, CHUNKING
| ssl-cert: Subject: commonName=ip-10-10-31-82.eu-west-1.compute.internal
| Subject Alternative Name: DNS:ip-10-10-31-82.eu-west-1.compute.internal
| Not valid before: 2021-11-10T16:53:34
|_Not valid after:  2031-11-08T16:53:34
|_ssl-date: TLS randomness does not represent time
110/tcp open  pop3    Dovecot pop3d
|_pop3-capabilities: SASL CAPA STLS PIPELINING AUTH-RESP-CODE UIDL RESP-CODES TOP
| ssl-cert: Subject: commonName=ip-10-10-31-82.eu-west-1.compute.internal
| Subject Alternative Name: DNS:ip-10-10-31-82.eu-west-1.compute.internal
| Not valid before: 2021-11-10T16:53:34
|_Not valid after:  2031-11-08T16:53:34
|_ssl-date: TLS randomness does not represent time
143/tcp open  imap    Dovecot imapd (Ubuntu)
|_ssl-date: TLS randomness does not represent time
|_imap-capabilities: listed more ENABLE have IDLE LOGINDISABLEDA0001 post-login OK ID capabilities STARTTLS Pre-login LOGIN-REFERRALS SASL-IR IMAP4rev1 LITERAL+
| ssl-cert: Subject: commonName=ip-10-10-31-82.eu-west-1.compute.internal
| Subject Alternative Name: DNS:ip-10-10-31-82.eu-west-1.compute.internal
| Not valid before: 2021-11-10T16:53:34
|_Not valid after:  2031-11-08T16:53:34
Service Info: Host:  mail.filepath.lab; OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 25.00 seconds
```


mail.filepath.lab