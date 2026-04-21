# cloudflare
```
docker run -d \
  --name cloudflared-tunnel \
  --restart always \
  cloudflare/cloudflared:latest \
  tunnel --no-autoupdate run --token <YOUR_TOKEN>
```
