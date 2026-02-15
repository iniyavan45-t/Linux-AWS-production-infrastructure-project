# Production-Grade Auto-Scaling Web Application (Linux + AWS)

## Overview
This project documents the design and implementation of a production-grade, highly available web application deployed on AWS using Linux-based servers. The architecture is designed to automatically scale based on traffic and provide monitoring and alerting.

This repository focuses on **project documentation and workflow**, created from hands-on implementation.

---

## Architecture
Users → Application Load Balancer → Auto Scaling Group (Ubuntu EC2) → (Optional) RDS  
Monitoring & Alerts → Amazon CloudWatch and SNS

---

## Technologies Used
- AWS EC2
- Application Load Balancer (ALB)
- Auto Scaling Group (ASG)
- Amazon CloudWatch
- Amazon SNS
- Amazon IAM
- Amazon VPC
- Linux (Ubuntu)
- Nginx
- UFW Firewall

---

## Key Implementation Steps
- Created IAM role for secure EC2 access to AWS services
- Launched and configured Ubuntu EC2 instances
- Performed Linux hardening (non-root user, SSH hardening, firewall)
- Installed and configured Nginx web server
- Created a custom AMI for scaling
- Configured Launch Template and Auto Scaling Group
- Deployed Application Load Balancer with health checks
- Implemented CloudWatch monitoring and SNS email alerts
- Tested auto-scaling behavior using load generation

---

## Monitoring & Alerts
- CloudWatch metrics for CPU utilization
- Auto Scaling policies based on CPU thresholds
- SNS email alerts triggered when CPU usage exceeds defined limits

---

## Optional Enhancements
- Amazon RDS (MySQL) for centralized persistent storage
- Amazon S3 for storing application and Nginx logs

---

## Documentation
Detailed step-by-step implementation notes are available in the `docs/` folder.

---

## Note
This repository is intended for **documentation and learning purposes**.  
The infrastructure was implemented during hands-on practice; full automation scripts and live infrastructure are not maintained here.

---

## Interview Summary
“I deployed a production-grade Ubuntu Linux web application on AWS using ALB and Auto Scaling. I hardened Linux servers, enabled monitoring and alerts using CloudWatch and SNS, and validated real-time scaling behavior under load.”
