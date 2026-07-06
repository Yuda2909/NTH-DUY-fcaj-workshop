---
title: "Worklog Week 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:
- Implement a continuous delivery pipeline (CI/CD) to automate serverless application deployments.
- Build systematic pipeline definitions inside GitHub Actions platforms.
- Set up unit testing workflows across backend functions and client apps.
- Implement specialized environmental variable configurations separating production from dev scopes.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| Mon | - Work on-site at the company office <br> - Design secure deployment pipeline security patterns with the team lead | 06/29/2026 | 06/29/2026 | Company office |
| Tue | - Set up unit testing engines (Jest for backend Node.js modules; native Flutter test tools for clients) <br> - Write code assertion logic targeting core computational math routines | 06/30/2026 | 06/30/2026 | Jest & Flutter Docs |
| Wed | - Author declarative pipeline execution files (`.github/workflows/deploy.yml`) <br> - Configure lint checks, testing verifications, and automated build phases | 07/01/2026 | 07/01/2026 | GitHub Actions Manuals |
| Thu | - Set up OpenID Connect (OIDC) identities to securely authenticate GitHub runners into AWS without static access keys <br> - Automate multi-environment stack deployments | 07/02/2026 | 07/02/2026 | AWS Security Manuals |
| Fri | - Run end-to-end continuous integration pipeline simulations by issuing merge events <br> - Audit pipeline log records to identify and clean up slow build execution blocks | 07/03/2026 | 07/03/2026 | GitHub Actions Manuals |

---

### Week 11 Achievements:

#### 1. Continuous Automation (CI/CD)
* Built a production-grade **CI/CD pipeline utilizing GitHub Actions**, eliminating manual deployment bottlenecks across the development ecosystem.
* Secured automated runner configurations by deploying **OIDC token exchanges**, completely eliminating the need to store long-lived static AWS root access credentials within third-party environments.

#### 2. Test Enforcement & Quality Assurance
* Implemented systematic testing workflows running automated test assertions on every code modification request.
* Set up isolated environment staging setups (`dev`, `staging`), enabling safe, risk-free preview validation of backend features.