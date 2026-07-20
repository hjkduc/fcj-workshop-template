---
title: "Week 7 Worklog"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:
* Kick off the real-world capstone project **Wakan (Personalized AI Travel Assistant)**, defining product scope and service tiering (Free/Plus/Pro).
* Design the complete Cloud-Native Serverless system architecture and establish collaborative Git repositories and AWS IAM developer environments.
* Perform a preliminary security review and architecture evaluation against the six pillars of the AWS Well-Architected Framework.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | **Topic: Project Kickoff, Feature Scope Definition & Environment Setup**<br>- **Knowledge:**<br>  + Product Requirements Document (PRD) creation for Wakan AI Travel Assistant.<br>  + Feature tiering strategy (Free vs Plus vs Pro tiers for itinerary generation limits and AI API quotas).<br>  + Team workspace security and version control repository structuring.<br>- **Practice:**<br>  + Finalize Wakan PRD and feature breakdown.<br>  + Initialize team GitHub repository and create dedicated individual IAM Users with MFA enforcement for team members. | 01/06/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Topic: Wakan Cloud Architecture Design (Serverless & Microservices)**<br>- **Knowledge:**<br>  + Decoupled Serverless Topology: Frontend delivery (S3 + CloudFront + OAC), API tier (API Gateway + Cognito), Async compute (Lambda + SQS + Step Functions), and Data tier (DynamoDB).<br>  + Security Perimeter: AWS WAF Web ACLs, Origin Cloaking, and VPC Isolation.<br>- **Practice:**<br>  + Draft and finalize the high-level AWS system architecture diagram using Draw.io / Lucidchart.<br>  + Define REST API endpoints, request/response schemas, and DynamoDB data access patterns. | 02/06/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Topic: AWS Well-Architected Framework Review & Security Baseline**<br>- **Knowledge:**<br>  + The 6 Pillars: Security, Operational Excellence, Reliability, Performance Efficiency, Cost Optimization, and Sustainability.<br>  + Security Pillar Deep Dive: Least privilege access, data encryption at rest/in transit, edge protection.<br>- **Practice:**<br>  + Conduct the AWS Well-Architected Tool assessment for the proposed Wakan architecture.<br>  + Identify high-risk issues (HRI) and draft a mitigation roadmap for authentication and API endpoints. | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Topic: Identity and Access Management (IAM) Roles & Security Guardrails**<br>- **Knowledge:**<br>  + IAM Policy Syntax: Effect, Action, Resource, Conditions.<br>  + Cross-service IAM Execution Roles (Lambda execution roles, API Gateway logging roles).<br>  + Least-Privilege enforcement and Permission Boundaries.<br>- **Practice:**<br>  + Draft JSON IAM execution policies for Lambda workers with minimal DynamoDB and Secrets Manager permissions.<br>  + Configure AWS Secrets Manager secret structures for external AI API key management. | 04/06/2026 | 04/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Topic: Team Sync, Architecture Review with Mentors & Baseline Sign-off**<br>- **Knowledge:**<br>  + Technical presentation skills and architectural decision record (ADR) documentation.<br>  + Feedback integration from Senior Cloud Architects.<br>- **Practice:**<br>  + Present the Wakan architecture proposal and Well-Architected assessment to AWS Mentors.<br>  + Incorporate mentor feedback regarding asynchronous processing and get formal architecture sign-off. | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Week 7 Achievements:

#### Monday (01/06/2026):
* Successfully kicked off project **Wakan (Personalized AI Travel Assistant)**, defining the core product scope and feature tiering (Free, Plus, Pro).
* Established team version control structure on GitHub with branch protection rules.
* Provisioned individual IAM Users with MFA enforcement and initial permission boundaries for all team members.

#### Tuesday (02/06/2026):
* Designed and finalized the complete AWS Serverless architecture diagram for Wakan, featuring CloudFront, S3, API Gateway, Cognito, Lambda, DynamoDB, and WAF.
* Defined RESTful API contracts and data models for itinerary generation, user profiles, and caching.
* Mapped data flow connections between API Gateway, Cognito authorizers, and backend Lambda workers.

#### Wednesday (03/06/2026):
* Executed an AWS Well-Architected Framework assessment across all 6 pillars for the Wakan architecture proposal.
* Identified potential bottlenecks in synchronous AI API invocations and planned asynchronous processing fallback mechanisms.
* Established security baselines prioritizing data encryption in transit (HTTPS/TLS) and at rest (KMS).

#### Thursday (04/06/2026):
* Created fine-grained IAM Execution Roles for Lambda functions adhering strictly to the Principle of Least Privilege.
* Configured AWS Secrets Manager parameter structures to securely store external AI API tokens without hardcoding credentials in source code.
* Defined CloudWatch logging permission policies for API Gateway and Lambda execution environments.

#### Friday (05/06/2026):
* Presented the Wakan architecture design and Well-Architected review report to AWS Mentors.
* Received positive evaluation on security posture and validated the asynchronous processing strategy for AI itinerary generation.
* Secured formal project architecture sign-off, clearing the team to proceed into infrastructure provisioning and feature development.