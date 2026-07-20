---
title: "Week 11 Worklog"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:
* Conduct basic penetration testing and simulate attack vectors to validate edge and application security measures.
* Audit IAM policies and resource permissions using IAM Access Analyzer to eliminate privilege escalation risks and sensitive data leaks.
* Patch identified vulnerabilities, harden infrastructure, and finalize the comprehensive Cloud Security Audit Report before the product demo.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | **Topic: General Team Review on Testing Outcomes & Security Baseline**<br>- **Knowledge:**<br>  + Penetration testing methodologies for serverless architectures, vulnerability severity scoring (CVSS v3.1), OWASP Top 10 API Security Risks.<br>  + Setting security assessment scopes across web frontend, API endpoints, and database tiers.<br>- **Practice:**<br>  + Analyze E2E test results with cross-functional sub-teams, define security assessment scopes, and configure attack simulation tools (OWASP ZAP, Postman). | 29/06/2026 | 29/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Topic: Penetration Testing & WAF Attack Simulation (SQLi, XSS, Rate Limits)**<br>- **Knowledge:**<br>  + Web application exploit vectors (SQL Injection, Cross-Site Scripting - XSS, Parameter Tampering, HTTP Flood).<br>  + AWS WAF rule evaluation mechanics and Web ACL inspection logs.<br>- **Practice:**<br>  + Execute malicious payload simulations against CloudFront and API Gateway endpoints using OWASP ZAP.<br>  + Verify AWS WAF blocking capabilities and inspect WAF blocked request logs in CloudWatch. | 30/06/2026 | 30/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Topic: IAM Policy Hardening & Least-Privilege Audit**<br>- **Knowledge:**<br>  + Automated IAM auditing using AWS IAM Access Analyzer.<br>  + Identifying privilege escalation vectors and wildcard (`*`) over-grant risks in Action and Resource clauses.<br>  + Condition key enforcement (`aws:PrincipalTag`, `aws:SecureTransport`).<br>- **Practice:**<br>  + Scan all Lambda execution roles and IAM policies using IAM Access Analyzer.<br>  + Restrict wildcard resource permissions to exact DynamoDB/S3 ARNs and remove unused IAM permissions. | 01/07/2026 | 01/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Topic: Secrets Manager Audit, Data Leak Prevention & Encryption Inspection**<br>- **Knowledge:**<br>  + Data Loss Prevention (DLP) in cloud environments, KMS key policies, rotation logs.<br>  + Detecting sensitive credential exposure in CloudWatch Logs streams or API response payloads.<br>- **Practice:**<br>  + Audit AWS Secrets Manager access logs and inspect CloudWatch Logs using Insights queries to ensure no raw AI tokens or credentials are logged.<br>  + Enforce KMS key policy boundaries restricting secret decryption strictly to authorized roles. | 02/07/2026 | 02/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Topic: Vulnerability Patching, Hardening & Final Security Report Generation**<br>- **Knowledge:**<br>  + Remediation strategies for cloud misconfigurations, hardening CORS policies, and request body validation.<br>  + Drafting formal Cloud Cybersecurity Assessment Reports for enterprise review.<br>- **Practice:**<br>  + Patch identified minor vulnerabilities (stricter CORS origins, tighter API Gateway request models).<br>  + Compile security audit findings and generate the final Cloud Security Audit Report for Wakan. | 03/07/2026 | 03/07/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Week 11 Achievements:

#### Monday (29/06/2026):
* Conducted a general team review of E2E testing outcomes and established penetration testing scopes for the Wakan application.
* Set up security assessment and API vulnerability scanning tools (OWASP ZAP, Burp Suite, Postman).
* Aligned vulnerability severity benchmarks based on CVSS v3.1 and OWASP Top 10 API Security standards.

#### Tuesday (30/06/2026):
* Executed simulated web exploits (SQL Injection, Cross-Site Scripting, HTTP Floods) targeting Wakan endpoints.
* Confirmed that AWS WAF Web ACLs successfully intercepted and blocked 100% of malicious attack payloads at the edge.
* Inspected WAF Sampled Logs in CloudWatch to verify correct rule matching and IP blocking responses.

#### Wednesday (01/07/2026):
* Audited all IAM policies across Lambda execution roles using AWS IAM Access Analyzer.
* Eliminated all wildcard (`*`) resource permissions, restricting database access strictly to specific Wakan DynamoDB ARNs.
* Enforced the Principle of Least Privilege across all execution roles, revoking unnecessary permissions.

#### Thursday (02/07/2026):
* Audited AWS Secrets Manager access patterns and KMS key policies protecting external AI API tokens.
* Executed CloudWatch Logs Insights queries across all log streams, verifying zero leakage of plain-text secrets or sensitive tokens.
* Restricted KMS decryption permissions strictly to the AWS Lambda (AI Processor) execution role.

#### Friday (03/07/2026):
* Patched identified minor security misconfigurations, enforcing strict origin matching on API Gateway CORS policies.
* Verified JSON Schema payload validation models to drop malformed input requests before reaching compute layers.
* Compiled all security testing findings and generated the comprehensive Cloud Security Audit Report for the Wakan platform.