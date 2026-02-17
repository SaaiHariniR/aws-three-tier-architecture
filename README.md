# AWS Three-Tier Architecture Deployment

## 📖 Project Overview
Designed and deployed a secure three-tier architecture on AWS using a custom VPC with public and private subnets. Implemented a Bastion Host for secure access to private EC2 instances and deployed a MariaDB RDS instance for the database tier.

---

## 🏗 Architecture Components

- Custom VPC (10.0.0.0/16)
- 1 Public Subnet
- 3 Private Subnets (Multi-AZ)
- Internet Gateway
- NAT Gateway with Elastic IP
- Bastion Host (EC2 - Amazon Linux 2)
- Web Server (EC2 - Apache)
- App Server (EC2 - MariaDB Client)
- RDS MariaDB (Private Subnet)
- Security Group referencing for tier communication

---

## 🔐 Security Implementation

- SSH access restricted to Bastion Host
- Private EC2 instances not publicly accessible
- Database accessible only from App Server security group
- NAT Gateway for controlled outbound internet access

---

## 🧪 Connectivity Tests

- Verified App Server to Web Server connectivity (ICMP test)
- Successfully connected App Server to RDS MariaDB
- Created and verified database `mydb`

---

## 🛠 Tools & Services Used

- AWS EC2
- AWS VPC
- Route Tables
- Internet Gateway
- NAT Gateway
- Elastic IP
- RDS (MariaDB)
- Amazon Linux 2

---

## 🎯 Key Learnings

- VPC networking and subnet design
- Security group referencing
- Private resource access via Bastion Host
- Database connectivity troubleshooting
- Real-world cloud infrastructure deployment

