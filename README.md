Title: AWS Mattermost Deployment (VPC + Public/Private Subnets + RDS)

Overview
Is project me maine AWS pe Mattermost deploy kiya using secure cloud architecture. Isme networking, security groups, database connectivity, aur application access proper tariqay se configure kiya gaya.

Architecture

VPC (10.0.0.0/16)

Public Subnet (App server)

Private Subnet (Database server)

Security Groups (App: 22/8065, DB: 3306 only from App SG)

Mattermost runs on port 8065

Key Steps Performed

Created VPC, subnets, route tables, and IGW

Launched EC2 instance for Mattermost

Configured security groups and inbound/outbound rules

Installed and started Mattermost server

Accessed the application via browser: http://<public-ip>:8065

Proof / Screenshots

Added screenshots in repo: Picture1.png … Picture6.png

What I Learned

CIDR planning + subnetting (overlap avoidance)

Secure access using SG rules (least privilege)

App-to-DB communication over TCP 3306

Exposing app via public IP and custom port 8065

Basic troubleshooting (service logs + connectivity)
