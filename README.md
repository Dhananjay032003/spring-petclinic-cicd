🚀 Spring PetClinic – End-to-End DevOps Automation Project

A production-style DevOps project that automates infrastructure provisioning, configuration management, and CI/CD deployment of a Spring Boot application on AWS using Terraform, Ansible, and AWS CodePipeline.

📌 Project Overview

This project uses the Spring PetClinic application as a real-world workload to demonstrate DevOps best practices.

The focus is on automation, repeatability, and zero manual deployment.

🎯 DevOps Objectives

Infrastructure as Code (IaC)

Configuration management

CI/CD automation

Cloud-based deployment

Production-style workflow


🏗️ Architecture
Developer
   |
   |  Git Push
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

🛠️ Tech Stack
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

Provisioned EC2 instances using Terraform

Managed SSH access, security groups, and networking

Installed Java and dependencies using Ansible

Deployed Spring Boot application automatically

CI/CD pipeline triggers on GitHub commits

No manual SSH or deployment steps

📂 Infrastructure & Configuration Details
🔹 Terraform

Creates EC2 instances

Manages key pairs and security groups

Outputs public IPs for Ansible inventory

🔹 Ansible

Connects to EC2 via SSH

Installs Java and required packages

Deploys and manages the Spring Boot application

🔄 CI/CD Pipeline Flow

Code pushed to GitHub

AWS CodePipeline is triggered automatically

AWS CodeBuild:

Pulls source code

Builds application using Maven

Executes Ansible deployment

Application is deployed to EC2
🌐 Application Access

After successful pipeline execution, access the application at:

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
Default (H2 – In-Memory)

Automatically initialized at startup

H2 Console:

http://<EC2_PUBLIC_IP>:8080/h2-console

MySQL (Optional)
docker run -e MYSQL_USER=petclinic \
-e MYSQL_PASSWORD=petclinic \
-e MYSQL_ROOT_PASSWORD=root \
-e MYSQL_DATABASE=petclinic \
-p 3306:3306 mysql:9.5


Activate profile:

spring.profiles.active=mysql

PostgreSQL (Optional)
docker run -e POSTGRES_USER=petclinic \
-e POSTGRES_PASSWORD=petclinic \
-e POSTGRES_DB=petclinic \
-p 5432:5432 postgres:18.1


Activate profile:

spring.profiles.active=postgres

🧪 Testing Strategy

Integration tests using H2

Database-specific tests for MySQL and PostgreSQL

Build validation through CI/CD pipeline



🧠 Challenges & Learnings

Troubleshot Ansible SSH and inventory issues

Resolved Java and dependency compatibility problems

Fixed IAM permission issues in AWS CodeBuild

Gained hands-on experience with CI/CD troubleshooting

Learned end-to-end DevOps workflow design



✅ DevOps Checklist

 Infrastructure as Code

 Configuration Management

 CI/CD Pipeline

 Automated Deployment

 Cloud Hosting

 Zero Manual Intervention

📌 Note on Base Application

The application workload is based on the Spring PetClinic sample project.
All DevOps automation, infrastructure, and CI/CD implementation are independently designed and implemented for this project.

Original source:

https://github.com/spring-projects/spring-petclinic

🤝 Contributing

Apache License 2.0

Issues and pull requests are welcome

Commits must include Signed-off-by (DCO)

📜 License

This project is licensed under the Apache License 2.0.

⭐ Final Note

This repository demonstrates production-style DevOps automation using real tools and real cloud workflows.
It is intended for learning, interviews, and hands-on DevOps practice.





<img width="1600" height="719" alt="image" src="https://github.com/user-attachments/assets/0a722fc9-9617-471b-9410-81b49c6e17f1" />

<img width="1600" height="762" alt="image" src="https://github.com/user-attachments/assets/69bab8f2-1eeb-49ce-b7f4-44a4784b97c7" />

<img width="1600" height="717" alt="image" src="https://github.com/user-attachments/assets/fc8442aa-7f6a-49a6-b77c-5e08a45743f4" />

<img width="1600" height="766" alt="image" src="https://github.com/user-attachments/assets/c082f125-420a-4b17-9b59-de708c36d102" />

<img width="1600" height="706" alt="image" src="https://github.com/user-attachments/assets/d6bfda54-d821-418e-a47e-09d1b3aad437" />

<img width="1600" height="651" alt="image" src="https://github.com/user-attachments/assets/2e24aa0a-0c1a-43a0-ab4d-d9a74f44eb3a" />

<img width="1600" height="518" alt="image" src="https://github.com/user-attachments/assets/34cde43b-e48c-4591-b22c-48d85d5a5454" />


<img width="1156" height="867" alt="image" src="https://github.com/user-attachments/assets/ae37a632-a6f9-46e4-a388-b3fc929fa95c" />
