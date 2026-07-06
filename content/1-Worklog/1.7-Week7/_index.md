---
title: "Worklog Week 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives:
- Research user management, federated directory services, and secure web token lifecycles.
- Deep-dive into Amazon Cognito User Pools and Identity Pools.
- Map out multi-tenant security requirements and onboarding workflows for AWS BILLO.
- Learn OAuth 2.0 and JSON Web Token (JWT) verification steps.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| Mon | - Work on-site at the company office <br> - Participate in structural reviews on access security, session expiry durations, and custom user properties | 06/01/2026 | 06/01/2026 | Company office |
| Tue | - Study Amazon Cognito User Pools configuration settings: user attributes, password complexity profiles, and MFA choices | 06/02/2026 | 06/02/2026 | Cognito Documentation |
| Wed | - Analyze custom authentication flows (Define Auth Challenge, Create Auth Challenge, Verify Auth Challenge Response) | 06/03/2026 | 06/03/2026 | Cognito Documentation |
| Thu | - Map custom claims into JWT access tokens to support complex platform roles <br> - Understand token anatomy, verifying payload signatures against target JWKS endpoints | 06/04/2026 | 06/04/2026 | Cognito Documentation |
| Fri | - Build structural sequence flows outlining signup verification states for customers and merchants <br> - Conduct technical walkthroughs with team leads on the chosen identity approach | 06/05/2026 | 06/05/2026 | Company office |

---

### Week 7 Achievements:

#### 1. Enterprise Identity Architecture
* Acquired an advanced operational understanding of **Amazon Cognito**, focusing on secure account onboarding, data separation, and sign-in operations.
* Developed sequence workflows for phone-number-based, passwordless authentication utilizing custom text-delivery challenges.

#### 2. Token-Based Security Frameworks
* Mastered **JSON Web Token (JWT)** anatomy (`id_token`, `access_token`, `refresh_token`), including cryptography signature enforcement routines.
* Designed the logical structural schema for embedding access claims into tokens to streamline Role-Based Access Control (RBAC).