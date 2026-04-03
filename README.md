# 🚀 Jenkins Setup on AWS EC2

This project demonstrates how to install and configure Jenkins on an Ubuntu EC2 instance for CI/CD automation.

## 📌 Tech Stack
- AWS EC2
- Ubuntu
- Jenkins
- GitHub

## 🏗️ Architecture

GitHub → Jenkins → EC2 Server

- Code is pushed to GitHub  
- Jenkins pulls code and builds  
- Deployment happens on EC2  

## ⚙️ Jenkins Installation Steps

### 1. Update System
```bash
sudo apt-get update


## Install Java
sudo apt-get install openjdk-11-jdk -y

## Install Jenkins
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee \
/usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update
sudo apt-get install jenkins -y


## Start Jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins

## Enable Firewall

sudo ufw allow 8080
sudo ufw enable
sudo ufw status

##  Access Jenkins

http://<EC2-PUBLIC-IP>:8080

##  Get Admin Password

sudo cat /var/lib/jenkins/secrets/initialAdminPassword

## 🚀 Future Enhancements

- Integrate with GitHub Webhooks  
- Create CI/CD pipelines  
- Deploy .NET application automatically  
- Add monitoring & alerts  

## 👨‍💻 Author

- Naveen Patil
- DevOps / Network Engineer
