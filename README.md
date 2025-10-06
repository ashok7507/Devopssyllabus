# ☁️ Cloud & DevOps Notes  

This repository contains detailed notes on **Cloud Computing**, **Linux**, **Networking**, **AWS Services**, and **DevOps Tools** — organized by days for easier learning and revision.

---

## 🗓️ DAY 1  

### 🌩️ Cloud Computing  
**Definition:**  
It is a method that provides on-demand services over the internet.  

**On-Demanded Services:**  
1. Storage  
2. Databases  
3. Infrastructure  
4. Networking  
5. Monitoring  
6. Security  

---

### ☁️ Types of Clouds  
1. Private  
2. Public  
3. Hybrid  

---

### 🧰 Cloud Providers  
1. AWS  
2. Azure  
3. GCP  

---

### ⚙️ AWS Services  
1. EC2  
2. IAM  
3. S3  
4. VPC  
5. Route53 / DNS  
6. RDS  
7. CloudWatch  
8. KMS  
9. SNS  

---

### 🛠️ DevOps Tools  
1. Git & GitHub  
2. Terraform  
3. Ansible  
4. Docker  
5. Kubernetes  
6. Jenkins (CI/CD)  

---

### 🐧 Linux Topics  
1. What is Linux?  
2. Architecture of Linux  
3. Basic Commands  
4. User & Group Management  
5. Permission Management  
6. Editors (Vim, Nano)  
7. File Management  

---

### 🌐 Networking  
1. OSI Model  
2. IP Address  
3. Types of IPs  
4. Classes of IP Address  
5. Subnetting  
6. Port Numbers & Protocols  
7. CIDR  

---

## 🗓️ DAY 3 – Linux Deep Dive  

### 🐧 What is Linux?  
Linux is an open-source, kernel-based operating system.  
**Kernel:** The intermediate layer between hardware and software that converts high-level code into machine-understandable binary (0s and 1s).  

**Architecture Layers:**  
- Application  
- Shell  
- Kernel  
- Hardware  

---

### 👥 Types of Users  
- Local User (e.g., ubuntu)  
- Root User (root)  
- Default User (nologin shell)  

---

### 💻 Basic Linux Commands  

| Command | Description |
|----------|-------------|
| ls | List files and directories |
| ls -a | Show hidden files |
| cd | Change directory |
| sudo -i | Switch to root user |
| mkdir | Create directory |
| rmdir | Remove empty directory |
| rm -rf | Remove non-empty folder |
| touch | Create file |
| rm filename | Delete file |
| cat | View file content |
| head / tail | View top or bottom lines of a file |
| cp | Copy files |
| mv | Move/Rename files |
| pwd | Show current directory |
| chmod | Change file permissions |
| df -h | Show disk usage |
| ping | Test network connectivity |
| curl / wget | Download files |
| ssh | Remote login |
| history | Show command history |
| whoami | Display current user |
| vim filename | Edit file using Vim |

---

### 👤 User & Group Management  

#### User Management
```bash
adduser username         # Create user with home directory  
useradd username         # Create user (no skeleton files)  
usermod -l new old       # Rename user  
usermod -aG group user   # Add user to group  
userdel username         # Delete user  
passwd username          # Set password

