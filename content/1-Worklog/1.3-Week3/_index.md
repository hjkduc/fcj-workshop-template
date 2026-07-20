---
title: "Week 3 Worklog"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:
* Automate operational workflows using event-driven serverless computing (AWS Lambda) and AWS Systems Manager (SSM).
* Master Infrastructure as Code (IaC) using AWS CloudFormation and the AWS Cloud Development Kit (CDK).
* Enhance observability, automate data lifecycle management, and perform advanced cloud cost analytics (FinOps) using Amazon Athena and AWS Glue.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | **Topic: Serverless Automation with AWS Lambda & Secure Access via Systems Manager**<br>- **Knowledge:**<br>  + AWS Lambda: Execution model, triggers, IAM execution roles, environment variables, stateless nature.<br>  + AWS Systems Manager (SSM): Session Manager (bastionless SSH/RDP), Parameter Store (secure configuration management), Run Command, and Patch Manager.<br>- **Practice:**<br>  + Build an event-driven AWS Lambda function triggered by Amazon S3 upload events.<br>  + Securely access a private EC2 instance using SSM Session Manager without opening inbound port 22. | 04/05/2026 | 04/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Topic: Advanced CloudWatch & Grafana Monitoring & IaC with AWS CloudFormation**<br>- **Knowledge:**<br>  + Advanced CloudWatch: Custom metrics, CloudWatch Logs Insights, Amazon Managed Grafana workspace integration.<br>  + AWS CloudFormation: Declarative templates (YAML/JSON), Stacks, Parameters, Mappings, Resources, Outputs, Stack Drift Detection.<br>- **Practice:**<br>  + Write a YAML CloudFormation template to deploy a multi-tier network and EC2 infrastructure stack.<br>  + Integrate custom CloudWatch metrics with an Amazon Managed Grafana dashboard. | 05/05/2026 | 05/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Topic: Advanced IaC with AWS CDK, EC2 Optimization & VPC Flow Logs**<br>- **Knowledge:**<br>  + AWS Cloud Development Kit (CDK): Imperative IaC using TypeScript/Python, Constructs (L1, L2, L3), CDK Stacks, and CLI commands (`cdk synth`, `cdk deploy`).<br>  + EC2 Compute Optimizer: AI-driven right-sizing recommendations.<br>  + VPC Flow Logs: Network interface IP traffic monitoring and analysis.<br>- **Practice:**<br>  + Initialize an AWS CDK project to programmatically provision an S3 Bucket and DynamoDB Table.<br>  + Enable VPC Flow Logs, capture network traffic, and query logs using CloudWatch Logs Insights. | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Topic: Automated Backups (EBS Data Lifecycle) & VS Code Toolkit Setup**<br>- **Knowledge:**<br>  + Amazon Data Lifecycle Manager (DLM): Automated EBS snapshot lifecycle policies.<br>  + AWS Backup: Centralized backup policies across AWS services.<br>  + AWS Toolkit for VS Code: Local serverless testing, SAM integration, and resource navigation.<br>- **Practice:**<br>  + Configure an Amazon DLM policy to automate daily EBS snapshot creation and 7-day retention schedules.<br>  + Set up AWS Toolkit for VS Code and test Lambda execution locally. | 07/05/2026 | 07/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Topic: FinOps: Savings Plans & Reserved Instances & Cost Analysis using AWS Glue & Athena**<br>- **Knowledge:**<br>  + FinOps Commitment Models: Compute Savings Plans, EC2 Instance Savings Plans, vs Reserved Instances (Standard/Convertible).<br>  + Cost & Usage Reports (CUR): Detailed billing data export to S3.<br>  + Serverless Big Data Analytics: AWS Glue Data Catalog & Amazon Athena (SQL queries on billing data).<br>- **Practice:**<br>  + Set up a CUR export to S3, crawl the billing schema using AWS Glue, and query detailed cost metrics via Amazon Athena SQL. | 08/05/2026 | 08/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Week 3 Achievements:

#### Monday (04/05/2026):
* Understood event-driven serverless computing architecture using AWS Lambda and execution roles.
* Eliminated the need for bastion hosts and open SSH port 22 by implementing secure access via AWS Systems Manager Session Manager.
* Stored and retrieved application parameters securely using AWS Systems Manager Parameter Store.

#### Tuesday (05/05/2026):
* Mastered declarative Infrastructure as Code (IaC) principles using AWS CloudFormation templates.
* Deployed repeatable infrastructure stacks and performed Stack Drift Detection to identify manual configuration changes.
* Deepened system observability by analyzing logs with CloudWatch Logs Insights and visualizing metrics via Amazon Managed Grafana.

#### Wednesday (06/05/2026):
* Transitioned to imperative IaC by developing infrastructure stacks using the AWS Cloud Development Kit (CDK).
* Analyzed EC2 Compute Optimizer recommendations to right-size instance types and eliminate resource waste.
* Enabled VPC Flow Logs to inspect network traffic patterns and detect unauthorized access attempts.

#### Thursday (07/05/2026):
* Implemented automated data protection by configuring Amazon Data Lifecycle Manager (DLM) policies for EBS snapshots.
* Explored centralized governance for cross-service backup management using AWS Backup.
* Streamlined cloud development workflows by integrating the AWS Toolkit extension into local VS Code environments.

#### Friday (08/05/2026):
* Evaluated commitment-based pricing options (Savings Plans vs Reserved Instances) to optimize long-term compute expenditure.
* Configured AWS Cost & Usage Reports (CUR) to deliver granular billing data to an Amazon S3 storage bucket.
* Utilized AWS Glue and Amazon Athena to run serverless SQL queries on raw billing data, gaining deep financial visibility (FinOps).