# AWS Security Baseline
## Root account
- MFA enabled: yes/no
- Root access used only for billing and account recovery: yes/no
## IAM admin user
- Admin user created: yes/no
- MFA enabled: yes/no
- Access keys created: only if needed
## Password and key rules
- No AWS keys in Git
- No PEM files in Git
- SSH key stored securely
- Use least privilege after MVP
## Network rules for future EC2
- SSH allowed only from admin public IP
- Grafana only through HTTPS after NGINX setup
- Prometheus not public
