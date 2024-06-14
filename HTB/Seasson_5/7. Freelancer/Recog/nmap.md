```bash
PORT      STATE SERVICE                                                                                  
53/tcp    open  domain                            
80/tcp    open  http                                        
88/tcp    open  kerberos-sec                                        
135/tcp   open  msrpc       
139/tcp   open  netbios-ssn
389/tcp   open  ldap                                       
445/tcp   open  microsoft-ds
464/tcp   open  kpasswd5                                             
593/tcp   open  http-rpc-epmap
636/tcp   open  ldapssl                                       
3268/tcp  open  globalcatLDAP
3269/tcp  open  globalcatLDAPssl
5985/tcp  open  wsman 
9389/tcp  open  adws
47001/tcp open  winrm                     
49664/tcp open  unknown
49665/tcp open  unknown      
49666/tcp open  unknown
49667/tcp open  unknown
49669/tcp open  unknown
49670/tcp open  unknown                                              
49671/tcp open  unknown                                              
49672/tcp open  unknown            
49675/tcp open  unknown  
55297/tcp open  unknown           
```

```bash

Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-06-04 19:01 CEST
Nmap scan report for 10.10.11.5
Host is up (0.11s latency).

PORT     STATE SERVICE       VERSION
53/tcp   open  domain        Simple DNS Plus
80/tcp   open  http          nginx 1.25.5
|_http-title: Did not follow redirect to http://freelancer.htb/
|_http-server-header: nginx/1.25.5
88/tcp   open  kerberos-sec  Microsoft Windows Kerberos (server time: 2024-06-04 22:01:58Z)
135/tcp  open  msrpc         Microsoft Windows RPC
139/tcp  open  netbios-ssn   Microsoft Windows netbios-ssn
389/tcp  open  ldap          Microsoft Windows Active Directory LDAP (Domain: freelancer.htb0., Site: Default-First-Site-Name)
445/tcp  open  microsoft-ds?
464/tcp  open  kpasswd5?
593/tcp  open  ncacn_http    Microsoft Windows RPC over HTTP 1.0
636/tcp  open  tcpwrapped
3268/tcp open  ldap          Microsoft Windows Active Directory LDAP (Domain: freelancer.htb0., Site: Default-First-Site-Name)
3269/tcp open  tcpwrapped
Service Info: Host: DC; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2024-06-04T22:02:06
|_  start_date: N/A
|_clock-skew: 4h59m59s

```