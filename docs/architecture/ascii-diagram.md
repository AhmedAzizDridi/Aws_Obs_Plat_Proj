# ASCII Architecture Diagram
 +-------------------------+
 | IT Admin |
 | Browser + SSH client |
 +-----------+-------------+
 |
 | HTTPS / SSH
 v
+-------------------------------------------------------------+
| AWS |
| |
| +---------------- VPC / Public Subnet ------------------+ |
| | | |
| | +---------------- EC2 Ubuntu ---------------------+ | |
| | | Docker Compose | | |
| | | - Prometheus | | |
| | | - Grafana | | |
| | | - AlertManager | | |
| | | - Loki later | | |
| | | - NGINX later | | |
| | +-------------------+-----------------------------+ | |
| | | | |
| +----------------------+--------------------------------+ |
+-------------------------|-----------------------------------+
 |
 | Scrape metrics / receive logs
 v
 +------------------+-----------------------+
 | Company Network |
 | Linux servers -> node_exporter |
 | Windows PCs -> windows_exporter |
 | Routers -> SNMP exporter later |
 | Websites -> blackbox exporter |
 +------------------------------------------+
