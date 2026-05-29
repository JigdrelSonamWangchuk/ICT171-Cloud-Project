# Commands to Create Proper Nginx Server Block

##  Create Config File:
sudo nano /etc/gnix/sites-available/jigdrel.shop

## Add:
```bash
server {
    listen 80;
    server_name jigdrel.shop www.jigdrel.shop;

    root /var/www/html;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}
```
## Enable
```bash
sudo ln -s /etc/nginx/sites-available/yourdomain.com /etc/nginx/sites-enabled/
```

## Test Config
```bash
Sudo nginx -t
```

## Restart Nginx
```bash
sudo systemctl restart nginx
```

## Install SSL
```bash
sudo apt update
sudo apt install certbot python3-certbot-ngnix -y
```

## Request Certificate
```bash
sudo certbot --nginx -d jigdrel.shop -d www.jigdrel.shop
```


