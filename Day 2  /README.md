🔐 SSH (Secure Shell) – Complete Documentation
📌 Overview

SSH (Secure Shell) is a secure network protocol used to remotely access and manage systems over an encrypted connection. It replaces insecure protocols like Telnet and is widely used in DevOps, cloud computing, and system administration.

🧱 Architecture
Client Machine  ───── Encrypted Connection ─────  Remote Server
(SSH Client)                                  (SSH Daemon - sshd)


SSH Client → Initiates connection

SSH Server → Accepts connections

Port → Default TCP 22

Encryption → Ensures secure communication

⚙️ Installation (Ubuntu Server)
Update packages
sudo apt update

Install SSH server
sudo apt install openssh-server -y

Check SSH status
sudo systemctl status ssh

Enable SSH at boot
sudo systemctl enable ssh

🔑 Basic SSH Connection
ssh username@ip_address


Example:

ssh kongu@192.168.236.130

🔐 Authentication Methods
1. Password Authentication

User logs in using system password.

2. SSH Key Authentication (Recommended)

Generate key:

ssh-keygen


Copy key to server:

ssh-copy-id username@ip_address


Login without password:

ssh username@ip_address

📁 File Transfer using SSH
SCP (Secure Copy)
scp file.txt username@ip:~/destination

SFTP
sftp username@ip

🌐 SSH Port Forwarding

Local forwarding:

ssh -L 8080:localhost:3000 username@server_ip


Access service:

http://localhost:8080

⚙️ SSH Configuration File

Location:

~/.ssh/config


Example:

Host myserver
    HostName 192.168.236.130
    User kongu
    Port 22


Connect using:

ssh myserver

🛠️ SSH in DevOps

Common uses:

Remote server management

Docker deployment

Git operations

CI/CD pipelines

Cloud infrastructure access

Tools using SSH:

Git

VS Code Remote SSH

Jenkins

Ansible

Terraform

🔒 Security Best Practices

Disable root login

Use SSH keys instead of passwords

Change default port

Enable firewall

Use fail2ban

Edit config:

sudo nano /etc/ssh/sshd_config


Set:

PermitRootLogin no
PasswordAuthentication no


Restart SSH:

sudo systemctl restart ssh

❗ Common Errors & Fixes
Connection refused

SSH service not running

Permission denied

Wrong username/password

Key not configured

Connection timed out

Firewall blocking port 22

Network issue

🧠 How SSH Works

Client initiates connection

Server shares public key

Encryption channel established

Authentication occurs

Secure session created

💻 SSH + VS Code Workflow
VS Code → SSH → Ubuntu Server → Remote Development Environment


Allows editing Linux files directly from Windows.

🚀 Real-World Applications

Remote server access

Deploying Docker containers

Managing cloud instances

Secure file transfer

Remote coding environments

📚 Conclusion

SSH is a foundational technology for secure remote access, system administration, and DevOps workflows. Understanding SSH enables efficient server management, automation, and secure communication across distributed systems.
