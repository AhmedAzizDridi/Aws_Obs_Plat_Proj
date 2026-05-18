# Project Charter - AWS Observability and Incident Response Platform
## Problem statement
The company needs centralized visibility into servers, PCs, services, and network health. Current
troubleshooting is manual and reactive.
## Objective
Build a secure AWS-hosted observability platform that collects infrastructure metrics, displays dashboards,
triggers alerts, and later supports centralized logging and AI-assisted incident analysis.
## In scope
- AWS infrastructure foundation
- EC2 monitoring server
- Dockerized observability stack
- Prometheus metrics
- Grafana dashboards
- AlertManager notifications
- Linux and Windows device monitoring
- Centralized logging in later phase
- Infrastructure automation in later phase
- Documentation and handover
## Out of scope for first production version
- Kubernetes cluster
- Full SIEM implementation
- Automatic remediation on production machines
- Public access to Prometheus
- Storing company secrets in Git
## Success criteria
- At least one Linux server monitored
- At least one Windows machine monitored
- Grafana dashboard accessible securely
- Alerts sent for downtime or resource saturation
- Documentation completed for deployment, backup, and recovery
## Main stakeholders
- IT operations
- Management
- End users affected by infrastructure incidents
## Project owner
Ahmed Aziz Dridi
