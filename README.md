
# Deploying a Simple Website on AWS EC2 (Ubuntu + Apache)

This project demonstrates how to deploy a simple HTML website on an AWS EC2 instance using Ubuntu and Apache web server. It is designed for beginners learning cloud computing and DevOps fundamentals.



## 🚀 Project Objectives
- Launch an EC2 instance on AWS  
- Install and configure Apache web server  
- Replace default Apache page with a custom HTML website  
- Test and verify public access  
- Document the process for DevOps learning  



## 🖥️ Technologies Used
- **AWS EC2**
- **Ubuntu Server 22.04**
- **Apache2 Web Server**
- **HTML**
- **SSH**



## 🧩 Step-by-Step Process

### 1. Launch EC2 Instance
- AMI: Ubuntu Server 22.04
- Instance type: t2.micro (free tier)
- Security group:
  - SSH (22) – My IP
  - HTTP (80) – Anywhere

### 2. Connect to EC2 via SSH

```bash
ssh -i ubuntu-key.pem ubuntu@PUBLIC_IP
```

### 3. Install Apache

```bash
sudo apt update -y
sudo apt install apache2 -y
sudo systemctl start apache2
sudo systemctl enable apache2
```

### 4. Replace Default Apache Webpage

```bash
cd /var/www/html
sudo rm index.html
sudo nano index.html
```

Paste your HTML code.

### 5. Restart Apache

```bash
sudo systemctl restart apache2
```

### 6. Test the Website
Visit:

```
http://PUBLIC_IP
```

You should see your custom webpage.

## 📸 Screenshots
Screenshots included in the `screenshots/` folder:
- EC2 instance running
- Apache installed successfully
- Custom website working


## 📚 Learning Outcome
Through this project, you will learn:
- Basic cloud deployment  
- Linux commands  
- Web server configuration  
- How to host static websites  
- How to document and publish cloud projects  



## 👩‍💻 Author
**Innocentia Azal**  
Cloud & DevOps Engineer in Training  
Cloud Career Kick Starter Program

