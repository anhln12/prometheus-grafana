job_name: 'spring-actuator'
  scheme: https
  authorization:
      type: Bearer
      credentials: <your_token>
  tls_config:
      insecure_skip_verify: true
  metrics_path: '/actuator/prometheus'
  scrape_interval: 5s
  static_configs:
    - targets: ['your_ip:your_port']

  - job_name: "ucm"
    scheme: https
    scrape_interval: 5s
    metrics_path: '/ucm-benchmark/actuator/prometheus'
    static_configs:
      - targets: ["api-digital.asimgroup.vn"]


[refer](https://prometheus.io/docs/prometheus/latest/configuration/configuration/)
