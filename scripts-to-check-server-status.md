# Short Script to Check Server Status

## Create a Scripts Folder
```bash
mkdir scripts
cd scripts
```
## Create a Script File
```bash
nano server-check.sh
```
## Paste This Script
```bash
#!/bin/bash
echo "===== Server Status Check ====="
echo

echo "Current Date and Time:"
date
echo

echo "Server Uptime:"
uptime
echo

echo "Disk Usage:"
df -h
echo

echo "Nginx Status:"
systemctl is-active nginx
echo

echo "MySQL Status:"
systemctl is-active mysql
echo

echo "Public IP Address:"
curl ifconfig.me
echo
```
## Make it Executable
```bash
chmod +x server-check.sh
```
## Run the Script
```bash
./server-check.sh
```

