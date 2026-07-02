---
title: "Event 2"
date: 2026-06-06
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

## Event Objectives

- Introduce the critical importance of Prompt Engineering in optimizing the output quality of Large Language Models.
- Provide a standardized framework and core components to construct effective prompts.
- Share advanced prompting methodologies and strategies for optimizing token expenses during AI workloads.
- Demonstrate a practical production-ready AWS serverless architecture through the **Proptimizer** application.

---

## Speaker Lineup

- **Bao Huynh** - Junior Cloud Native Developer, Endava Vietnam
- **Le Hoang Gia Dai**
- **Nguyen Quoc Bao**
- **Truong Huy Phuoc**
- **Viet Phat** - AI Majoring at Swinburne University of Technology
- **Tran Trung Vinh** - System Administrator at Central Retail Group

---

## Key Highlights

### 1. The Core Philosophy of Prompt Engineering

Prompt engineering goes beyond simply typing messages. It is the process of structuring the way users communicate with AI models so that the model can understand the task, context, constraints, and expected output more accurately.

Without methodical prompts, users may face several problems:

- **Generic prompts** lead to vague and low-utility responses.
- **Wasted tokens** increase operational cost.
- **Ambiguous instructions** produce inconsistent outputs.
- **Poor communication** reduces productivity and increases rework.

---

### 2. Anatomy of an Effective Prompt

To improve the output quality of an LLM, a prompt should include seven fundamental components:

- **Role**: Defines the persona or professional perspective that the model should take.
- **Instruction**: States the specific task that the model needs to complete.
- **Context**: Provides necessary background and situational boundaries.
- **Input Data**: Supplies the raw information or content that needs to be processed.
- **Output Format**: Defines the expected response structure, such as JSON, Markdown, table, or summary.
- **Examples**: Provides few-shot examples for the model to follow.
- **Constraints/Guidelines**: Sets clear rules, limitations, tone, and things to avoid.

---

### 3. Advanced Prompting Methodologies

The session introduced several advanced prompting methods:

- **Chain-of-Thought (CoT)**: Guides the model to reason step by step before producing the final answer.
- **Self-Consistency**: Runs multiple reasoning paths and selects the most consistent result.
- **Tree-of-Thoughts (ToT)**: Allows the model to explore multiple reasoning branches and evaluate different possible solutions.
- **RAG (Retrieval-Augmented Generation)**: Combines external information retrieval with LLM text generation.
- **Role Prompting**: Assigns a specific identity to control the tone, vocabulary, and style of the response.

---

### 4. Understanding Token Economics

The event also explained the importance of token economics when using AI models.

Key points include:

- LLMs process text using tokens, which are often subword chunks rather than full words.
- Token consumption can vary between languages.
- Vietnamese may require more tokens than English for the same meaning.
- Writing concise and structured prompts helps reduce cost.
- Token cost should be considered before integrating AI into production systems.

---

### 5. Practical Implementation: Proptimizer Architecture

The speakers showcased **Proptimizer**, a browser extension that automates prompt engineering and supports flexible AI interaction on any webpage.

The application is built on AWS serverless architecture, including:

- **CloudFront and Amazon S3** for frontend delivery.
- **Amazon Cognito** for authentication.
- **Amazon API Gateway** for routing backend requests.
- **AWS Lambda** for serverless backend logic.
- **Amazon Bedrock** for AI model integration.
- **Amazon DynamoDB** for data storage.
- **Amazon CloudWatch** for logs and monitoring.

The architecture demonstrates how an AI application can be designed with low infrastructure cost while still being scalable and maintainable.

---

## Key Takeaways and Personal Reflections

### Recalibrating My AI Interaction Framework

This session changed the way I think about prompt engineering. I learned that the quality of AI output depends heavily on the clarity of the input. Instead of writing casual one-line prompts, I should provide clear roles, context, constraints, and output formats.

This approach can save time because it reduces the number of repeated attempts needed to correct poor AI responses.

### Real-World Cloud and Serverless Validation

The highlight of the event was seeing a theoretical cloud architecture turned into a real AI browser extension.

Proptimizer showed how AWS serverless services can support a practical AI product. The combination of CloudFront, S3, API Gateway, Lambda, Bedrock, DynamoDB, Cognito, and CloudWatch provides a strong reference architecture for future AI applications.

---

## Professional Application Plan

After this event, I can apply the knowledge in the following ways:

- **Use structured prompt templates** for coding, debugging, and technical documentation.
- **Apply Chain-of-Thought prompting** for complex analysis tasks.
- **Estimate token usage and cost** before using AI in production.
- **Use serverless architecture patterns** such as CloudFront + S3 + API Gateway + Lambda for future applications.
- **Refer to Proptimizer’s architecture** when designing AI applications on AWS.
- **Improve teamwork with AI** by using consistent prompt formats across team members.

---

## Conclusion

The June 6th event provided valuable knowledge in two areas: advanced Prompt Engineering and modern serverless application design on AWS.

It helped me understand how to communicate with AI more effectively and how to design AI-powered systems using cost-optimized AWS services.
