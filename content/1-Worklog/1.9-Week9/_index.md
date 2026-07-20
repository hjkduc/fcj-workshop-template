---
title: "Week 9 Worklog"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:
* Secure sensitive credentials used by AI processing modules using AWS Secrets Manager.
* Implement API rate limiting, throttling, and usage plans on Amazon API Gateway to prevent spam and resource abuse.
* Conduct internal security audits, cross-review backend/AI codebase, and enforce strict cloud security policies.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | **Topic: Peer Code Review & Secure Coding Standards (Backend & AI Integration)**<br>- **Knowledge:**<br>  + Static Application Security Testing (SAST) principles and OWASP Secure Coding Guidelines.<br>  + Identifying hardcoded credential vulnerabilities and insecure direct object references (IDOR).<br>  + Error handling best practices to prevent sensitive stack trace leakage.<br>- **Practice:**<br>  + Perform cross-team code review on Lambda backend scripts and AI integration modules.<br>  + Refactor Lambda codebase to remove local environment secret dependencies and standardize error responses. | 15/06/2026 | 15/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Topic: Credential Management & Encryption with AWS Secrets Manager**<br>- **Knowledge:**<br>  + AWS Secrets Manager architecture, secret rotation strategies, and KMS envelope encryption.<br>  + Dynamic secret retrieval at runtime via AWS SDK vs caching secrets in Lambda global memory scope.<br>  + Resource-based policies for Secrets Manager to restrict cross-account and unauthorized access.<br>- **Practice:**<br>  + Provision AWS Secrets Manager secrets to securely store External AI API tokens.<br>  + Implement dynamic secret retrieval inside the AWS Lambda (AI Processor) using AWS SDK with local caching. | 16/06/2026 | 16/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Topic: Amazon API Gateway Usage Plans, API Keys & Tiered Access Control**<br>- **Knowledge:**<br>  + API Gateway Usage Plans, API Keys, and client request throttling mechanics.<br>  + Mapping service tier quotas (Free, Plus, Pro) to usage plans for Wakan itinerary generation.<br>  + Request validation templates to reject malformed payloads before reaching Lambda.<br>- **Practice:**<br>  + Create API Gateway Usage Plans and API Keys corresponding to Wakan subscription tiers.<br>  + Associate API Keys with Cognito authenticated sessions and configure JSON Schema request validators. | 17/06/2026 | 17/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Topic: API Rate Limiting, Throttling Rules & DDoS Prevention**<br>- **Knowledge:**<br>  + Token Bucket algorithm used by Amazon API Gateway for request throttling.<br>  + Rate limits (steady-state requests per second) vs Burst limits (maximum capacity bucket).<br>  + Handling HTTP 429 (Too Many Requests) errors gracefully on client applications.<br>- **Practice:**<br>  + Configure Rate Limiting (50 req/sec) and Burst Limits (100 req/sec) on API Gateway stages.<br>  + Test API throttling resilience using simulated load tools and verify HTTP 429 response handling. | 18/06/2026 | 18/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Topic: Comprehensive Security Policy Audit & Cloud Architecture Review**<br>- **Knowledge:**<br>  + Cloud security auditing procedures, IAM privilege analysis, and network security review.<br>  + S3 Public Access Block verification, CloudWatch audit logging, and VPC endpoint security.<br>- **Practice:**<br>  + Execute an end-to-end security policy audit across all Wakan cloud resources (IAM, WAF, API Gateway, S3, Secrets Manager).<br>  + Generate an internal security audit report and resolve minor permission over-grant issues. | 19/06/2026 | 19/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Week 9 Achievements:

#### Monday (15/06/2026):
* Conducted a thorough peer code review across Backend and AI integration sub-teams, ensuring compliance with OWASP secure coding guidelines.
* Refactored Lambda functions to eliminate hardcoded configuration values and prevented internal system stack trace leakage in API responses.
* Standardized JSON exception responses for seamless error handling on the Wakan frontend interface.

#### Tuesday (16/06/2026):
* Encrypted and safely isolated External AI API tokens inside AWS Secrets Manager using KMS keys.
* Integrated dynamic secret retrieval in AWS Lambda (AI Processor) via AWS SDK, leveraging global variable caching to minimize API call latency and costs.
* Attached resource-based permission policies ensuring only designated Lambda execution roles can decrypt and read the AI tokens.

#### Wednesday (17/06/2026):
* Built Amazon API Gateway Usage Plans and API Keys to enforce usage quotas aligned with Wakan subscription tiers (Free, Plus, Pro).
* Implemented request validation models on API Gateway to drop invalid HTTP payloads at the edge before invoking downstream compute.
* Linked Cognito identity authentication tokens with API Gateway key validation workflows.

#### Thursday (18/06/2026):
* Configured Rate Limiting (steady-state) and Burst Throttling rules on Amazon API Gateway stages to prevent API abuse and DDoS floods.
* Protected downstream Lambda functions and external AI APIs from unexpected traffic spikes and cost overruns.
* Validated throttling behavior using automated request bursts, verifying correct HTTP 429 (Too Many Requests) error responses.

#### Friday (19/06/2026):
* Completed a comprehensive internal cybersecurity audit across all Wakan infrastructure assets.
* Verified that all S3 buckets enforce Block Public Access, CloudFront uses OAC, and IAM roles strictly adhere to Least-Privilege boundaries.
* Documented the final security audit review and secured architecture approval for production readiness.