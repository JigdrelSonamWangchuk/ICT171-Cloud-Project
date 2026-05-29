# These are the command lines to access VM and Install Nginx

## To access VM
```bash
ssh -i “cloudserver-key.pem” Jigdrel@20.2.235.141
```

## Install Nginx
```bash
sudo apt update
sudo apt install nginx-full
```
## Edit index.html on the Webserver and Test
```bash
nano /var/www/html/index.html
```
