# cloudflare-client-ssh
https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-windows-amd64.exe

https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-windows-amd64.msi

## config
```
Host hostname
    HostName hostname
    User user
    ProxyCommand cloudflared access ssh --hostname %h
```
## connect
ssh hostname
## scp
### file
scp E:\README hostname:/home/user/README
### folder
scp -r E:\folder hostname:/home/user/folder
## test
ssh user@hostname -o "ProxyCommand=cloudflared access ssh --hostname %h"
## fix loi REMOTE HOST IDENTIFICATION HAS CHANGED
ssh-keygen -R hostname
