# NGINX Reverse Proxy Different Port 

> ### มี app 2 ตัว
> :88
> :89

### Step 1 install nginx
```sh
$ apt-get install nginx -y
```

### Step 2 edit site available
```sh
$ vi /etc/nginx/site-available/default
```

### example
```sh
server {
    listen 80;
    server_name app.domain.com;
    location / {
        proxy_set_header Host $host;
        proxy_pass http://127.0.0.1:88;
        proxy_redirect off;
    }
}
server {
    listen 80;
    server_name api.domain.com;
    location / {
        proxy_set_header Host $host;
        proxy_pass http://127.0.0.1:89;
        proxy_redirect off;
    }
}
```

### Step 3 restart nginx
```sh
$ systemctl restart nginx
```