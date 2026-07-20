---
title: "Week 8 Worklog"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:
* Establish unified API contract schemas between Frontend, Backend, and AI processing sub-teams.
* Deploy foundational web hosting for Wakan UI Assets using Amazon S3 and Amazon CloudFront secured by Origin Access Control (OAC).
* Enforce edge protection using AWS WAF and configure identity management via Amazon Cognito User Pools and least-privilege IAM roles.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | **Topic: API Contract Synchronization & Schema Specification (Frontend-Backend-AI)**<br>- **Knowledge:**<br>  + RESTful API standards, OpenAPI (Swagger) 3.0 specification, JSON Schema validation.<br>  + Decoupled architecture contracts for asynchronous itinerary generation payloads.<br>- **Practice:**<br>  + Draft OpenAPI spec for Wakan REST API endpoints (`/itinerary`, `/preferences`, `/user/profile`).<br>  + Align request/response parameters and error codes across Frontend, Backend, and AI sub-teams. | 08/06/2026 | 08/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Topic: Frontend Hosting via Amazon S3 & CDN Acceleration with Amazon CloudFront**<br>- **Knowledge:**<br>  + Amazon S3 static asset storage and bucket isolation strategies.<br>  + Amazon CloudFront Distribution, Edge Caching, Custom SSL/TLS certificates via AWS Certificate Manager (ACM).<br>  + Origin Access Control (OAC): Restricting public S3 bucket access to CloudFront requests only.<br>- **Practice:**<br>  + Provision a private S3 bucket for Wakan web frontend assets.<br>  + Deploy a CloudFront distribution with OAC integration, blocking direct public internet access to the S3 bucket. | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Topic: Edge Security Perimeter with AWS WAF & Threat Mitigation**<br>- **Knowledge:**<br>  + AWS WAF (Web Application Firewall): Web ACLs, Custom Rules vs AWS Managed Rule Groups (`AWSManagedRulesCommonRuleSet`, SQLi, Known Bad Inputs).<br>  + Rate-based rules for HTTP flood / DDoS attack mitigation at the edge.<br>- **Practice:**<br>  + Provision an AWS WAF Web ACL attached to the Wakan CloudFront distribution.<br>  + Configure rate-limiting rules (100 requests / 5 min per IP) and enable WAF sampled request logging. | 10/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Topic: User Identity Management & Authentication with Amazon Cognito**<br>- **Knowledge:**<br>  + Amazon Cognito User Pools vs Identity Pools, OAuth 2.0 / OIDC flows.<br>  + JWT Token Lifecycle: ID Tokens, Access Tokens, Refresh Tokens.<br>  + User Pool Client configurations, MFA enforcement, and custom user attributes.<br>- **Practice:**<br>  + Provision an Amazon Cognito User Pool for Wakan with email sign-in verification.<br>  + Configure custom user attributes (preferred travel styles, budget tier) and enable Hosted UI integration. | 11/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Topic: Least-Privilege IAM Execution Roles & Security Guardrails for AWS Lambda**<br>- **Knowledge:**<br>  + Granular IAM execution roles for AWS Lambda workers.<br>  + Policy condition keys (`aws:PrincipalOrgID`, `s3:ResourceAccount`, `dynamodb:LeadingKeys`).<br>  + Least-Privilege access enforcement and resource-based policies.<br>- **Practice:**<br>  + Author strict JSON IAM execution policies for Wakan Lambda functions, restricting DynamoDB access to specific table ARNs and Secrets Manager to specific secret keys.<br>  + Validate IAM permissions using IAM Policy Simulator. | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Week 8 Achievements:

#### Monday (08/06/2026):
* Synchronized RESTful API contract specifications across Frontend, Backend, and AI sub-teams using OpenAPI 3.0 standards.
* Defined data schemas for user travel preference inputs and AI-generated itinerary outputs.
* Established standardized JSON error code structures for client-side exception handling.

#### Tuesday (09/06/2026):
* Deployed a private Amazon S3 bucket for hosting Wakan static web frontend assets (UI Assets).
* Configured Amazon CloudFront CDN distribution to accelerate global web asset delivery with low latency.
* Restricted S3 origin access using CloudFront Origin Access Control (OAC), completely removing public bucket access.

#### Wednesday (10/06/2026):
* Built a robust edge security perimeter by deploying an AWS WAF Web ACL on top of CloudFront.
* Configured AWS Managed Rule Groups to block common web vulnerabilities (OWASP Top 10, SQLi, Cross-Site Scripting).
* Implemented rate-based rules to protect backend services against automated bot traffic and HTTP DDoS floods.

#### Thursday (11/06/2026):
* Deployed Amazon Cognito User Pools to manage registration, login, and authentication workflows for Wakan users.
* Enabled email verification, strong password policies, and Multi-Factor Authentication (MFA) capabilities.
* Configured custom user profile attributes to store user travel preferences directly within Cognito tokens.

#### Friday (12/06/2026):
* Authored granular IAM Execution Roles for all backend Lambda functions adhering strictly to the Principle of Least Privilege.
* Restricted Lambda database access specifically to Wakan DynamoDB table ARNs and secret access strictly to designated Secrets Manager keys.
* Tested and validated IAM execution boundaries using IAM Policy Simulator to prevent unintended privilege escalation.