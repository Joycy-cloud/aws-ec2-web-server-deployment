# AWS EC2 Web Server Deployment

## Project Overview
This project demonstrates how to deploy a publicly accessible static website on an Amazon EC2 virtual machine using Amazon Linux 2023 and Apache HTTP Server.

The EC2 instance is configured with a security group to control inbound traffic, and the website is served over HTTP.

## Technologies Used
- AWS EC2
- Amazon Linux 2023
- Apache HTTP Server
- AWS Security Groups
- SSH
- Git Bash
- HTML and CSS

## Architecture
User Browser → Internet → AWS Security Group → EC2 Instance → Apache Web Server → Website

## Implementation Steps

1. Launched an EC2 instance using Amazon Linux 2023.
2. Configured an SSH key pair for secure remote access.
3. Created a security group with:
   - SSH (Port 22): Restricted to My IP.
   - HTTP (Port 80): Allowed from Anywhere IPv4.
4. Connected to the instance using SSH from Git Bash.
5. Updated system packages using DNF.
6. Installed Apache HTTP Server.
7. Started and enabled the Apache service.
8. Created a custom HTML webpage.
9. Verified the webpage using localhost and a web browser.

## Commands Used

### Update system
```bash
sudo dnf update -y
```

### Install Apache
```bash
sudo dnf install httpd -y
```

### Start Apache
```bash
sudo systemctl start httpd
```

### Enable Apache at startup
```bash
sudo systemctl enable httpd
```

### Check Apache status
```bash
sudo systemctl status httpd
```

### Test locally
```bash
curl http://localhost
```

## Screenshots

### Deployed Website
![Website](screenshots/website.png)

### Apache Server Status
![Apache Status](screenshots/apache-status.png)

### EC2 Instance
![EC2 Instance](screenshots/ec2-instance.png)

## Learning Outcomes
- Understanding AWS EC2 instance provisioning.
- Configuring inbound traffic using security groups.
- Connecting to a Linux server through SSH.
- Installing and managing Apache using systemctl.
- Hosting and accessing a static website on AWS.

## Future Improvements
- Automate deployment using Jenkins.
- Containerize the application using Docker.
- Configure HTTPS using SSL/TLS.
- Manage infrastructure using Terraform.

## Author
Joycy John Lobo