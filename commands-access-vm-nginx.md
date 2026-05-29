# These are the command lines to access VM and Install Nginx

## To access VM
ssh -i “webserver-key.pem” ububtu@20.2.235.141 

## Install Nginx
sudo apt update
sudo apt install nginx-full

## Edit index.html on the Webserver and Test
nano /var/www/html/index.html
