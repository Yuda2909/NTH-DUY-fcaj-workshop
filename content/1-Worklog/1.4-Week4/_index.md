---
title: "Worklog Week 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Week 4 Objectives:
- Deep-dive into secure networking concepts using Amazon VPC (Virtual Private Cloud).
- Understand Subnets, Internet Gateways, NAT Gateways, Route Tables, and Security Groups.
- Research modern Flutter application design architecture and native state management frameworks.
- Prepare structural requirements for integrating Flutter cross-platform applications with remote backends.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| Mon | - Work on-site at the company office <br> - Present isolated networking proposals for enterprise client connections and secure backend microservices | 05/11/2026 | 05/11/2026 | Company office |
| Tue | - Study Amazon VPC structural anatomy: isolate public subnets from private compute subnets <br> - Practice configuring Network Access Control Lists (NACLs) and inbound/outbound Security Groups | 05/12/2026 | 05/12/2026 | https://cloudjourney.awsstudygroup.com/ |
| Wed | - Review Flutter state management alternatives (Bloc, Provider, Riverpod) <br> - Build a clean interface mockup containing user registration screens and text entry validations | 05/13/2026 | 05/13/2026 | Flutter Documentation |
| Thu | - Research networking models in Flutter using `dio` and `http` abstract client packages <br> - Implement client-side exception handling layers for flaky network scenarios | 05/14/2026 | 05/14/2026 | Flutter Documentation |
| Fri | - Test local Flutter mock interactions alongside dummy mock data states <br> - Document architectural guidelines for secure communications between mobile applications and AWS API Gateway | 05/15/2026 | 05/15/2026 | https://cloudjourney.awsstudygroup.com/ |

---

### Week 4 Achievements:

#### 1. Isolated Cloud Networking
* Understood how to construct an **Amazon VPC** network topology, creating multi-AZ public and private subnets.
* Configured stateful **Security Groups** acting as firewalls to tightly control entry rules, ensuring data-tier nodes remain completely inaccessible from the public web.

#### 2. Client-Side Engineering & Network Specifications
* Successfully designed an extensible UI baseline using **Flutter**, incorporating input validation layers for registration screens.
* Established standardized networking abstractions using the `dio` ecosystem, prepping the application for seamless authentication token interceptors and production API usage.