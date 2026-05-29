# Commands to Create Proper Nginx Server Block

##  Create Config File:
sudo nano /etc/gnix/sites-available/jigdrel.shop

## Add:
server {
    listen 80;
    server_name jigdrel.shop www.jigdrel.shop;

    root /var/www/html;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}

## Enable
sudo ln -s /etc/nginx/sites-available/yourdomain.com /etc/nginx/sites-enabled/

## Test Config
Sudo nginx -t

## Restart Nginx
sudo systemctl restart nginx

## Install SSL
sudo apt update
sudo apt install certbot python3-certbot-ngnix -y

## Request Certificate
sudo certbot --nginx -d jigdrel.shop -d www.jigdrel.shop


