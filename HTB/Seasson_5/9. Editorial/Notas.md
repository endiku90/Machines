submissions@tiempoarriba.htb
[git] [api]

- Editorial 10.10.11.20
    
    - Enum
        
        - TCP/80
            
            - /about
                
            - /upload
                
            - /upload-cover
                
                - URL
	                - [SSRF]
				            localhost:5000/api
                    
                - file
                    
        - TCP/22
            
    - InternalEnum(user dev)
        
        - ## ./apps/.git
            
            - git log
                
                - git show $num_commit
                    
        - netstat -tulnp
            
        - uname -a
            
        - Lateral
            
            - user prod
                
                - sudo -l
                    
                    - python injection
	                    - https://security.snyk.io/vuln/SNYK-PYTHON-GITPYTHON-3113858