# SuiNode
how to install Sui node

Install 

 Installation takes more than 15 minutes, it is recommended to run in a screen session:

```screen -S sui```

# Using script for a quick installation:

```wget -O sui.sh https://api.nodes.guru/sui.sh && chmod +x sui.sh && ./sui.sh```

# Check node:

```curl -s -X POST http://127.0.0.1:9000 -H 'Content-Type: application/json' -d '{ "jsonrpc":"2.0", "method":"rpc.discover","id":1}' | jq .result.info```

 Check node logs:

```journalctl -u suid -f -o cat```

 Restart node:

```sudo systemctl restart suid```

 Stop node:

```sudo systemctl stop suid```

 Delete node:

```sudo systemctl stop suid
sudo systemctl disable suid
rm -rf ~/sui /var/sui/ /usr/local/bin/sui*
rm /etc/systemd/system/suid.service
```

Network Update 

```systemctl stop suid```

```rm -rf /var/sui/db/*```

```systemctl restart suid```
