whatweb
```bash
gobuster dir -u runner.htb -w /usr/share/seclists/Discovery/Web-Content/raft-medium-directories.txt 

ffuf -w /usr/share/seclists/Discovery/Web-Content/raft-medium-directories.txt -u http://runner.htb/FUZZ -fc 200 -c 


cewl http://runner.htb -d3 --lowercase > conten/cewl.txt```

Recognaisse
```
ffuf -w /usr/share/seclists/Discovery/Web-Content/raft-medium-directories.txt -u http://runner.htb/FUZZ -fc 200 -c  

gobuster dir -u runner.htb -w /usr/share/seclists/Discovery/Web-Content/raft-medium-directories.txt 

cewl http://runner.htb -d3 --lowercase > conten/cewl.txt
cewl http://runner.htb -d2 --lowercase > conten/cewl.txt
```

gobuster vhost -u runner.htb -w conten/cewl.txt !!!! FALLA ?¿!

``` bash
ffuf -w conten/cewl.txt -u http://FUZZ.runner.htb -fc 200 -c 

python3 exploit.py -t http://teamcity.runner.htb  -u test -p test

#Extraction
7z x TeamCity_Backup_20240425_115048.zip

