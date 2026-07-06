---
title: "Worklog Week 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:
- Research cloud-native infrastructure automation tools: AWS CloudFormation and AWS SAM.
- Understand the benefits of Infrastructure as Code (IaC) over manual console click-throughs.
- Author initial baseline templates defining basic serverless parameters.
- Establish unified code-driven local deployment pipelines.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| :--- | :--- | :--- | :--- | :--- |
| Mon | - Work on-site at the company office <br> - Align development standards around AWS SAM for rapid configuration, localized testing, and structured deployments | 05/25/2026 | 05/25/2026 | Company office |
| Tue | - Study AWS SAM template anatomy: globals, resources, outputs, and transform scopes <br> - Install the AWS SAM CLI suite on the development system | 05/26/2026 | 05/26/2026 | https://cloudjourney.awsstudygroup.com/ |
| Wed | - Build a basic `template.yaml` defining an isolated AWS Lambda runtime environment <br> - Execute local simulations using containerized runtime layers via docker utilities | 05/27/2026 | 05/27/2026 | https://cloudjourney.awsstudygroup.com/ |
| Thu | - Expand the SAM layout to include an integrated Amazon DynamoDB resource block <br> - Practice cloud deployment mechanisms using `sam build` and `sam deploy --guided` inputs | 05/28/2026 | 05/28/2026 | https://cloudjourney.awsstudygroup.com/ |
| Fri | - Debug initial cloud execution policies, template drift, and IAM mapping configurations <br> - Standardize environment runtime parameter options across standard deployment profiles | 05/29/2026 | 05/29/2026 | https://cloudjourney.awsstudygroup.com/ |

---

### Week 6 Achievements:

#### 1. Infrastructure as Code (IaC) Onboarding
* Transitioned the infrastructure management paradigm to **Infrastructure as Code (IaC)** using **AWS SAM**, guaranteeing predictable environment configurations.
* Installed, configured, and verified the AWS SAM CLI developer suite alongside Docker for local cloud runtime emulation.

#### 2. Declarative Resource Provisioning
* Authored clean, parameter-driven YAML descriptors deploying unified serverless modules.
* Successfully executed guided programmatic cloud deployments, tracking stack lifecycles and CloudFormation rollbacks cleanly from the terminal workspace.