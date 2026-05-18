# Architecture Overview
## Objective
Build an AWS-hosted observability platform for monitoring company infrastructure.
## High-level components
- Company devices: Windows PCs, Linux servers, routers, and services
- Exporters: node_exporter, windows_exporter, blackbox_exporter, SNMP exporter
- AWS EC2: central monitoring server
- Docker Compose: service orchestration
- Prometheus: metrics collection
- Grafana: dashboards and visualization
- AlertManager: notifications
- Loki: centralized logs in later volume
- NGINX: reverse proxy and HTTPS in later volume
## Data flow
1. Exporters expose metrics on company devices.
2. Prometheus scrapes exporter endpoints.
3. Grafana queries Prometheus.
4. AlertManager sends notifications when alert rules fire.
5. Logs will be collected by Promtail and viewed in Grafana later.
## Security principles
- SSH key only
- MFA on AWS account
- Least privilege IAM
- No public Prometheus access
- Grafana exposed only through HTTPS
- Secrets excluded from Git
