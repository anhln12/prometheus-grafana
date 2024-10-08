Monitoring NGINX with Prometheus

![image](https://github.com/anhln12/prometheus-grafana/assets/18412583/dc06de91-4c18-4d16-bade-33eaf87a0c35)

**Step 1:** Expose Basic Nginx Metrics

configuration file
vim /etc/nginx/conf.d/status.conf

```
server {
    #listen 8088;
    # Optionally: allow access only from localhost
    listen 10.30.18.61:8088;

    server_name _;
    location /metrics {
    stub_status on;
    }
    location /status {
        #stub_status;
        #               auth_basic "Restricted";
        #       auth_basic_user_file /etc/nginx/.htpasswd;
        vhost_traffic_status_display;
        vhost_traffic_status_display_format html;
        #allow 127.0.0.1;        #only allow requests from localhost
        #deny all;               #deny all other hosts
    }
}
```

**Step 2:** Configuration is valid
```
nginx -t
```

**Step 3:** To update the Nginx config without downtime
```
systemctl reload nginx
```

**Step 4:** Run docker nginxvts

docker-compose.yml 
```
version: "3"
services:
  nginx-vts-exporter:
    image: sophos/nginx-vts-exporter
    environment:
      - NGINX_STATUS=http://10.30.18.61:8088/status/format/json
    ports:
      - 172.30.18.61:9913:9913
    restart: always
```


**Step 5:** Add a new job in the required section
```
  - job_name: "Nginx LB02 INF VTS"
    scrape_interval: 5s
    #scheme: http
    #metrics_path: '/metrics'
    static_configs:
      - targets: ["ip:9913"]


```
**Step 6:** Add dashboard Grafana
Grafana: https://grafana.com/grafana/dashboards/2949-nginx-vts-stats/




# how to compile and install the Nginx module – ngx_http_vhost_traffic_status

The module gathers traffic information per the server blocks and upstream servers and shows information for Nginx proxy cache like used space.

Server zones information
    Requests – Total, Requests/s, Time
    Responses – 1xx, 2xx, 3xx, 4xx, 5xx, Total
    Traffic – Sent, Received, Sent/s, Received/s
    Cache – Miss, Bypass, Expired, Stale, Updating, Revalidated, Hit, Scarce, Total

Building the module

Step 1: Download the module

https://github.com/vozlt/nginx-module-vts 

git clone https://github.com/vozlt/nginx-module-vts

Step 2: Build 

Kiểm tra version nginx đang sử dụng: nginx -V

Download version nginx trùng với version nginx đã được cài đặt

wget https://nginx.org/download/nginx-1.18.0.tar.gz

Tiến hành biên dịch: 
```
cd nginx-1.18.0
./configure --with-compat --add-dynamic-module=/home/anhle4/nginx-module-vts
```
Tiến hành biên dịch:
```
make
```
Note:
```
apt-get install build-essential libpcre3 libpcre3-dev zlib1g zlib1g-dev libssl-dev libgd-dev libxml2 libxml2-dev uuid-dev
```

Sau khi biên dịch xong ta sẽ thu được file nhị phân của module nginx-vts. Copy file vào đường dẫn module của nginx
```
cp objs/ngx_http_vhost_traffic_status_module.so /usr/lib/nginx/modules/
```

Step 3: Use the module
```
user nginx nginx;
worker_processes auto;
pid /run/nginx.pid;
worker_rlimit_nofile 100000;
 
error_log /var/log/nginx/error_log info;
 
#load modules
load_module modules/ngx_http_vhost_traffic_status_module.so;
```

Step 4: Reload nginx


# Fix lỗi 501 Not implemented

problem has fixed when added http block vhost_traffic_status_zone

```
http {
    vhost_traffic_status_zone;
        vhost_traffic_status_filter_by_host on;

    ...

    server {

        ...

        location /status {
            vhost_traffic_status_display;
            vhost_traffic_status_display_format html;
        }
    }
}
```

**Kết quả:**

http://172.30.12.52:8088/status/

<img width="590" alt="image" src="https://github.com/anhln12/prometheus-grafana/assets/18412583/ef1b155f-1a0d-4e52-85c8-299764226d36">


Refer:
[https://grafana.com/grafana/dashboards/11967-nginx-vts-sts-performance-metrics/](https://grafana.com/grafana/dashboards/2949-nginx-vts-stats/)


















