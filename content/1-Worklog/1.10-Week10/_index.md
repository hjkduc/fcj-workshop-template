---
title: "Week 10 Worklog"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:
* Perform End-to-End (E2E) full system integration testing across all Wakan cloud microservices.
* Establish a centralized observability and monitoring framework using Amazon CloudWatch Logs and CloudWatch Alarms.
* Enforce financial guardrails and cost controls via AWS Budgets and SNS notifications to protect promotional credits.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | **Topic: End-to-End (E2E) Full System Integration Testing**<br>- **Knowledge:**<br>  + End-to-End synthetic user testing methodologies for decoupled serverless architectures.<br>  + Trace analysis across CloudFront -> API Gateway -> Cognito -> Lambda (Orchestrator & AI Processor) -> DynamoDB.<br>  + Edge-case validation: Auth failure, API timeout, cache hit/miss logic.<br>- **Practice:**<br>  + Execute full user journeys (registration, login, travel preference selection, AI itinerary generation, cache retrieval).<br>  + Benchmark latency and identify processing bottlenecks during live AI API invocation. | 22/06/2026 | 22/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Topic: Centralized Observability & CloudWatch Logs Management**<br>- **Knowledge:**<br>  + Amazon CloudWatch Log Groups, Log Streams, Log Retention Policies, and structured JSON logging.<br>  + Log aggregation across API Gateway, Lambda functions, Cognito, and WAF.<br>  + Querying multi-service logs efficiently using CloudWatch Logs Insights.<br>- **Practice:**<br>  + Configure 14-day retention policies on all Wakan CloudWatch Log Groups to prevent unnecessary storage costs.<br>  + Write custom CloudWatch Logs Insights queries to track API error counts and cold start execution times. | 23/06/2026 | 23/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Topic: Proactive Monitoring, CloudWatch Alarms & SNS Alerting**<br>- **Knowledge:**<br>  + Amazon CloudWatch Alarms, metric math, static threshold vs anomaly detection models.<br>  + Amazon SNS (Simple Notification Service) developer alert topics.<br>  + Key performance indicators (KPIs): API Gateway 5xx rate, Lambda execution errors, DynamoDB throttling.<br>- **Practice:**<br>  + Create an Amazon SNS alert topic sending email notifications to the engineering team.<br>  + Configure CloudWatch Alarms for Lambda error thresholds (>2% error rate) and API Gateway HTTP 5xx responses. | 24/06/2026 | 24/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Topic: Financial Guardrails, AWS Budgets & Anomaly Detection**<br>- **Knowledge:**<br>  + FinOps cost control mechanisms and tracking credit exhaustion rates on AWS.<br>  + AWS Budgets: Fixed amount vs percentage thresholds, actual spend vs forecasted spend alerts.<br>  + AWS Cost Anomaly Detection integration for automatic cost spike identification.<br>- **Practice:**<br>  + Configure AWS Budgets with tiered email alerts triggered when credit consumption reaches 50%, 80%, and 100%.<br>  + Set up AWS Cost Anomaly Detection monitors targeting Wakan serverless compute and database services. | 25/06/2026 | 25/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Topic: Serverless Performance Optimization & Cross-Team Bug Remediation**<br>- **Knowledge:**<br>  + AWS Lambda cold start mitigation, memory provisioning optimization, and concurrency limits.<br>  + DynamoDB query vs scan performance tuning, TTL cleanup verification.<br>- **Practice:**<br>  + Resolve bugs identified during E2E testing (handling JSON parsing edge cases and CORS preflight headers).<br>  + Fine-tune Lambda memory allocations to reduce execution duration and lower overall execution cost. | 26/06/2026 | 26/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Week 10 Achievements:

#### Monday (22/06/2026):
* Executed synthetic End-to-End (E2E) integration testing simulating real user journeys on the Wakan application.
* Verified seamless request forwarding from CloudFront edge locations through API Gateway to Cognito authentication and Lambda compute.
* Tested DynamoDB caching logic, confirming that duplicate itinerary requests successfully hit cache and return instant responses without triggering external AI calls.

#### Tuesday (23/06/2026):
* Centralized system-wide logging by configuring Amazon CloudWatch Log Groups for API Gateway, Lambda functions, and AWS WAF.
* Implemented a 14-day log retention policy across all log groups to avoid storage bloat and unnecessary cloud costs.
* Mastered CloudWatch Logs Insights, authoring custom SQL-like queries to parse structured JSON logs and diagnose system exceptions.

#### Wednesday (24/06/2026):
* Built a proactive system alerting ecosystem using Amazon CloudWatch Alarms integrated with Amazon SNS email notifications.
* Set up automated alarms triggering notifications when API Gateway returns 5xx Server Errors or when Lambda functions experience execution failures.
* Configured DynamoDB read/write capacity alarms to detect potential database throttling during traffic spikes.

#### Thursday (25/06/2026):
* Secured project finances by implementing multi-tiered budget alerts in AWS Budgets to monitor promotional credit usage.
* Set up automated email notifications when actual or forecasted cloud expenditure reaches 50%, 80%, and 100% of allocated budget limits.
* Activated AWS Cost Anomaly Detection to automatically alert the team if unexpected cost spikes occur in Lambda or DynamoDB usage.

#### Friday (26/06/2026):
* Collaborated across sub-teams (Frontend, Backend, AI) to fix edge-case bugs discovered during initial E2E testing.
* Resolved CORS preflight header issues on API Gateway and handled unexpected payload formatting from external AI APIs.
* Optimized Lambda memory configurations, successfully reducing average execution times and improving overall application responsiveness.