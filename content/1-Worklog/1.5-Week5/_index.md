---
title: "Worklog Week 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:
- Study advanced concepts in Amazon DynamoDB modeling, specifically Single-Table Design.
- Understand Global Secondary Indexes (GSIs) and Local Secondary Indexes (LSIs).
- Map complex domain relationships (One-to-Many, Many-to-Many) onto a single NoSQL table.
- Formulate the initial data dictionary for the AWS BILLO core engine.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| Mon | - Work on-site at the company office <br> - Brainstorm data relationships for users, commercial merchants, physical stores, and ledger balances | 05/18/2026 | 05/18/2026 | Company office |
| Tue | - Study Single-Table Design theoretical frameworks pioneered by industry specialists <br> - Learn how generic partition keys (`PK`) and sort keys (`SK`) replace dedicated collections | 05/19/2026 | 05/19/2026 | DynamoDB Documentation |
| Wed | - Design access patterns for retrieving single store listings, user wallets, and complete transaction filters <br> - Draft an entity relationship mapping chart within spreadsheet modeling tools | 05/20/2026 | 05/20/2026 | DynamoDB Documentation |
| Thu | - Implement and configure Global Secondary Indexes (GSIs) to enable inverted lookups across entities <br> - Analyze overloading concepts where a single index serves distinct query requirements | 05/21/2026 | 05/21/2026 | DynamoDB Documentation |
| Fri | - Present the finalized access pattern matrix to the project mentor for operational review <br> - Optimize partition distribution strategies to mitigate hot-partition throttling concerns | 05/22/2026 | 05/22/2026 | Company office |

---

### Week 5 Achievements:

#### 1. Single-Table Design Strategy
* Successfully mastered advanced **NoSQL Modeling** through Single-Table Design paradigms, shifting away from relational databases to minimize multi-table join computational overhead.
* Created an internal documentation matrix containing over 15+ target application access patterns, ensuring efficient $O(1)$ or $O(\log N)$ data lookups.

#### 2. Index Overloading & Throughput Security
* Configured highly flexible **Global Secondary Indexes (GSIs)** leveraging key overloading, enabling lookups across fields like `StoreId`, `TransactionDate`, or `MerchantStatus` within a singular data store.
* Mitigated operational data bottlenecks by structuring uniform partition distribution strategies across high-velocity transactional nodes.