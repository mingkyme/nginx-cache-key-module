# nginx-cache-key-module

This modules is copied of [[free-nginx 1.27.](https://freenginx.org/)] repo.

```nginx
server {
    proxy_cache my_zone;
    add_header X-Cache-Key $cache_key always;
    location / {
        proxy_pass http://origin;
    }
}
```

```bash
curl -I $URL/1.jpg
X-Cache-Status: HIT
X-Cache-Key: http://origin/1.jpg
```
