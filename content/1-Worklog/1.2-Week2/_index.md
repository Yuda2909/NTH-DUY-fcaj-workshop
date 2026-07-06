---
title: "Worklog Week 2"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Week 2 Objectives:
- Research core AWS Compute and Storage services required for a serverless paradigm.
- Master the fundamentals of AWS Lambda and its execution lifecycles.
- Understand Amazon S3 architecture, bucket policies, and asset management patterns.
- Implement practical sandbox proofs-of-concept (PoC) using the AWS Console.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| Mon | - Work on-site at the company office <br> - Participate in technical alignment meetings regarding microservice vs. serverless design paradigms for the BILLO backend | 04/27/2026 | 04/27/2026 | Company office |
| Tue | - Deep-dive into AWS Lambda core mechanics (execution context, cold starts, IAM roles) <br> - Write and test basic Node.js Lambda handlers directly inside the AWS Console | 04/28/2026 | 04/28/2026 | https://cloudjourney.awsstudygroup.com/ |
| Wed | - Study Amazon Simple Storage Service (S3) architecture and storage classes <br> - Practice creating S3 buckets, uploading objects, and managing public/private access settings | 04/29/2026 | 04/29/2026 | https://cloudjourney.awsstudygroup.com/ |
| Thu | - Configure secure S3 Bucket Policies and Cross-Origin Resource Sharing (CORS) rule structures <br> - Set up a practical trigger connecting an S3 bucket upload to an automated Lambda function | 04/30/2026 | 04/30/2026 | https://cloudjourney.awsstudygroup.com/ |
| Fri | - Test event-driven execution flows by analyzing logs generated during automated triggers <br> - Document performance characteristics and findings for the serverless storage stack | 05/01/2026 | 05/01/2026 | https://cloudjourney.awsstudygroup.com/ |

---

### Week 2 Achievements:

#### 1. Serverless Compute Mechanics
* Mastered the operational lifecycle of **AWS Lambda**, including trigger bindings, timeout behaviors, and execution roles.
* Successfully built sandbox Lambda handlers capable of processing incoming JSON event payloads and returning structured responses.

#### 2. Cloud Storage Mastery & Event-Driven Flows
* Acquired a thorough understanding of **Amazon S3** object storage structures, resource access control lists (ACLs), and bucket permissions.
* Engineered an event-driven automation loop: uploading a file to an S3 object path securely triggers an asynchronous AWS Lambda function invocation.
* Formulated clean, restrictive CORS configurations to prevent unauthorized client domains from polling sensitive cloud resources.