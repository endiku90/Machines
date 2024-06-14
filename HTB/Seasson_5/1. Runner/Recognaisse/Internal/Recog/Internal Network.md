```
john@runner:~$ ss -tulnp
Netid                State                 Recv-Q                Send-Q                                 Local Address:Port                                 Peer Address:Port                Process                
udp                  UNCONN                0                     0                                      127.0.0.53%lo:53                                        0.0.0.0:*                                          
udp                  UNCONN                0                     0                                            0.0.0.0:68                                        0.0.0.0:*                                          
tcp                  LISTEN                0                     4096                                   127.0.0.53%lo:53                                        0.0.0.0:*                                          
tcp                  LISTEN                0                     4096                                       127.0.0.1:8111                                      0.0.0.0:*                                          
tcp                  LISTEN                0                     4096                                       127.0.0.1:9443                                      0.0.0.0:*                                          
tcp                  LISTEN                0                     511                                          0.0.0.0:80                                        0.0.0.0:*                                          
tcp                  LISTEN                0                     128                                          0.0.0.0:22                                        0.0.0.0:*                                          
tcp                  LISTEN                0                     4096                                       127.0.0.1:9000                                      0.0.0.0:*                                          
tcp                  LISTEN                0                     4096                                       127.0.0.1:5005                                      0.0.0.0:*                                          
tcp                  LISTEN                0                     4096                                               *:8000                                            *:*                                          
tcp                  LISTEN                0                     511                                             [::]:80                                           [::]:*                                          
tcp                  LISTEN                0                     128                                             [::]:22                                           [::]:*         ```


### tcp 8111:
john@runner:/etc/nginx/sites-available$ cat teamcity 
server {
    listen 80;
    server_name teamcity.runner.htb;

    location / {
        proxy_pass http://localhost:8111;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
        proxy_buffering off;
        proxy_request_buffering off;
        proxy_http_version 1.1;
        proxy_intercept_errors on;
    }
}

### tcp9443
server {
    listen 80;
    server_name portainer-administration.runner.htb;

    location / {
        proxy_pass https://localhost:9443;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}
```

puerto 9000 parece portainer

```bash
9999/tcp open  jdwp    Java Debug Wire Protocol (Reference Implementation) version 17.0 17.0.7

```