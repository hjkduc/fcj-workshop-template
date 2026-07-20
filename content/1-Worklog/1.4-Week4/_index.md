---
title: "Week 4 Worklog"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:
* Master containerization with Docker and container orchestration using Amazon ECS and serverless AWS Fargate.
* Learn Kubernetes fundamentals via Amazon EKS, automated cluster bootstrapping with EKS Blueprints, and enterprise Red Hat OpenShift Service on AWS (ROSA).
* Implement automated CI/CD pipelines following DevOps best practices and orchestrate complex serverless microservices with AWS Step Functions.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | **Topic: Containerization with Docker & Orchestration with Amazon ECS & AWS Fargate**<br>- **Knowledge:**<br>  + Docker Fundamentals: Images, Containers, Dockerfile best practices, and Amazon Elastic Container Registry (ECR).<br>  + Amazon ECS Core Concepts: Clusters, Task Definitions, Tasks, and Services.<br>  + Compute Launch Types: EC2 Launch Type vs Serverless AWS Fargate engine.<br>- **Practice:**<br>  + Containerize a web application, push the Docker image to Amazon ECR.<br>  + Provision an Amazon ECS cluster and deploy the application using the serverless AWS Fargate launch type. | 11/05/2026 | 11/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Topic: CI/CD Pipeline for ECS with AWS CodePipeline & IaC for ECS using CDK**<br>- **Knowledge:**<br>  + AWS Developer Tools: AWS CodeCommit, CodeBuild, CodeDeploy, and CodePipeline.<br>  + Automated Container Delivery: Rolling updates, Blue/Green deployments for ECS.<br>  + High-Level CDK Constructs: `ApplicationLoadBalancedFargateService`.<br>- **Practice:**<br>  + Construct an automated CI/CD pipeline using AWS CodePipeline to build and deploy container updates to ECS on code commit.<br>  + Write a CDK script to programmatically deploy an ECS Fargate service behind an ALB. | 12/05/2026 | 12/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Topic: Getting Started with Amazon EKS (Kubernetes) & EKS Blueprints for CDK**<br>- **Knowledge:**<br>  + Kubernetes Architecture: Control Plane, Worker Nodes, Pods, Deployments, Services, and Ingress.<br>  + Amazon EKS Managed Kubernetes: Managed Node Groups, Fargate profiles, and `kubectl` CLI integration.<br>  + EKS Blueprints for CDK: Framework for bootstrapping production-ready EKS clusters.<br>- **Practice:**<br>  + Provision an Amazon EKS cluster using EKS Blueprints for CDK.<br>  + Deploy a sample multi-pod workload and expose it via a LoadBalancer Service using `kubectl`. | 13/05/2026 | 13/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Topic: CI/CD for EKS Applications & Red Hat OpenShift Service on AWS (ROSA)**<br>- **Knowledge:**<br>  + Kubernetes Deployment Strategies: GitOps principles (ArgoCD/Flux) vs AWS CodePipeline for EKS.<br>  + Red Hat OpenShift Service on AWS (ROSA): Managed enterprise OpenShift architecture, hybrid cloud integration, and security compliance.<br>- **Practice:**<br>  + Configure a continuous deployment pipeline for Kubernetes manifests targeting an EKS cluster.<br>  + Analyze ROSA cluster deployment topologies and enterprise migration scenarios. | 14/05/2026 | 14/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Topic: Hybrid Storage Gateway, Amazon FSx & Advanced Workflows with Step Functions**<br>- **Knowledge:**<br>  + AWS Storage Gateway: Volume Gateway, Tape Gateway, and S3 File Gateway for hybrid cloud storage.<br>  + Amazon FSx Family: FSx for Windows File Server, Lustre, NetApp ONTAP, and OpenZFS.<br>  + AWS Step Functions: State Machines, visual workflows, error handling, retries, and parallel execution.<br>- **Practice:**<br>  + Build an event-driven AWS Step Functions State Machine to orchestrate asynchronous microservices.<br>  + Evaluate Amazon FSx storage options for high-performance enterprise workloads. | 15/05/2026 | 15/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Week 4 Achievements:

#### Monday (11/05/2026):
* Mastered containerization workflows using Docker, writing optimized Dockerfiles, and managing repositories in Amazon ECR.
* Understood container orchestration abstractions in Amazon ECS (Clusters, Task Definitions, Services).
* Eliminated server provisioning and OS management overhead by deploying containerized workloads onto serverless AWS Fargate.

#### Tuesday (12/05/2026):
* Built a fully automated CI/CD pipeline using AWS CodePipeline to build Docker images and execute zero-downtime rolling updates on ECS.
* Programmatically provisioned load-balanced ECS Fargate infrastructure using high-level AWS CDK constructs.
* Understood Blue/Green deployment strategies using AWS CodeDeploy for mission-critical containerized applications.

#### Wednesday (13/05/2026):
* Acquired a solid understanding of Kubernetes core concepts (Control Plane, Nodes, Pods, Deployments, Services).
* Bootstrapped an Amazon EKS cluster effortlessly using EKS Blueprints for CDK.
* Interacted with EKS clusters using `kubectl` to deploy, manage, and expose containerized applications.

#### Thursday (14/05/2026):
* Explored automated deployment techniques for Kubernetes, comparing GitOps workflows with native CI/CD pipelines.
* Understood enterprise containerization advantages with Red Hat OpenShift Service on AWS (ROSA).
* Analyzed hybrid application deployment patterns for large-scale enterprise migrations.

#### Friday (15/05/2026):
* Evaluated hybrid storage integration strategies using AWS Storage Gateway and the Amazon FSx suite.
* Mastered serverless workflow orchestration using AWS Step Functions State Machines.
* Designed resilient visual workflows with built-in error handling, branching logic, and parallel state execution.