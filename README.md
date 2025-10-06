# ☁️ CLOUD & DEVOPS FULL NOTES
**Author:** Shree Farmer  
**Topics Covered:** Cloud Computing • AWS • Linux • Networking • DevOps • CI/CD • Containers

---

# 🗓️ DAY 1

## ☁️ Cloud Computing
It is a one type of method that is provide ondemanded services over the internet.

### 💡 On-Demanded Services:
1. Storage
2. Databases
3. Infrastructure
4. Networking
5. Monitoring
6. Security

---

## ☁️ Types of Clouds:
1. Private
2. Public
3. Hybrid

---

## 🌐 Types of Cloud Providers:
1. AWS
2. Azure
3. GCP

---

## 🧩 AWS Services:
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

## ⚙️ DevOps Tools:
1. Git & GitHub
2. Terraform
3. Ansible
4. Docker
5. Kubernetes
6. Jenkins (CI/CD)

---

# 🐧 LINUX

## 🧠 What is Linux?
Linux is nothing but it is an open source kernel-based operating system.

---

## 🧱 Architecture of Linux:
```
Application
Shell
Kernel
Hardware
```

---

## 🧑‍💻 Types of Users
- Local User (e.g., ubuntu)
- Root User (root)
- Default User (nologin shell)

---

## 💻 Basic Commands of Linux:
| Command | Description |
|----------|-------------|
| ls | Lists files and directories |
| ls -a | Show hidden files and folders |
| cd | Change directory |
| sudo -i | Switch to root user (super user do) |
| ctrl+d | Return to local user |
| mkdir | Create a new directory |
| rmdir | Remove an empty directory |
| rm -rvf foldername | Remove non-empty folder forcefully |
| touch | Create a new file |
| rm filename | Remove a particular file |
| head | Show first 10 lines (head -20 for 20 lines) |
| tail | Show last 10 lines (tail -13 for 13 lines) |
| cp | Copy files or directories |
| mv | Move or rename files or directories |
| pwd | Print current working directory |
| cat | Display file contents |
| ll | Long listing to check directory details and permissions |
| chmod | Change file/directory permissions |
| df -h | Show disk space usage (human readable) |
| ping | Test network connectivity |
| curl -O | Download URL from internet |
| wget | Download file from internet |
| ssh | Securely connect to a remote server |
| history | Show command history |
| clear | Clear terminal (ctrl+l) |
| whoami | Display current username |
| vim filename | Open file in Vim editor |
| find -name filename | Find a file by name |
| sudo apt-get update | Update system packages |
| sudo apt-get upgrade | Upgrade system packages |
| sudo apt-get install packagename | Install a package |
| sudo apt-get remove packagename | Remove a package |

---

# 👥 USER & GROUP MANAGEMENT

## 🧑‍💻 User Management Commands

### ➕ Create Users
```bash
useradd username        # Creates a new user account (skeleton file will not be created)
adduser username        # Creates a user with skeleton file
```

### 🧩 Modify Users
```bash
usermod -l new-name current-name   # Rename a user
usermod -aG groupname username     # Add user to a group (append)
```

### ❌ Delete Users
```bash
userdel username   # Deletes an existing user
```

### 🔐 Password Management
```bash
passwd username    # Sets or changes a user’s password
```

---

## 👥 Group Management Commands

### ➕ Create Group
```bash
groupadd groupname
```

### ✏️ Modify Group
```bash
groupmod -n newgroup oldgroup   # Rename group
```

### ❌ Delete Group
```bash
groupdel groupname
```

### 👥 Manage Group Membership
```bash
gpasswd -a username groupname   # Add user into group
gpasswd -d username groupname   # Remove user from group
```

---

## 🔐 PERMISSION MANAGEMENT

| Symbol | Value | Description |
|---------|--------|-------------|
| r | 4 | Read |
| w | 2 | Write |
| x | 1 | Execute |

🧱 **Structure:**  
`rwxrwxrwx = owner, group of file, other users`

### 🔧 Examples:
```bash
ll                            # Check file/folder permissions
chmod u+r filename            # Add read permission to owner
chmod g-r filename            # Remove read from group
chmod o=x filename            # Give execute permission to others
chown user filename           # Change owner of file
chown user:group filename     # Change owner and group of file
```

---

## ✍️ EDITOR (VIM)

### 🧭 Basic Commands
```bash
vim filename          # Open or create file
vim +n filename       # Open file at line n
vim + filename        # Open file at last line
```

### 🎮 Modes in Vim

| Mode | How to Enter | Purpose |
|------|---------------|----------|
| Normal | ESC | Default mode |
| Insert | i | Insert text |
| Visual | v | Select text |
| Command | : | Save/Quit/Settings |

---

### ⚙️ NORMAL MODE ACTIONS

| Action | Key |
|---------|-----|
| Move Cursor | `h` (left), `l` (right), `j` (down), `k` (up) |
| Delete a Line | `dd` |
| Copy a Line | `yy` |
| Paste | `p` |
| Undo | `u` |
| Redo | `Ctrl + r` |
| Cut | `cc` |

---

### ⚡ COMMAND MODE

| Command | Description |
|----------|-------------|
| :w | Save |
| :q | Quit |
| :wq | Save and Quit |
| :q! | Quit without saving |
| :set nu | Show line numbers |
| :set nonu | Hide line numbers |
| :help | Open Vim help |

---

# 🌐 NETWORKING

## 📶 OSI Model

| Layer | Name | Function | Example |
|--------|------|-----------|----------|
| 7 | Application | Interface between user and network | HTTP, FTP, DNS |
| 6 | Presentation | Data formatting, encryption | SSL, TLS |
| 5 | Session | Manages connections | RPC, NetBIOS |
| 4 | Transport | Reliable data transfer | TCP, UDP |
| 3 | Network | Routing, IP addressing | IP, ICMP |
| 2 | Data Link | MAC addressing | Ethernet, VLAN |
| 1 | Physical | Transmission | Cables, Wi-Fi |

---

## 🌍 IP Addressing

| Type | Description | Example |
|------|--------------|----------|
| Public IP | Visible on Internet | 203.0.113.12 |
| Private IP | Local network only | 192.168.0.10 |
| Static IP | Fixed | Servers |
| Dynamic IP | Changes periodically | DHCP users |

---

## 🔢 IP Classes

| Class | Range | Usage |
|--------|--------|-------|
| A | 1.0.0.0 – 126.255.255.255 | Large networks |
| B | 128.0.0.0 – 191.255.255.255 | Medium networks |
| C | 192.0.0.0 – 223.255.255.255 | Small networks |
| D | 224.0.0.0 – 239.255.255.255 | Multicasting |
| E | 240.0.0.0 – 255.255.255.255 | Research |

---

## 🌐 Port Numbers

| Service | Port |
|----------|------|
| SSH | 22 |
| HTTP | 80 |
| HTTPS | 443 |
| DNS | 53 |
| FTP | 21 |
| Jenkins | 8080 |
| MySQL | 3306 |
| Grafana | 3000 |
| Kubernetes API | 6443 |

---

# ☁️ AWS SERVICES OVERVIEW

## 💻 EC2 (Elastic Compute Cloud)
- Used to create virtual servers in AWS cloud
- Supports scaling, snapshots, load balancers, and auto-scaling

### Commands
```bash
aws ec2 describe-instances
aws ec2 start-instances --instance-ids <id>
aws ec2 stop-instances --instance-ids <id>
```

## 👤 IAM (Identity and Access Management)
- Used for user, group, and role management
- Manage policies and permissions
- Supports MFA for security

## 🪣 S3 (Simple Storage Service)
- Object-based storage system
- Stores data as key-value

# 🏠 VPC (Virtual Private Cloud)

### Components:
- VPC: Virtual network in AWS
- Subnet: Subdivision of VPC
- NAT Gateway: Enables private subnet instances to access internet
- Internet Gateway: Connects VPC to internet
- Route Table: Directs traffic in VPC
- DHCP: Assigns IP addresses dynamically
- Peering Connection: Connects two VPCs privately

### Security:
- SG (Security Group) vs NACL (Network ACL)
  - SG: Stateful firewall, instance level
  - NACL: Stateless firewall, subnet level

### Other Concepts:
- Transit Gateway: Connects multiple VPCs centrally
- VPN: Secure connection to VPC
- How to create a VPC: Use AWS console or CLI

---

# 🗄️ RDS (Relational Database Service)

Features: High availability, fault tolerance, disaster recovery, scaling, patching

### Tasks:
1. Steps to create RDS database
2. Multi-AZ deployment
3. Proxy server setup
4. Read replicas
5. Connect RDS to EC2 (client, username, password, port 3306)
6. Create snapshot
7. Copy snapshot & replicate to another region

---

# 📊 CloudWatch

### Dashboards:
- Automatic dashboards
- Custom dashboards creation

### Metrics:
- CPU utilization, Network in/out, Disk read/write
- Namespace: Organizes metrics in CloudWatch
- Enable detailed monitoring on EC2

### Alarms:
- Create alarms on metrics (average, OK, insufficient data)
- Composite alarms
- Billing alarms
- Use cases for composite alarms

---

# 🔑 KMS (Key Management Service)

- Encrypt data in AWS
- SSE (Server-Side Encryption) & CSE (Client-Side Encryption)
- Manages CMKs (Customer Master Keys)
- Data keys: plaintext & encrypted
- Encrypted data = ciphertext

---

# ☁️ Cloud Computing Concepts: IaaS, PaaS, SaaS

### 9 Components of an Application Stack
1. Physical Servers
2. Storage
3. Networking
4. Virtualization
5. Operating System (OS)
6. Middleware (e.g., .NET, Java runtime)
7. Runtime Environment (e.g., Node.js, Python)
8. Application
9. Data

| Component        | IaaS     | PaaS     | SaaS     |
| ---------------- | -------- | -------- | -------- |
| Physical Servers | Provider | Provider | Provider |
| Storage          | Provider | Provider | Provider |
| Networking       | Provider | Provider | Provider |
| Virtualization   | Provider | Provider | Provider |
| Operating System | You      | Provider | Provider |
| Middleware       | You      | Provider | Provider |
| Runtime          | You      | Provider | Provider |
| Application      | You      | You      | Provider |
| Data             | You      | You      | Provider |

---

# 🛠️ DevOps Tools

### Git & GitHub
- Git: Version control system
- GitHub: Online repository hosting

#### Commands:
```bash
# Configuration
git config --global user.name "username"
git config --global user.email "email"
git config --list

# Clone repo
git clone <repo-url>

# Add & commit
git add .
git commit -m "message"

# Branch management
git branch
git branch -M main
git checkout -b branchname
git branch -d branchname

# Push & fetch
git remote add origin <repo-url>
git push origin branchname
git fetch origin main

# Merge & pull request
git merge branchname
git pull origin branchname
```

### CI/CD Tools
- Terraform: Infrastructure as code
- Ansible: Automate configuration
- Docker: Package apps into containers
- Kubernetes: Orchestrate containers
- Jenkins: Automate build, test, deployment

### AWS CLI Commands
```bash
aws ec2 start-instances --instance-ids <id>
aws ec2 stop-instances --instance-ids <id>
aws ec2 create-image --instance-id <id> --name "MyNewAMI" --description "AMI created from instance X"
aws ec2 allocate-address --domain vpc
aws ec2 describe-volumes
aws ec2 describe-instances --query "Reservations[*].Instances[*].[InstanceId, Tags[?Key=='Name'].Value | [0]]" --output text
```

### SCP Command Example
```bash
scp -i "jon.pem" ubuntu@54.159.199.19:/home/ubuntu/AndroRAT/rat.apk C:\Users\Sumeet\Desktop
```

---

# 🛡️ Transit Gateway

1. Connect all VPCs in one region
2. Create 3 VPCs & subnets
3. Create transit gateway & attachments
4. Edit routes of each VPC
5. Test connectivity (ping)

---

# 🛠️ DevOps - Git & GitHub

Git is a version control system (VCS) used for tracking changes in code.
GitHub is an online platform to host Git repositories.

## Key Features
- Free and open source
- Tracks history of code changes
- Facilitates collaboration

## Workflow

### 1) Create Repositories
```bash
# On GitHub website: Create a new repository
```

### 2) Git Configuration Commands
```bash
git config --global user.name "username"
git config --global user.email "email@example.com"
git config --list
```

### 3) Download Repos to Local Server
```bash
git clone <repository-url>  # Clone remote repo to local
```

### 4) Add & Commit Changes
```bash
git add .                    # Stage changes

git commit -m "updated branch"  # Commit changes
```

### 5) Remote Management
```bash
git remote add origin <branchname> <URL-of-repo>  # Add remote

git remote remove origin <branchname>              # Remove remote

git push origin <branchname>                       # Push changes to remote
```

### 6) Check Status
```bash
git status  # Shows file status
# Status types:
# untracked  -> new file
# modified   -> file changed
# staged     -> ready for commit
# unmodified -> unchanged
```

### 7) Branch Management
```bash
git branch                  # List branches
git branch -M main          # Rename branch
git checkout -b branchname  # Create new branch and switch
git branch branchname       # Create new branch without switching
git branch -d branchname    # Delete branch
git checkout branchname     # Switch branch
```

### 8) Merge Branches
```bash
# Merge using pull request or locally:
git commit -m "merging perform"
git merge <branchname>
```

### 9) Pull Requests
```bash
create file on github
commit changes
git pull # Fetch and merge changes from remote
```

### 10) Fetch Updates
```bash
git fetch origin          # Fetch changes only, no merge
git branch -r             # List remote branches
git fetch origin main     # Fetch main branch updates
```

### 11) Push vs Fetch
- `git push`: Upload local changes to remote repo
- `git fetch`: Update remote tracking branches without changing local code
 ```bash

 ```

### 12) Show Commits
```bash
git log  # Show all branches commit 
git log <branchname>  # Show commit history
git show <commitId>  #Show a perticular commit 
```

### 13) Forking
- Fork allows you to create your own copy of a repository on GitHub to experiment or contribute back.
