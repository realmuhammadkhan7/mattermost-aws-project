AWS Mattermost Deployment Project

This project demonstrates the deployment of Mattermost on AWS using a secure VPC-based architecture with public and private subnets.

------------------------------------
PROJECT OVERVIEW
------------------------------------

In this project, we deployed:
- Mattermost application on an EC2 instance (Application Server)
- MySQL database on a separate EC2 instance (Database Server)
- Custom VPC with public and private subnets
- Secure communication between application and database

------------------------------------
ARCHITECTURE USED
------------------------------------

- VPC CIDR: 10.0.0.0/16
- Public Subnet: 10.0.1.0/24
- Private Subnet: 10.0.2.0/24

Application Server:
- Located in Public Subnet
- Exposes Mattermost on port 8065
- Accessible from the internet

Database Server:
- Located in Private Subnet
- MySQL running on port 3306
- Accessible only from Application Server

------------------------------------
PORTS AND SECURITY
------------------------------------

- SSH: Port 22 (restricted access)
- MySQL: Port 3306 (TCP)
- Mattermost: Port 8065 (TCP)

Separate security groups were used for:
- Application Server
- Database Server

------------------------------------
STEPS PERFORMED
------------------------------------

1. Installed MySQL on Database Server
2. Retrieved temporary MySQL root password
3. Executed MySQL configuration script
4. Installed Mattermost on Application Server
5. Started Mattermost server
6. Accessed Mattermost via web browser

------------------------------------
SCREENSHOTS INCLUDED
------------------------------------

01-mysql-installation.png  
02-temp-mysql-password.png  
03-run-mysql-script.png  
04-mattermost-installation.png  
05-mattermost-server-running.png  
06-mattermost-web-ui.png  

------------------------------------
RESULT
------------------------------------

Mattermost was successfully deployed and accessed via browser using:
http://<Application-Server-Public-IP>:8065

------------------------------------
LEARNINGS
------------------------------------

- AWS VPC networking (CIDR, subnets, routing)
- Security Groups and port management
- EC2 based application deployment
- Secure database access using private subnet
- Git and GitHub for project version control

------------------------------------
AUTHOR
------------------------------------

Muhammad Umair Khan
