<h1 align="center">
🚀 SPRING PETCLINIC — END-TO-END DEVOPS AUTOMATION PROJECT 🚀
</h1>

<p align="center">
<b>Terraform • Ansible • AWS • CI/CD • Infrastructure as Code</b>
</p>

<p align="center">
Production-style automation of infrastructure provisioning, configuration management, 
and CI/CD deployment for a Spring Boot application on AWS
</p>

<p align="center">
<img src="https://img.shields.io/badge/AWS-EC2-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Terraform-IaC-purple?style=for-the-badge" />
<img src="https://img.shields.io/badge/Ansible-Config-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/CI%2FCD-Automated-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Spring%20Boot-Java-green?style=for-the-badge" />
</p>

<hr/>

📌 Project Overview

This is a production-style DevOps project built around the Spring PetClinic application to demonstrate real-world DevOps practices.

The emphasis is on automation, repeatability, scalability, and zero manual deployment — not just running an application.

🎯 DevOps Objectives

✔ Infrastructure as Code (IaC)
✔ Configuration Management
✔ CI/CD Pipeline Automation
✔ Cloud-Based Deployment
✔ Production-Ready Workflow


🏗️ Architecture Overview

Developer
   |
   | Git Push
   v
GitHub Repository
   |
   v
AWS CodePipeline
   |
   v
AWS CodeBuild
   |
   v
Ansible (Configuration & Deployment)
   |
   v
EC2 Instances (Terraform Provisioned)
   |
   v
Spring Boot Application (PetClinic)


🛠️ Technology Stack

| Layer                    | Tools                           |
| ------------------------ | ------------------------------- |
| Cloud Provider           | AWS                             |
| Compute                  | EC2                             |
| Infrastructure as Code   | Terraform                       |
| Configuration Management | Ansible                         |
| CI/CD                    | AWS CodePipeline, AWS CodeBuild |
| Application              | Spring Boot                     |
| Build Tool               | Maven                           |
| Java Version             | Java 17                         |
| Database                 | H2 (default), MySQL, PostgreSQL |
| OS                       | Amazon Linux                    |


🤖 Automation Highlights

Provisioned EC2 infrastructure using Terraform

Managed SSH access, security groups, and networking

Installed Java and system dependencies via Ansible

Deployed Spring Boot application automatically

CI/CD pipeline triggers on every GitHub commit

Zero manual SSH or deployment steps


📂 Infrastructure & Configuration Details

🔹 Terraform Responsibilities

EC2 instance creation

Key pair and security group management

Output generation for Ansible inventory


🔹 Ansible Responsibilities

SSH-based configuration management

Java and dependency installation

Application deployment and service management


🔄 CI/CD Pipeline Flow

Developer pushes code to GitHub

AWS CodePipeline triggers automatically

AWS CodeBuild:

Pulls source code

Builds application using Maven

Executes Ansible playbooks

Application deployed to EC2 instances


🌐 Application Access

After a successful pipeline execution, the application is available at:

http://<EC2_PUBLIC_IP>:8080


▶️ Run Application Locally (Optional)
Prerequisites

Java 17+

Git

Maven or Gradle

Clone Repository
git clone https://github.com/spring-projects/spring-petclinic.git
cd spring-petclinic

Run with Maven
./mvnw spring-boot:run

Run with Gradle
./gradlew bootRun

🗄️ Database Configuration
🔹 Default (H2 – In-Memory)

Auto-initialized at startup

Console:

http://<EC2_PUBLIC_IP>:8080/h2-console

🔹 MySQL (Optional)
docker run -e MYSQL_USER=petclinic \
-e MYSQL_PASSWORD=petclinic \
-e MYSQL_ROOT_PASSWORD=root \
-e MYSQL_DATABASE=petclinic \
-p 3306:3306 mysql:9.5


Activate:

spring.profiles.active=mysql

🔹 PostgreSQL (Optional)
docker run -e POSTGRES_USER=petclinic \
-e POSTGRES_PASSWORD=petclinic \
-e POSTGRES_DB=petclinic \
-p 5432:5432 postgres:18.1


Activate:

spring.profiles.active=postgres

🧪 Testing Strategy

Integration tests using H2

Database-specific tests for MySQL and PostgreSQL

CI/CD pipeline enforces build validation

🧠 Challenges & Learnings

Resolved Ansible SSH and inventory issues

Fixed Java and dependency compatibility problems

Debugged IAM permission issues in AWS CodeBuild

Learned end-to-end CI/CD troubleshooting

Gained hands-on cloud DevOps experience

✅ DevOps Checklist

 Infrastructure as Code

 Configuration Management

 CI/CD Pipeline

 Automated Deployment

 Cloud Hosting

 Zero Manual Intervention

📌 Note on Base Application

The application workload is based on the Spring PetClinic sample project.
All DevOps automation, infrastructure, and CI/CD workflows are independently designed and implemented.

Original Source:

https://github.com/spring-projects/spring-petclinic

🤝 Contributing

Licensed under Apache License 2.0

Issues and pull requests welcome

Commits must include Signed-off-by (DCO)

📜 License

This project is licensed under the Apache License 2.0.

⭐ Final Note

This repository represents a real-world DevOps automation workflow using industry tools and cloud infrastructure.
Designed for learning, interviews, and professional DevOps portfolios.


<img width="1600" height="719" alt="image" src="https://github.com/user-attachments/assets/42acaf25-93ae-45b5-9c9f-22366a6bbf32" />
<img width="1600" height="762" alt="image" src="https://github.com/user-attachments/assets/a7788289-ed15-4656-b84f-b4473da09f25" />
<img width="1600" height="717" alt="image" src="https://github.com/user-attachments/assets/cbbc99e9-8b99-4e71-bee4-f52f3ec0d867" />
<img width="1600" height="706" alt="image" src="https://github.com/user-attachments/assets/29586335-20a1-4198-be3d-dea58cf86d01" />
<img width="1600" height="766" alt="image" src="https://github.com/user-attachments/assets/95f19ff3-551e-417b-861e-a18fc31a9b07" />
<img width="1600" height="651" alt="image" src="https://github.com/user-attachments/assets/c4aff999-4026-4e74-845c-7b180b568b30" />
<img width="1600" height="518" alt="image" src="https://github.com/user-attachments/assets/f0f2db33-6c7f-424e-8fea-b7c32fff9508" />

