---
title: "Worklog Week 3"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:
- Understand NoSQL database fundamentals with a primary focus on Amazon DynamoDB.
- Learn core concepts of DynamoDB: Partition Keys (PK), Sort Keys (SK), and Indexes.
- Research API architecture options using Amazon API Gateway.
- Build an interconnected backend pipeline: API Gateway to Lambda to DynamoDB.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| Mon | - Work on-site at the company office <br> - Sync up on data persistence layer demands for the BILLO ledger and real-time transaction processing requirements | 05/04/2026 | 05/04/2026 | Company office |
| Tue | - Study Amazon DynamoDB data models, read/write capacity units (RCU/WCU), and on-demand pricing <br> - Create test tables using composite primary keys (PK + SK) | 05/05/2026 | 05/05/2026 | https://cloudjourney.awsstudygroup.com/ |
| Wed | - Research Amazon API Gateway (REST APIs vs. HTTP APIs) <br> - Design simple HTTP endpoints, paths, query string inputs, and method mappings (GET/POST) | 05/06/2026 | 05/06/2026 | https://cloudjourney.awsstudygroup.com/ |
| Thu | - Configure an API Gateway route to natively proxy incoming traffic directly into a Lambda function <br> - Grant Lambda necessary IAM roles to read and write records inside DynamoDB | 05/07/2026 | 05/07/2026 | https://cloudjourney.awsstudygroup.com/ |
| Fri | - Perform end-to-end sandbox endpoint verification using API client utilities (Postman) <br> - Analyze data flow execution times and compile basic throughput metrics | 05/08/2026 | 05/08/2026 | https://cloudjourney.awsstudygroup.com/ |

---

### Week 3 Achievements:

#### 1. Managed NoSQL Architecture
* Mastered **Amazon DynamoDB** provisioning models, item structures, and data types.
* Created scalable, schema-less test tables utilizing composite primary keys, enabling multi-dimensional querying paths essential for transaction histories.

#### 2. Synchronous RESTful Integrations
* Acquired a strong grasp of **Amazon API Gateway** execution mechanisms, request integration mappings, and error status overrides.
* Successfully built a fully operational 3-tier serverless pipeline: API Gateway safely handles external HTTP client requests, proxies data into a computing Lambda function, which systematically queries and writes records directly to a DynamoDB storage backend.