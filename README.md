## Docker yml files

Ngnix config 

```
location / {
    proxy_pass http://guacamole:8080/;
    proxy_buffering off;
    proxy_http_version 1.1;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection $http_connection;
    proxy_cookie_path / /;
    access_log off;
}
```
