---
title: "Week 1 Worklog"
date: 2026-04-20
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Week 1 Objectives:
* Master AWS foundational services including Compute (EC2, Lightsail), Storage (S3), Database (RDS), and Networking (VPC, Route 53).
* Learn to manage access security with IAM, system health with CloudWatch, and cost governance with AWS Budgets.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | **Topic: AWS Console, CLI Configuration & Access Management (IAM)**<br>- **Knowledge:**<br>  + Differentiate Authentication vs Authorization in AWS.<br>  + IAM Core Components: Users, Groups, Roles, and JSON-based IAM Policies (Principle of Least Privilege).<br>  + AWS CLI & Programmatic Access (Access Key ID & Secret Access Key).<br>- **Practice:**<br>  + Configure AWS CLI on local workstation (`aws configure`).<br>  + Create an IAM User, assign MFA security, and set up an IAM Group with specific policy access. | 20/04/2026 | 20/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Topic: Basic Networking with Amazon VPC & Compute with EC2 / Auto Scaling**<br>- **Knowledge:**<br>  + Amazon VPC architecture: Subnets (Public vs Private), Internet Gateway (IGW), Route Tables, Security Groups (Stateful) vs NACLs (Stateless).<br>  + Amazon EC2 fundamentals: Instance types, AMIs, Key Pairs, EBS storage.<br>  + High Availability concepts: Elastic Load Balancing (ELB) & Auto Scaling Groups (ASG).<br>- **Practice:**<br>  + Build a custom VPC with Public/Private subnets, IGW, and Route Tables.<br>  + Launch an EC2 instance in the public subnet and SSH into it via terminal. | 21/04/2026 | 21/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Topic: Storage with Amazon S3 & Relational Databases with Amazon RDS**<br>- **Knowledge:**<br>  + Amazon S3: Object storage, Buckets, Storage Classes, Bucket Policies, Static Website Hosting.<br>  + Amazon RDS: Managed relational databases (MySQL/PostgreSQL), Multi-AZ deployments, Automated Backups vs DB Snapshots.<br>- **Practice:**<br>  + Create an S3 Bucket, configure Bucket Policy for public read access, and host a static HTML website.<br>  + Provision an Amazon RDS MySQL database and connect to it from an EC2 instance. | 22/04/2026 | 22/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Topic: Simplifying Compute with Amazon Lightsail & System Monitoring with CloudWatch**<br>- **Knowledge:**<br>  + Amazon Lightsail: Simplified Virtual Private Server (VPS) solution for lightweight workloads.<br>  + Amazon CloudWatch: Metrics, CloudWatch Logs, Alarms, and Dashboards.<br>- **Practice:**<br>  + Deploy a WordPress instance on Amazon Lightsail with a Static IP.<br>  + Set up a CloudWatch Alarm monitoring EC2 CPU Utilization (>80%) with SNS email notifications. | 23/04/2026 | 23/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Topic: Hybrid DNS with Amazon Route 53 & Cost Management with AWS Budgets**<br>- **Knowledge:**<br>  + Amazon Route 53: Domain Name System (DNS), Public vs Private Hosted Zones, Routing Policies (Simple, Weighted, Failover).<br>  + AWS Cost Governance: AWS Budgets, Cost Allocation Tags, Billing Dashboard.<br>- **Practice:**<br>  + Create a Hosted Zone in Route 53 and map A/CNAME records to an S3/EC2 web endpoint.<br>  + Configure an AWS Budget with email alerts when forecasted costs exceed 80% of the threshold. | 24/04/2026 | 24/04/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Week 1 Achievements:

#### Monday (20/04/2026):
* Understood core identity management principles in AWS IAM (Users, Groups, Roles, Policies).
* Mastered security best practices by enabling Multi-Factor Authentication (MFA) for Root and IAM accounts.
* Installed and configured AWS CLI on the local machine using Access Keys for programmatic management.

#### Tuesday (21/04/2026):
* Acquired a deep understanding of cloud networking architecture in Amazon VPC (Subnets, IGW, Route Tables, Security Groups).
* Successfully created a custom VPC topology with isolated network layers.
* Provisioned Amazon EC2 instances, attached EBS volumes, and established SSH connectivity via Key Pairs.
* Understood how EC2 Auto Scaling and Elastic Load Balancing ensure application resilience.

#### Wednesday (22/04/2026):
* Mastered Amazon S3 object storage mechanics, bucket security policies, and lifecycle rules.
* Successfully deployed a static web application hosted on Amazon S3.
* Provisioned a managed relational database using Amazon RDS (MySQL) with Multi-AZ considerations.
* Configured Security Group rules to allow secure database access from application instances.

#### Thursday (23/04/2026):
* Learned the differences between Amazon EC2 and Amazon Lightsail for rapid application deployment.
* Successfully launched a full-stack WordPress site using Amazon Lightsail in minutes.
* Understood system observability with Amazon CloudWatch (Metrics, Logs, and Alarms).
* Configured automated CloudWatch Alarms and Amazon SNS email alerts to detect abnormal CPU utilization.

#### Friday (24/04/2026):
* Mastered DNS management with Amazon Route 53, hosted zones, and domain routing strategies.
* Mapped domain records (A/CNAME) to cloud endpoints in Route 53.
* Implemented financial guardrails by setting up cost alerts in AWS Budgets to prevent unexpected charges.