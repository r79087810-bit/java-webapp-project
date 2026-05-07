🚀 DevOps CI/CD Pipeline using Jenkins Master–Slave Architecture
📌 Project Overview

This project demonstrates a complete CI/CD pipeline implementation using Jenkins Master–Slave architecture to automate the build, test, and deployment of a Java web application.

The system is designed to simulate a real-world DevOps workflow where code changes are automatically built and deployed to a Tomcat server using Jenkins.


🏗️ System Architecture
GitHub Repository
        │
        ▼
Jenkins Master (Job Orchestration)
        │
        ├───────────────┐
        ▼               ▼
Build Node        Deploy Node
(Maven Build)     (Tomcat Server)
        │               │
        └───────┬───────┘
                ▼
      Email Notifications


⚙️ Tech Stack
Jenkins (CI/CD Automation)
GitHub (Source Code Management)
Maven (Build Tool)
Java Web Application
Apache Tomcat (Deployment Server)
Linux (SSH-based Agent Setup)
Email Notification System


🔄 CI/CD Workflow
Developer pushes code to GitHub repository
Jenkins is triggered via GitHub Webhook / Poll SCM
Jenkins Master schedules the pipeline job
Build node pulls code and executes Maven build
WAR file is generated after successful build
Deployment node transfers WAR to Tomcat server
Application is deployed and hosted on Tomcat
Email notification is sent based on build status:
Success
Failure
Aborted



🖥️ Jenkins Architecture Setup
🔹 Master Node
Job scheduling
Pipeline execution control
Plugin management

🔹 Build Node (Slave 1)
Executes Maven build
Generates .war file
🔹 Deployment Node (Slave 2)
Hosts Apache Tomcat server
Deploys application

All nodes are connected using SSH-based Jenkins agents

🔔 Notification System

Email notifications are configured for:

✔ Build Success
❌ Build Failure
⚠ Deployment Failure
⛔ Build Aborted


🔗 CI/CD Triggers

This project supports two triggering mechanisms:

✅ GitHub Webhooks (Real-time automation)
✅ Poll SCM (Backup trigger method)



🎯 Key Learnings
Jenkins Master–Slave architecture setup
CI/CD pipeline design and implementation
GitHub webhook integration
Maven-based Java build automation
Application deployment on Tomcat server
Email notification configuration in Jenkins
Real-world DevOps workflow understanding

