---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:
* Study modern cloud architecture methodologies, decomposing legacy monolithic applications into agile, event-driven microservices.
* Build a full-stack serverless application (Serverless Book Store) combining AWS Lambda, Amazon DynamoDB, Amazon S3, and API Gateway.
* Master asynchronous event-driven messaging (SNS, SQS, EventBridge) and flexible GraphQL API integration with AWS AppSync.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | **Topic: Migration to Microservices & Event-Driven Architecture Fundamentals**<br>- **Knowledge:**<br>  + Monolith vs Microservices: Benefits, challenges, Domain-Driven Design (DDD), and Strangler Fig pattern.<br>  + Event-Driven Architecture (EDA): Event Producers, Event Routers (Amazon EventBridge), Event Consumers, and Schema Registry.<br>- **Practice:**<br>  + Design a microservices decomposition roadmap for a legacy monolithic app using the Strangler Fig pattern and EventBridge rules. | 18/05/2026 | 18/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Topic: SPA Authentication & Integrating AWS AI Services**<br>- **Knowledge:**<br>  + Single Page Application (SPA) Security: OAuth 2.0 / OIDC authentication flows, JWT handling, and CORS policies.<br>  + Pre-built AWS AI Services: Amazon Rekognition (Vision), Polly (Text-to-Speech), Translate, and Transcribe.<br>- **Practice:**<br>  + Build a web frontend prototype calling AWS AI services (Polly & Translate) via secure API endpoints. | 19/05/2026 | 19/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Topic: Serverless Book Store: Backend with Lambda, S3 & DynamoDB**<br>- **Knowledge:**<br>  + Serverless Application Patterns: RESTful API design using Amazon API Gateway.<br>  + DynamoDB Single-Table Design: Access patterns, primary keys, and Secondary Indexes for efficient querying.<br>  + S3 Asset Storage: Hosting web assets and managing CORS rules.<br>- **Practice:**<br>  + Develop core RESTful CRUD endpoints for the Serverless Book Store using API Gateway, Lambda, and DynamoDB. | 20/05/2026 | 20/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Topic: Frontend Integration, AWS SAM Deployment & Cognito User Authentication**<br>- **Knowledge:**<br>  + Infrastructure as Code for Serverless: AWS Serverless Application Model (SAM) templates, CLI workflow (`sam build`, `sam deploy`).<br>  + User Authentication: Amazon Cognito User Pools, Hosted UI, and API Gateway Cognito Authorizers.<br>- **Practice:**<br>  + Deploy the full-stack Book Store application using AWS SAM CLI.<br>  + Integrate Amazon Cognito User Pools to secure backend API routes with JWT token verification. | 21/05/2026 | 21/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Topic: Asynchronous Event Handling (SQS/SNS) & GraphQL APIs with AWS AppSync**<br>- **Knowledge:**<br>  + Messaging Decoupling: Amazon SNS (Pub/Sub) vs Amazon SQS (Queuing, Dead Letter Queues - DLQs), Fan-out pattern.<br>  + GraphQL APIs: REST vs GraphQL comparison, AWS AppSync schemas, Data Sources, and Resolvers.<br>- **Practice:**<br>  + Implement an asynchronous order processing pipeline using SNS fan-out to SQS queues.<br>  + Build an AWS AppSync GraphQL API querying DynamoDB tables with JavaScript resolvers. | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Week 5 Achievements:

#### Monday (18/05/2026):
* Mastered architectural strategies for migrating monolithic applications to microservices using Domain-Driven Design and the Strangler Fig pattern.
* Understood core Event-Driven Architecture (EDA) principles and event routing capabilities with Amazon EventBridge.
* Designed an event-driven integration blueprint to decouple legacy components progressively.

#### Tuesday (19/05/2026):
* Understood secure authentication patterns for Single Page Applications (SPAs) using OAuth 2.0 and JWTs.
* Explored managed AWS AI Services (Polly, Translate, Rekognition) for rapid feature integration without ML expertise.
* Developed a web interface that seamlessly translates text and generates audio streams via AWS AI APIs.

#### Wednesday (20/05/2026):
* Applied DynamoDB Single-Table Design principles to optimize data access patterns for the Serverless Book Store.
* Created RESTful API routes in Amazon API Gateway backed by AWS Lambda business logic.
* Configured Amazon S3 for secure static web asset hosting and CORS compliance.

#### Thursday (21/05/2026):
* Automated full-stack serverless deployments using the AWS Serverless Application Model (SAM) CLI.
* Secured backend API Gateway endpoints using Amazon Cognito User Pool Authorizers.
* Connected the frontend user interface to Cognito authentication workflows for user registration and sign-in.

#### Friday (22/05/2026):
* Built a resilient, decoupled messaging pipeline using the Amazon SNS fan-out pattern to Amazon SQS queues with Dead Letter Queue (DLQ) error handling.
* Learned the fundamentals of GraphQL vs REST APIs and deployed an AWS AppSync API.
* Configured AppSync data sources and resolvers to query DynamoDB tables flexibly with minimal network payload.