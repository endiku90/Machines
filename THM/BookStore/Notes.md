```bash
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-06-15 17:08 CEST
Nmap scan report for bookstore.thm (10.10.172.106)
Host is up (0.46s latency).
Not shown: 997 closed tcp ports (reset)
PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 44:0e:60:ab:1e:86:5b:44:28:51:db:3f:9b:12:21:77 (RSA)
|   256 59:2f:70:76:9f:65:ab:dc:0c:7d:c1:a2:a3:4d:e6:40 (ECDSA)
|_  256 10:9f:0b:dd:d6:4d:c7:7a:3d:ff:52:42:1d:29:6e:ba (ED25519)
80/tcp   open  http    Apache httpd 2.4.29 ((Ubuntu))
|_http-server-header: Apache/2.4.29 (Ubuntu)
|_http-title: Book Store
5000/tcp open  http    Werkzeug httpd 0.14.1 (Python 3.6.9)
|_http-title: Home
| http-robots.txt: 1 disallowed entry 
|_/api </p> 
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 24.06 seconds

```


- Bookstore
    
    - tcp/80
        
        - directories
            
            - index.html
                
            - login.html
	                <!--Still Working on this page will add the backend support soon, also the debugger pin is inside sid's bash history file -->

            - books.html
		            - <!--GY4CANZUEA3TIIBXGAQDOMZAGNQSAMTGEAZGMIBXG4QDONZAG43SAMTFEA3TSIBWMYQDONJAG42CANZVEA3DEIBWGUQDEZJAGYZSANTGEA3GIIBSMYQDONZAGYYSANZUEA3DGIBWHAQDGZRAG43CAM3EEA2TIIBXGQQDGNZAGYZCAN3BEA3TQIBXGUQDOMRAGRQSAMZREA2DS=== -->
                
            - images
                
            - javascript
                
            - server-status
                
        - subdomains
            
    - tcp/22
        
    - tcp/5000
        
        - /console
            
        - /api
            
            - /api/v2/resources/books/all (Retrieve all books and get the output in a json format)
                
            - /api/v2/resources/books/random4 (Retrieve 4 random records)
                
            - /api/v2/resources/books?id=1(Search by a specific parameter , id parameter)
                
            - /api/v2/resources/books?author=J.K. Rowling (Search by a specific parameter, this query will return all the books with author=J.K. Rowling)
                
            - /api/v2/resources/books?published=1993 (This query will return all the books published in the year 1993)
                
            - /api/v2/resources/books?author=J.K. Rowling&published=2003 (Search by a combination of 2 or more parameters)