---
title: "Week 2 Worklog"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:
* Explore advanced database solutions (DynamoDB, ElastiCache), Content Delivery Networks (CloudFront), and migration strategies (DMS, Disaster Recovery).
* Implement comprehensive enterprise security across identity (Cognito, SSO), data protection (KMS, Macie), threat detection (GuardDuty), and edge protection (WAF).
* Design highly available, fault-tolerant, and interconnected multi-VPC networks (Transit Gateway, EBS Multi-Attach).

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | **Topic: NoSQL with DynamoDB, Caching with ElastiCache & Content Delivery via CloudFront**<br>- **Knowledge:**<br>  + Amazon DynamoDB: Key-value NoSQL database, Partition/Sort Keys, Global/Local Secondary Indexes (GSI/LSI), Time-To-Live (TTL).<br>  + Amazon ElastiCache: In-memory caching engines (Redis vs Memcached), Caching strategies (Lazy Loading, Write-Through).<br>  + Amazon CloudFront: Global Content Delivery Network (CDN), Edge Locations, Cache Behaviors, Origin Access Control (OAC).<br>- **Practice:**<br>  + Create a DynamoDB table with GSI and TTL auto-expiration.<br>  + Deploy a CloudFront Distribution pointing to an S3 Bucket origin with OAC restrictions. | 27/04/2026 | 27/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Topic: Server Migration (VM Import), DB Migration (DMS) & Disaster Recovery (DR)**<br>- **Knowledge:**<br>  + AWS Migration Strategies: 6 Rs of migration, AWS Application Migration Service (MGN).<br>  + AWS Database Migration Service (DMS): Replication Instances, Source/Target Endpoints, Schema Conversion Tool (SCT).<br>  + Disaster Recovery (DR): RTO & RPO metrics, DR strategies (Backup & Restore, Pilot Light, Warm Standby, Multi-Site Active-Active).<br>- **Practice:**<br>  + Setup an AWS DMS replication instance and configure a migration task from RDS MySQL to S3/DynamoDB.<br>  + Design a Pilot Light DR architecture diagram for an enterprise web app. | 28/04/2026 | 28/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Topic: Identity Management (SSO, Cognito) & Application Protection (WAF, Firewall Manager)**<br>- **Knowledge:**<br>  + IAM Identity Center (AWS SSO) & Identity Boundaries.<br>  + Amazon Cognito: User Pools (Authentication) vs Identity Pools (Authorization/Federated Identities).<br>  + AWS WAF (Web Application Firewall): Web ACLs, Managed Rule Groups, Rate-based Rules.<br>  + AWS Firewall Manager: Centralized security management across multi-account AWS Organizations.<br>- **Practice:**<br>  + Create an Amazon Cognito User Pool with email verification & MFA enabled.<br>  + Attach an AWS WAF Web ACL with SQLi/XSS protection rules to an ALB or CloudFront Endpoint. | 29/04/2026 | 29/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Topic: Data Protection (KMS, Macie), Threat Detection (GuardDuty) & Network Integration (Transit Gateway)**<br>- **Knowledge:**<br>  + AWS KMS: Symmetric vs Asymmetric Keys, Envelope Encryption, Customer Managed Keys (CMK).<br>  + Amazon Macie: Automated PII (Personally Identifiable Information) discovery & data classification using ML.<br>  + Amazon GuardDuty: Continuous threat intelligence & anomaly detection.<br>  + AWS Transit Gateway: Centralized hub-and-spoke network router connecting multi-VPC and on-premises networks.<br>- **Practice:**<br>  + Generate a KMS CMK key and configure S3 server-side encryption (SSE-KMS).<br>  + Set up AWS Transit Gateway to interconnect two isolated VPCs without VPC Peering. | 30/04/2026 | 30/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Topic: High Availability Storage (EBS Multi-Attach) & Enterprise Failover Clusters**<br>- **Knowledge:**<br>  + EBS Provisioned IOPS (io1/io2) with Multi-Attach capabilities.<br>  + Windows Server Failover Clustering (WSFC) & SQL Server Always On Availability Groups on AWS.<br>  + FSx for Windows File Server: Multi-AZ shared file storage.<br>- **Practice:**<br>  + Provision an io2 EBS volume with Multi-Attach enabled and mount it across multiple Linux EC2 instances.<br>  + Review architectural patterns for deploying Multi-AZ SQL Server Failover Clusters on AWS. | 01/05/2026 | 01/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Week 2 Achievements:

#### Monday (27/04/2026):
* Mastered NoSQL database design principles with Amazon DynamoDB, including partition key strategies and TTL.
* Understood in-memory caching patterns using Amazon ElastiCache (Redis) to relieve database read pressure.
* Deployed Amazon CloudFront with Origin Access Control (OAC), securing S3 origins and accelerating global content delivery.

#### Tuesday (28/04/2026):
* Analyzed the 6 Rs of cloud migration and mastered the mechanics of AWS Database Migration Service (DMS).
* Configured an active DMS replication pipeline to migrate relational data with minimal downtime.
* Evaluated RTO and RPO requirements to formulate appropriate Disaster Recovery (DR) architectures (Pilot Light & Warm Standby).

#### Wednesday (29/04/2026):
* Deepened identity management knowledge through IAM Identity Center and Amazon Cognito.
* Built a secure authentication workflow using Amazon Cognito User Pools.
* Implemented perimeter protection by configuring AWS WAF Web ACLs against common web vulnerabilities (OWASP Top 10).

#### Thursday (30/04/2026):
* Mastered envelope encryption concepts using AWS KMS Customer Managed Keys (CMK).
* Learned automated PII data discovery techniques with Amazon Macie and threat detection with Amazon GuardDuty.
* Interconnected multiple isolated VPCs using AWS Transit Gateway in a scalable hub-and-spoke topology.

#### Friday (01/05/2026):
* Explored high-performance block storage using EBS Multi-Attach on io2 volumes.
* Analyzed high-availability enterprise patterns for Windows Server Failover Clustering (WSFC) and SQL Server.
* Understood shared storage options for enterprise workloads using Amazon FSx for Windows File Server.