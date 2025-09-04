aws-load-balancer-project/
│
├── classic-load-balancer/
│   └── README.md
│
└── application-load-balancer/
    └── README.md


# AWS Classic Load Balancer Project

## 📌 Overview
This project demonstrates how to set up a **Classic Load Balancer (CLB)** with a single EC2 instance running Apache.

---

## 🔹 Steps

1. **Launch EC2 Instance**
   - Amazon Linux 2 AMI
   - Open port 80 in Security Group

2. **Install Apache**
   ```bash
   sudo yum update -y
   sudo yum install -y httpd
   sudo systemctl start httpd
   sudo systemctl enable httpd

echo "This is Classic Load Balancer" | sudo tee /var/www/html/index.html

Access CLB DNS name:

This is Classic Load Balancer
   


---

## 📝 application-load-balancer/README.md  

```markdown
# AWS Application Load Balancer Project

## 📌 Overview
This project demonstrates **Path-based routing** using Application Load Balancer (ALB) with two EC2 instances.

---

## 🔹 Steps

### Step 1: Launch Two EC2 Instances
- **Instance 1 (Green Page)**  
  ```bash
  sudo yum update -y
  sudo yum install -y httpd
  sudo systemctl start httpd
  sudo systemctl enable httpd
  echo "This is GREEN Page" | sudo tee /var/www/html/index.html

    sudo yum update -y
sudo yum install -y httpd
sudo systemctl start httpd
sudo systemctl enable httpd
echo "This is RED Page" | sudo tee /var/www/html/index.html

---
---
### Step 2: Configure Red Page Instance

- **Instance 2 (Red Page)**  
  ```bash
  sudo yum update -y
  sudo yum install -y httpd
  sudo systemctl start httpd
  sudo systemctl enable httpd
  echo "This is RED Page" | sudo tee /var/www/html/index.html


