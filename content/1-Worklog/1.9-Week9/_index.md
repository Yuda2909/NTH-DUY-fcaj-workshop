---
title: "Worklog Week 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives:
- Kickstart the foundational architecture for the AWS BILLO project.
- Initialize the initial project structures for both Frontend and Backend.
- Establish the core serverless infrastructure on AWS tailored for the development environment.
- Configure critical cloud services including Authentication, API Gateway, Databases, Storage, and Logging.
- Deploy the initial backend stack and successfully connect the frontend application to live AWS APIs.
- Work on-site at the company office on 06/15/2026 from 08:30 to 16:30.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| Mon | - Work on-site at the company office from 08:30 to 16:30 <br> - Review the system architecture and design schemas finalized in Week 8 <br> - Initialize the Flutter frontend project structure <br> - Initialize the Node.js backend project structure <br> - Discuss source code organization patterns and team development workflows | 06/15/2026 | 06/15/2026 | Company office |
| Tue | - Scaffold the initial AWS SAM / CloudFormation templates <br> - Define fundamental serverless resources required for the dev environment <br> - Configure deployment settings targeting the Singapore region (`ap-southeast-1`) <br> - Review the integration patterns between Lambda, API Gateway, DynamoDB, and S3 | 06/16/2026 | 06/16/2026 | https://cloudjourney.awsstudygroup.com/ |
| Wed | - Create and configure an Amazon Cognito User Pool <br> - Provision RBAC roles/groups within the User Pool: <br>&emsp; + Customer <br>&emsp; + Merchant <br>&emsp; + Admin <br> - Configure phone-number-based registration and OTP-based authentication workflows <br> - Set up and secure endpoints using API Gateway JWT Authorizers | 06/17/2026 | 06/17/2026 | https://cloudjourney.awsstudygroup.com/ |
| Thu | - Design and provision Amazon DynamoDB tables: <br>&emsp; + Main Table <br>&emsp; + Idempotency Table <br> - Architect the single-table design schemas for user profiles, wallets, merchant applications, stores, products, orders, and transactions <br> - Create Amazon S3 buckets for hosting product media and business licenses | 06/18/2026 | 06/18/2026 | https://cloudjourney.awsstudygroup.com/ |
| Fri | - Develop core boilerplate AWS Lambda functions for business logic <br> - Implement secure pre-signed URL generation workflows for direct-to-S3 uploads <br> - Configure Amazon CloudWatch Logs for enhanced Lambda execution monitoring <br> - Deploy the complete serverless dev stack onto AWS <br> - Establish Flutter frontend integration with live AWS APIs and perform authorized request testing | 06/19/2026 | 06/19/2026 | https://cloudjourney.awsstudygroup.com/ |

---

### Week 9 Achievements:

#### 1. Project Initialization & Architecture Alignment
* Successfully established the project foundation for the **AWS BILLO** ecosystem, decoupling the client-side app from the serverless backend.
* Scaffolded a clean, production-ready **Flutter frontend architecture**, adopting robust state management and folder structures optimized for scale.
* Initialized a **Node.js serverless backend project**, pre-configured for microservice-style development using native AWS integrations.
* Completed a full-day on-site collaboration at the office to review Week 8 system designs, aligning team workflows on Git branching strategies and codebase conventions.

#### 2. Infrastructure as Code (IaC) & Dev Environment Setup
* Mastered the utilization of **AWS SAM (Serverless Application Model)** and CloudFormation to define cloud resources programmatically.
* Successfully initialized deployment configurations targeting the **Singapore region (`ap-southeast-1`)** to minimize latency for end-users.
* Deepened technical knowledge regarding the reactive loops, invocation patterns, and execution context handoffs between API Gateway, Lambda, DynamoDB, and S3.

#### 3. Authentication & Security Enforcement
* Created and optimized an **Amazon Cognito User Pool** acting as the centralized Identity Provider (IdP) for the platform.
* Configured robust Role-Based Access Control (RBAC) by establishing distinct user groups:
    * **Customer**: For standard users and wallet holders.
    * **Merchant**: For business owners managing storefronts.
    * **Admin**: For internal platform operations and approvals.
* Implemented a secure authentication flow leveraging **Phone Number attributes and SMS-based OTP** (One-Time Password) verifications.
* Secured API endpoints by attaching an **API Gateway JWT Authorizer**, enforcing signature verification and token validation on all inbound requests.

#### 4. Database Modeling & Cloud Storage Provisioning
* Provisions high-performance **Amazon DynamoDB** tables tailored for serverless latency:
    * **Main Table**: Optimized for transactional records using Single-Table Design patterns.
    * **Idempotency Table**: Dedicated to preventing duplicate processing of financial API calls.
* Completed the data modeling schemas for critical entities including User Profiles, Digital Wallets, Merchant Applications, Stores, Product Catalogs, Orders, and Ledger Transactions.
* Created secure **Amazon S3 Buckets** configured with strict CORS policies to safely store product imagery and corporate KYC documents.

#### 5. Serverless Implementation & Frontend Integration
* Developed and deployed core **AWS Lambda Functions** written in Node.js to handle baseline backend CRUD operations and authorization checks.
* Built a secure **S3 Pre-signed URL generation mechanism**, allowing the frontend to upload large media assets directly to cloud storage safely without bottlenecking the backend computing layer.
* Configured dedicated **Amazon CloudWatch Log Groups** featuring structured logging to streamline real-time tracing, system metrics auditing, and debugging.
* Executed a flawless deployment of the serverless stack to the development environment via the AWS SAM CLI.
* Successfully connected the local Flutter application to the live AWS API Gateway, completing end-to-end integration tests for authorized HTTP requests.