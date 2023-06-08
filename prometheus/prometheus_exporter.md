# How to install Prometheus Node Exporter on Ubuntu 20.04

**1. Download Node Exporter**

[available for Linux in the official Prometheus website here](https://prometheus.io/download/#node_exporter)

```
wget https://github.com/prometheus/node_exporter/releases/download/v1.3.1/node_exporter-1.3.1.linux-amd64.tar.gz
```

**2. Extract Node Exporter and move binary**

```
tar xvf node_exporter-1.3.1.linux-amd64.tar.gz
cd node_exporter-1.3.1.linux-amd64
cp node_exporter /usr/local/bin
# Exit current directory
cd ..
# Remove the extracted directory
rm -rf ./node_exporter-1.3.1.linux-amd64
```
  
**3. Create Node Exporter User**

```
sudo useradd --no-create-home --shell /bin/false node_exporter
sudo chown node_exporter:node_exporter /usr/local/bin/node_exporter
```

**4. Create and start the Node Exporter service**

```
nano /etc/systemd/system/node_exporter.service

[Unit]
Description=Node Exporter
Wants=network-online.target
After=network-online.target

[Service]
User=node_exporter
Group=node_exporter
Type=simple
ExecStart=/usr/local/bin/node_exporter

[Install]
WantedBy=multi-user.target
```

```
sudo systemctl daemon-reload
```

**5. Test the Node Exporter service**

http://your_server_ip:9100/metrics

_Note: If port 9100 is unreachable_

```
sudo ufw allow 9100
sudo iptables -I INPUT -p tcp -m tcp --dport 9100 -j ACCEPT
```
[Refe](https://ourcodeworld.com/articles/read/1686/how-to-install-prometheus-node-exporter-on-ubuntu-2004)
