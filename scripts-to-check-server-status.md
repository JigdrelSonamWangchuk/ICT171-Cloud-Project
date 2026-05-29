# Short Script to Ccheck Server Status

```bash
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
