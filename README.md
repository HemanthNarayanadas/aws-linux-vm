# aws-linux-vm
AWS Linux Virtual Machine Setup & Windows Access
📌 Project Title

Cross-Platform Access: Managing an AWS Linux Instance from Windows Environment

📖 Project Description

This project demonstrates how to:

Launch a Linux virtual machine (EC2 instance) in AWS
Configure security and key pairs
Connect to the Linux instance from a Windows OS
Manage the server remotely using SSH
Deploy a simple web server on the Linux instance

This project shows practical cloud computing and remote server management skills.

🛠️ Technologies Used
Amazon Web Services (AWS)
EC2 (Elastic Compute Cloud)
Linux (Amazon Linux / Ubuntu)
Windows OS
SSH
PuTTY / PowerShell
Apache HTTP Server
🏗️ Architecture Overview

Windows Machine (Local)
⬇ SSH Connection
AWS EC2 Linux Instance
⬇
Web Server (Apache)

📋 Steps Performed
1️⃣ Create EC2 Instance
Login to AWS Console
Go to EC2 Dashboard
Launch Instance
Select:
AMI: Amazon Linux 2 / Ubuntu
Instance Type: t2.micro (Free tier)
Create Key Pair (.pem file)
Configure Security Group:
Allow SSH (Port 22)
Allow HTTP (Port 80)
2️⃣ Connect from Windows
Option 1: Using PowerShell
ssh -i keyname.pem ec2-user@public-ip-address
Option 2: Using PuTTY
Convert .pem to .ppk using PuTTYgen
Open PuTTY
Enter Public IP
Connect using private key
3️⃣ Install Apache Web Server
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
4️⃣ Test Web Server

Open browser:

http://public-ip-address

Apache test page should load.

🔐 Security Configuration
SSH access restricted via security group
Key-based authentication used
Only required ports opened (22, 80)
📂 Repository Structure
aws-linux-vm/
│
├── README.md
├── screenshots/
│   ├── ec2-launch.png
│   ├── ssh-connection.png
│   ├── apache-running.png
│
└── commands.txt
