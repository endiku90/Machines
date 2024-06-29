```bash
PORT     STATE SERVICE       VERSION
25/tcp   open  smtp          hMailServer smtpd
| smtp-commands: MAINFRAME, SIZE 20480000, AUTH LOGIN, HELP
|_ 211 DATA HELO EHLO MAIL NOOP QUIT RCPT RSET SAML TURN VRFY
53/tcp   open  domain        Simple DNS Plus
80/tcp   open  http          Microsoft IIS httpd 10.0
|_http-title: Axlle Development
| http-methods: 
|_  Potentially risky methods: TRACE
|_http-server-header: Microsoft-IIS/10.0
88/tcp   open  kerberos-sec  Microsoft Windows Kerberos (server time: 2024-06-24 12:55:58Z)
135/tcp  open  msrpc         Microsoft Windows RPC
139/tcp  open  netbios-ssn   Microsoft Windows netbios-ssn
445/tcp  open  microsoft-ds?
3389/tcp open  ms-wbt-server Microsoft Terminal Services
|_ssl-date: 2024-06-24T12:56:46+00:00; 0s from scanner time.
| ssl-cert: Subject: commonName=MAINFRAME.axlle.htb
| Not valid before: 2024-05-19T11:25:03
|_Not valid after:  2024-11-18T11:25:03
| rdp-ntlm-info: 
|   Target_Name: AXLLE
|   NetBIOS_Domain_Name: AXLLE
|   NetBIOS_Computer_Name: MAINFRAME
|   DNS_Domain_Name: axlle.htb
|   DNS_Computer_Name: MAINFRAME.axlle.htb
|   DNS_Tree_Name: axlle.htb
|   Product_Version: 10.0.20348
|_  System_Time: 2024-06-24T12:56:06+00:00
Service Info: Host: MAINFRAME; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2024-06-24T12:56:10
|_  start_date: N/A
```