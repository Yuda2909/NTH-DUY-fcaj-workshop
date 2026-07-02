---
title: "Event 1"
date: 2026-05-09
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

## Event Objectives

- Introduce the importance of Prompt Engineering in improving the output quality of Large Language Models.
- Explain how to build an effective prompt with the necessary components.
- Introduce advanced prompting techniques and cost optimization concepts when using AI.
- Demonstrate **Proptimizer**, a browser extension that automatically optimizes user prompts.

---

## Speaker Lineup

- **Huỳnh Hoàng Long** - Admin of FCAJ
- **Nguyễn Tuấn Thịnh** - DevOps/Cloud Engineer, First Cloud AI Journey
- **Khang Nguyen** - Solution Architect
- **Nguyễn Phương Thảo** - Application Cloud Dev

---

## Key Highlights

### Automated Prompt Engineering: Enhancing LLM Output Quality

The presentation by **Nguyễn Tuấn Thịnh** focused on how to write prompts effectively in order to maximize the capabilities of AI models. The session also introduced Proptimizer, a product built on AWS.

### Problems Caused by Poor Prompts

- Generic prompts lead to generic and low-value outputs.
- Wasted tokens increase operational cost.
- Unclear instructions produce inconsistent results.
- Poor communication with AI reduces productivity.

### Seven Components of an Effective Prompt

- **Role**: Defines the role that the model should take, such as career coach or senior developer.
- **Instruction**: Describes the specific task the model needs to perform.
- **Context**: Provides background information related to the problem.
- **Input Data**: Includes the data that needs to be processed.
- **Output Format**: Defines the expected structure or format of the result.
- **Examples**: Provides sample outputs or few-shot examples for the model to follow.
- **Constraints/Guidelines**: Sets rules such as word limits, writing style, or things to avoid.

### Principles of Writing Good Prompts

- Be clear and specific.
- Use directive language.
- Use delimiters to separate parts of the prompt.
- Describe what the model should do, not only what it should avoid.
- Avoid asking LLMs to perform exact arithmetic.
- Allow the model to say “I don’t know” instead of hallucinating.
- Break long input into smaller parts.

### Advanced Prompting Techniques

- **Chain-of-Thought (CoT)**: Encourages the model to reason step by step before answering.
- **Self-Consistency**: Runs multiple reasoning paths and selects the most consistent answer.
- **Tree-of-Thoughts (ToT)**: Explores multiple reasoning branches in parallel.
- **RAG (Retrieval-Augmented Generation)**: Combines external knowledge retrieval with text generation.
- **Role Prompting**: Assigns a specific role to guide tone, vocabulary, and response style.

### Token Economics

- Tokens are processing units used by LLMs.
- Tokens are not always the same as words; they can be subword units.
- Token usage differs by language, and Vietnamese may require more tokens than English for the same meaning.
- Concise and precise prompts help reduce AI operation cost.

### Proptimizer Product

Proptimizer is a browser extension that automatically optimizes user prompts and allows users to chat with AI directly on any website.

The architecture uses AWS services such as CloudFront and S3 for frontend hosting, Cognito for authentication, API Gateway and Lambda for backend logic, Amazon Bedrock for AI processing, DynamoDB for data storage, and CloudWatch for monitoring.

---

## What I Learned

### AI Interaction Mindset

- Prompting is communication, not just command input.
- Context strongly affects output quality.
- Shorter and more focused prompts can reduce cost and improve accuracy.

### Practical Techniques

- I learned how to apply the seven components of a prompt in real use cases.
- I understood the differences between CoT, Self-Consistency, and ToT.
- I realized that LLMs are not ideal for exact mathematical calculations and that such tasks should be handled by dedicated tools.

### Real Serverless Architecture

- I saw how a real AI product can be built on AWS serverless architecture.
- I understood the flow: User → CloudFront → API Gateway → Lambda → Bedrock → DynamoDB.
- I learned that AI applications can be built with low infrastructure cost by using AWS managed services properly.

---

## Professional Application

- Apply the seven prompt components to daily tasks such as coding, debugging, and documentation.
- Use Chain-of-Thought prompting for analysis tasks that require step-by-step reasoning.
- Estimate token cost before integrating AI into production systems.
- Refer to the Proptimizer architecture when designing serverless AI applications.
- Practice writing structured prompts to ensure consistent outputs in teamwork.

---

## Event Experience

Joining the **First Cloud AI Journey** event on May 9 was a practical and meaningful experience. The session was especially useful for people who use AI every day but have not fully understood how to communicate with AI effectively.

### New Perspective on Prompt Engineering

Before the event, I often wrote short prompts and accepted the results without much improvement. After the event, I understood that output quality depends directly on input quality. A prompt with clear role, context, and constraints can produce much better results than a vague question.

### Impression of Proptimizer

The Proptimizer demo impressed me because it turned prompt engineering theory into a real browser extension. The product also showed how AWS serverless services can support a real AI application with low infrastructure cost.

### Key Lessons

- Prompt Engineering is a practical communication skill that can be learned and improved.
- Token economics helps developers make better technical and financial decisions.
- Serverless architecture combined with managed AI services such as Amazon Bedrock is a practical direction for building AI products.

---

## Conclusion

Overall, the event not only provided theoretical knowledge but also demonstrated practical implementation through Proptimizer. It helped me change the way I approach AI and gave me a clearer direction for building AI applications on AWS.
