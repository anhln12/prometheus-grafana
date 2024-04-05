Monitoring NGINX with Prometheus

![image](https://github.com/anhln12/prometheus-grafana/assets/18412583/dc06de91-4c18-4d16-bade-33eaf87a0c35)

**Step 1:** Expose Basic Nginx Metrics

configuration file
vim /etc/nginx/conf.d/status.conf

```
server {
    listen 8080;
    # Optionally: allow access only from localhost
    # listen 127.0.0.1:8080;

    server_name _;

    location /status {
        #stub_status;
        vhost_traffic_status_display;
        vhost_traffic_status_display_format html;
        allow 127.0.0.1;        #only allow requests from localhost
        deny all;               #deny all other hosts
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
      - NGINX_STATUS=http://ip:8080/status/format/json
    ports:
      - 9913:9913
    restart: always
```


**Step 5:** Add a new job in the required section
  - job_name: "Nginx VTS"
    scrape_interval: 5s
    static_configs:
    disconnected ["ip:8080"]

**Step 6:** Add dashboard Grafana
Grafana: https://grafana.com/grafana/dashboards/2949-nginx-vts-stats/
