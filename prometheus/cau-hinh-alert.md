**Cấu hình Alert trong prometheus**

1. Cài đặt AlerManager trên serverr Promethus

Bước 1: Download alert_manager
```
wget https://github.com/prometheus/alertmanager/releases/download/v0.21.0/alertmanager-0.21.0.linux-amd64.tar.gz
```

Bước 2: Giải nén và copy vào thư mục /usr/local để dễ dàng quản lý
```
tar -xvzf alertmanager-0.21.0.linux-amd64.tar.gz
mv alertmanager-0.21.0.linux-amd64 /usr/local/alertmanager
```

Bước 3: Tạo user để chạy service alert_manager
```
useradd --no-create-home --shell /bin/false alert_manager
```

Phân quyền cho user vừa tạo là owner của thư mục source alert_manager
```
chown -R alert_manager:alert_manager /usr/local/alertmanager
```

Tạo service trong systemd cho alertmanager
```
vi /etc/systemd/system/alertmanager.service
```

Nội dung file service như sau:
```
[Unit]
Description=AlertManager
Wants=network-online.target
After=network-online.target

[Service]
User=alert_manager
Group=alert_manager
Type=simple
ExecStart=/usr/local/alertmanager/alertmanager --config.file=/usr/local/alertmanager/alertmanager.yml -cluster.advertise-address=0.0.0.0:9093

[Install]
WantedBy=multi-user.target
```

Enable và start service
```
systemctl daemon-reload
systemctl enable alertmanager
systemctl restart alertmanager
```

==Cài đặt docker==

Tạo ra file alertmanager.yml
```
global:
  resolve_timeout: 5m

route:
  group_by: ['alertname']
  group_wait: 10s
  group_interval: 5m
  repeat_interval: 30m
  receiver: 'web.hook'
receivers:
- name: 'web.hook'
  webhook_configs:
  - url: 'http://localhost:9087/alert/-364942581'
inhibit_rules:
  - source_match:
      severity: 'critical'
    target_match:
      severity: 'warning'
    equal: ['alertname', 'dev', 'instance']
```

Tạo file docker-compose.yaml
```
cat docker-compose.yml
version: '2'
services:
 ​​ ​​ ​​​​ alertmanager:
 ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ image: prom/alertmanager
 ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ privileged: true
 ​​ ​​ ​​ ​​​​  ​​ ​​​​ volumes:
 ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ - /alertmanager/alertmanager.yml:/alertmanager/alertmanager.yml
 ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ command:
 ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ - '--config.file=/alertmanager/alertmanager.yml'
 ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ ports:
 ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ - '9093:9093'
 ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ - '9094:9094'
```

Khởi tạo container
```
docker-compose up
```


**3. Cài đặt và cấu hình promethus_bot để gửi thông báo qua Telegram**
```
# Tải mã nguồn
git clone https://github.com/inCaller/prometheus_bot.git

# Build mã nguồn
cd prometheus_bot
make clean
make

# Copy vào thư mục /usr/local
sudo mkdir /usr/local/prometheus_bot
sudo cp prometheus_bot /usr/local/prometheus_bot

# Tạo tệp cấu hình cho prometheus_bot
# Nội dung xem bên dưới
sudo nano /usr/local/prometheus_bot/config.yaml

# Sao chép template gửi tin nhắn
sudo cp testdata/production_example.tmpl /usr/local/prometheus_bot/template.tmpl

# Test thử bằng lệnh, nhớ đổi lại chat_id
cp /usr/local/prometheus_bot/config.yaml .
export TELEGRAM_CHATID="-364942581"
make test
```

Nội dung tệp config.yam
```
telegram_token: "997872129:AAEPKYz3nPwmFsgq6ao-MdPsC5fy5z376GQ"

# ONLY IF YOU USING TEMPLATE required for test
# template_path: "/usr/local/prometheus_bot/template.tmpl"
time_zone: "Asia/Ho_Chi_Minh"
split_token: "|"

# ONLY IF YOU USING DATA FORMATTING FUNCTION, NOTE for developer: important or test fail
time_outdata: "02/01/2006 15:04:05"
split_msg_byte: 4000
```

Bây giờ chúng ta tạo service chạy prometheus_bot
```
[Unit]
Description=Prometheus Bot
After=network.target
 
[Service]
User=root
Group=root
Type=simple
ExecStart=/usr/local/prometheus_bot/prometheus_bot -c /usr/local/prometheus_bot/config.yaml
 
[Install]
WantedBy=multi-user.target
```

Các lệnh chạy dịch vụ
```
# Cấu hình để tự bật dịch vụ khi server khởi động
sudo systemctl daemon-reload
sudo systemctl enable prometheus_bot

# Bật dịch vụ
sudo service prometheus_bot start

# Tắt dịch vụ
sudo service prometheus_bot stop

# Xem trạng thái
sudo service prometheus_bot status
```

**4. Cấu hình alertmanager**
Bây giờ ta sửa tệp /usr/local/alertmanager/alertmanager.yml



