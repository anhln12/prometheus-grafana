# How to install Prometheus Node Exporter on Ubuntu 20.04

**1. Download Node Exporter**

  [available for Linux in the official Prometheus website here] (https://prometheus.io/download/#node_exporter)

  ```wget https://github.com/prometheus/node_exporter/releases/download/v1.3.1/node_exporter-1.3.1.linux-amd64.tar.gz```

**2. Extract Node Exporter and move binary **

  ```tar xvf node_exporter-1.3.1.linux-amd64.tar.gz
  cd node_exporter-1.3.1.linux-amd64
  cp node_exporter /usr/local/bin
  # Exit current directory
  cd ..
  # Remove the extracted directory
  rm -rf ./node_exporter-1.3.1.linux-amd64```

3. Create Node Exporter User
  ```
  sudo useradd --no-create-home --shell /bin/false node_exporter
  udo chown node_exporter:node_exporter /usr/local/bin/node_exporter
  ```
