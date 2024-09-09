# Techplement
Techplement intern week 1 task:-

# WordPress Deployment on AWS (Monolithic and Microservices Architecture)

This repository contains the files and documentation to deploy a WordPress application on AWS in two different architectures: **Monolithic** and **Microservices**.

## Project Overview

- **Monolithic Architecture**: Deploy WordPress and MySQL on a single EC2 instance.
- **Microservices Architecture**: Deploy WordPress and MySQL on separate EC2 instances.

## Technologies Used

- **AWS EC2**: Hosting WordPress and MySQL instances.
- **WordPress**: Content Management System.
- **MySQL**: Database for WordPress.
- **Ubuntu**: Operating System for EC2 instances.
- **Apache**: Web server for WordPress.
  
## Setup Instructions

### Prerequisites

1. An AWS Free Tier account.
2. Basic knowledge of AWS services, especially EC2 and security groups.
3. SSH access to EC2 instances.

### Deployment Steps

#### 1. Monolithic Architecture

1. **Launch an EC2 Instance**:  
   - Instance Type: `t2.micro`
   - AMI: `Ubuntu Server 20.04 LTS (HVM), SSD Volume Type`
   - Security Group: Allow inbound traffic on ports `80` (HTTP) and `22` (SSH).

2. **Connect to EC2 Instance via SSH**:  
   ```bash
   ssh -i "your-key.pem" ubuntu@your-ec2-public-ip
Install Apache, MySQL, and PHP:
Run the setup-wordpress.sh script to install and configure necessary packages.

Deploy WordPress:
Download and set up WordPress in the /var/www/html/ directory.

2. Microservices Architecture
Launch Two EC2 Instances:

Instance 1: WordPress Server (t2.micro).
Instance 2: MySQL Database Server (t2.micro).
Configure Security Groups:

Allow HTTP (80) and SSH (22) for WordPress Instance.
Allow MySQL (3306) for the MySQL instance, accessible from the WordPress instance's IP.
Connect to Each Instance via SSH:
Configure each server as needed for their specific roles.

Edit wp-config.php:
Modify the WordPress configuration file to point to the remote MySQL server.

Troubleshooting Tips
Database Connection Issues: Ensure correct credentials in wp-config.php and that MySQL server allows remote connections.
Permission Errors: Verify file permissions and ownership in the WordPress directory.
Credits
WordPress Official Documentation
AWS EC2 Documentation
**Resources used**:
AWS EC2
Ubuntu
WordPress
apache server 
mysql database
EC2 Instances and Security Groups

**WordPress Welcome Page**
Please check the screenshots/ folder for images showing the configurations.
