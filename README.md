# AWS DevOps CI/CD Project

## Project Overview

This project demonstrates a production-style DevOps deployment on AWS using Amazon EC2, Docker, Jenkins, Amazon S3, and Amazon CloudWatch. The application is automatically built and deployed through a Jenkins CI/CD pipeline whenever changes are pushed to GitHub.

---

## Architecture

```
                    GitHub
                       │
                 Source Code
                       │
                       ▼
                  Jenkins Server
                 (CI/CD Pipeline)
                       │
          Build Docker Image & Deploy
                       │
                       ▼
               Amazon EC2 Instance
          ┌─────────────────────────┐
          │      Docker Container   │
          │     Flask Application   │
          └─────────────────────────┘
                │             │
                │             │
                ▼             ▼
          Amazon S3      Amazon CloudWatch
           (Backups)   (Monitoring & Alarms)
```

---

## Technologies Used

* AWS EC2
* AWS IAM
* Amazon S3
* Amazon CloudWatch
* Jenkins
* Git & GitHub
* Docker
* Python
* Flask
* Linux (Amazon Linux 2023)

---

## Project Workflow

1. Developer pushes code to GitHub.
2. Jenkins pulls the latest source code.
3. Jenkins builds the Docker image.
4. Docker container is deployed on the EC2 instance.
5. Application becomes available to users.
6. Project backups are stored in Amazon S3.
7. CloudWatch monitors CPU, memory, disk, and network usage.
8. CloudWatch alarms notify when thresholds are exceeded.

---

## Features

* Automated CI/CD using Jenkins
* Dockerized Flask application
* Automated deployment on Amazon EC2
* Amazon S3 backup solution
* CloudWatch monitoring and dashboards
* CloudWatch alarms for system monitoring
* Secure AWS IAM configuration
* Security Group and firewall configuration

---

## Project Structure

```
.
├── app.py
├── requirements.txt
├── Dockerfile
├── Jenkinsfile
├── backup/
└── README.md
```

---

## Deployment Steps

1. Launch an Amazon EC2 instance.
2. Install Docker and Jenkins.
3. Clone the GitHub repository.
4. Configure the Jenkins pipeline.
5. Build and deploy the Docker container.
6. Verify the application.
7. Upload backups to Amazon S3.
8. Install and configure the CloudWatch Agent.
9. Create CloudWatch dashboards and alarms.

---

## Monitoring

Amazon CloudWatch is used to monitor:

* CPU Utilization
* Memory Usage
* Disk Usage
* Network Traffic

CloudWatch dashboards provide real-time visibility into server performance, while alarms notify when configured thresholds are exceeded.

---

## Backup Strategy

Project backups are stored in Amazon S3 to provide a secure and reliable backup solution.

---

## Screenshots

Include screenshots of:

* EC2 Instance
* 
* Jenkins Pipeline Success
* Running Flask Application
* Docker Container
* Amazon S3 Bucket
* CloudWatch Dashboard
* CloudWatch Alarm

---

## Future Enhancements

* HTTPS using SSL/TLS
* Infrastructure as Code with Terraform
* Kubernetes deployment (Amazon EKS)
* Automated testing in the CI/CD pipeline
* Centralized log management
* Blue/Green deployment strategy

---

## Author

**Ravindranadh Sharma**

AWS | DevOps | Docker | Jenkins | Cloud Computing
