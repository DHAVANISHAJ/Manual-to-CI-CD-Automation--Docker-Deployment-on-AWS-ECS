Manual to CI/CD Automation: Docker Deployment on AWS ECS
📌 Project Overview

This project demonstrates the end-to-end deployment of Dockerized applications on AWS ECS, starting from a manual infrastructure setup and evolving into a fully automated CI/CD pipeline. The goal is to showcase real-world DevOps practices by first validating the architecture manually and then automating the complete build and deployment process using AWS-native services.

The project highlights how containerized applications can be reliably built, pushed, and deployed with minimal manual intervention while ensuring scalability, high availability, and zero-downtime deployments.

Presentation Link

https://drive.google.com/file/d/19nRvvg_PSg9rkziqLl4KBDoqDe4_SpiV/view?usp=sharing


🎯 Objectives

Understand and validate container deployment on AWS ECS

Implement Docker image lifecycle management using Amazon ECR

Automate build and deployment using CI/CD principles

Demonstrate zero-downtime deployment using ECS services and ALB

Follow DevOps best practices for cloud-native applications

🏗️ Architecture

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/a0094f09-d568-4e5e-a589-a07591c33fb6" />




🔹 Phase 1: Manual Setup & Validation (Foundation Layer)

Purpose:
To understand, validate, and de-risk the architecture before automation.

Key Activities:

Created a custom VPC with public subnets and routing

Launched EC2 instances and installed Docker

Built Docker images locally for two applications

Created Amazon ECR repositories and pushed images

Created ECS task definitions and services (EC2 launch type)

Configured Application Load Balancer and target groups

Tested applications using EC2 public IP and ALB DNS

Outcome:
A fully working container deployment with clear understanding of networking, security groups, ECS behavior, and load balancing.

🔹 Phase 2: Fully Automated CI/CD Deployment (Production Layer)

Purpose:
To eliminate manual deployment steps and enable repeatable, reliable releases.

Automation Stack:

Source Control: GitHub / AWS CodeCommit

CI/CD Orchestration: AWS CodePipeline

Build & Image Push: AWS CodeBuild

Container Registry: Amazon ECR

Container Orchestration: Amazon ECS (Fargate)

Traffic Management: Application Load Balancer

Automation Flow:

Code push triggers CodePipeline automatically

CodeBuild builds Docker images using buildspec.yml

Images are pushed to Amazon ECR

ECS service updates tasks automatically

ALB routes traffic to healthy tasks

Old tasks move to draining state during deployment

Outcome:
A fully automated CI/CD pipeline with zero server management and seamless deployments.

🏁 Conclusion

This project successfully demonstrates how manual container deployments can be transformed into a fully automated CI/CD-driven workflow on AWS ECS. It reflects real-world DevOps practices and provides hands-on experience in designing, deploying, and automating cloud-native applications.
