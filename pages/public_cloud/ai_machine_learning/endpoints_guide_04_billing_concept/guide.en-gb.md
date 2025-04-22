---
title: AI Endpoints - Billing and lifecycle
excerpt: Learn how we bill AI Endpoints
updated: 2025-04-28
---

> [!primary]
>
> AI Endpoints is covered by the **[OVHcloud AI Endpoints Conditions](https://storage.gra.cloud.ovh.net/v1/AUTH_325716a587c64897acbef9a4a4726e38/contracts/48743bf-AI_Endpoints-ALL-1.1.pdf)** and the **[OVHcloud Public Cloud Special Conditions](https://storage.gra.cloud.ovh.net/v1/AUTH_325716a587c64897acbef9a4a4726e38/contracts/d2a208c-Conditions_particulieres_OVH_Stack-WE-9.0.pdf)**.
>

## Introduction

[AI Endpoints](https://endpoints.ai.cloud.ovh.net/) is a serverless platform provided by OVHcloud that offers easy access to a selection of world-renowned, pre-trained AI models. The platform is designed to be simple, secure, and intuitive, making it an ideal solution for developers who want to enhance their applications with AI capabilities without extensive AI expertise or concerns about data privacy.

## Objective

This documentation provides an overview of the billing and lifecycle management of various AI model categories offered on [AI Endpoints](https://endpoints.ai.cloud.ovh.net/). We will cover the cost structure for Large Language Models (LLM), Audio models, Image models, Embedding models, and more. Additionally, we will explain the lifecycle of our models, including decommissioning, redirection, on our website, ensuring that you have all the necessary information to manage your AI Endpoints effectively.

## AI Endpoints model lifecycle

OVHcloud AI Endpoints follows a model lifecycle process to ensure a seamless experience for our customers. This process includes the following steps:

- **Track model usage metrics**: We continuously monitor the usage of each model on our platform to identify underutilized or obsolete models that may no longer serve the needs of our customers.
- **Decommissioning decision**: Once a model is identified as a candidate for decommissioning, we make a decision to retire the model. At this point, we communicate the decision to our customers through official deprecation notices on our website and the #ai-endpoints channel of the OVHcloud [Discord server](https://discord.gg/ovhcloud).
- **Grace period**: After the deprecation notice is published, a grace period of 30 days is provided for all models except embedding models, which will have a grace period of 3 months. This period allows customers to transition to an alternative model. During this time, we offer guidance on recommended replacements and migration steps to ensure a smooth transition.
- **Removal from active deployment**: Once the grace period ends, the model is removed from active deployment. However, to ensure continuity, we may redirect API calls to the replacement model (if applicable) with a 10-second delay before the decommissioned model responds, signaling to users that the model is no longer in active use.
- **AI Endpoints changelog**: Decommissionings are highlighted in the [AI Endpoints Changelog](https://endpoints.ai.cloud.ovh.net/changelog), ensuring that customers are informed about the changes in the platform.

By following this model lifecycle process, OVHcloud ensures that customers are well-informed and prepared for any changes, while also maintaining a lean and up-to-date selection of AI models.

## Billing principles

Here is the model billing overview for AI Endpoints.

> [!primary]
>
> Please note that, as we are currently in the beta phase, the product is free during this period. Once the product is officially launched, the pricing will be determined and communicated accordingly in the table below, which presents the categories, models, and their respective pricing information:
>

| Category        | Model            | Price ($)  | Price (€)  | Unit Price |
| -------------- | --------------- | ------ | ------ | ---------- |
| Large Language Model (LLM)            | Llama 3.3 70B Instruct          | 0.70   | 0.67   | per 1M tokens          |
| Large Language Model (LLM)            | Llama 3.1 70B Instruct          | 0.70   | 0.67   | per 1M tokens          |
| Large Language Model (LLM)            | Mixtral 8x7B Instruct v0.1         | 0.65   | 0.63   | per 1M tokens          |
| Large Language Model (LLM)            | Mistral-Nemo-Instruct-2407          | 0.14   | 0.13   | per 1M tokens          |
| Large Language Model (LLM)            | Llama 3.1 8B Instruct          | 0.10   | 0.10   | per 1M tokens          |
| Large Language Model (LLM)            | Mistral 7B Instruct v0.3          | 0.10   | 0.10   | per 1M tokens          |
| Reasoning LLM   | DeepSeek R1         | Free   | Free   | per 1M tokens          |
| Reasoning LLM   | DeepSeek R1 Distill Llama 70B          | 0.70   | 0.67   | per 1M tokens          |
| Code LLM        | Qwen2.5 Coder 32B Instruct          | 0.90   | 0.87   | per 1M tokens          |
| Code LLM        | Mamba Codestral 7B v0.1          | 0.20   | 0.19   | per 1M tokens          |
| Visual LLM      | Qwen2.5 VL 72B Instruct         | 0.95   | 0.91   | per 1M tokens          |
| Visual LLM      | Llava Next Mistral 7B          | 0.30   | 0.29   | per 1M tokens          |
| Embeddings     | BGE Multilingual Gemma2          | 0.01   | 0.01   | per 1M tokens          |
| Embeddings     | BGE-M3          | 0.01   | 0.01   | per 1M tokens          |
| Embeddings     | BGE Base EN v1.5          | 0.01   | 0.005   | per 1M tokens          |
| Natural Language Processing (NLP)            | Roberta Base Go Emotions          | Free   | Free   | per 1M characters          |
| Natural Language Processing (NLP)            | Bert Base Multilingual uncased sentiment          | Free   | Free   | per 1M characters          |
| Natural Language Processing (NLP)            | Bert Base NER          | Free   | Free   | per 1M characters          |
| Natural Language Processing (NLP)            | Bart Large CNN          | Free   | Free   | per 1M characters          |
| Image generation| Stable Diffusion XL          | Free   | Free   | per image          |
| Speech to Text  | RIVA Automatic Speech Recognition          | Free   | Free   | per hour          |
| Text to Speech  | RIVA Text-to-Speech          | Free   | Free   | per hour          |
| Translation    | T5-Large          | Free   | Free   | per 1M characters          |
| Computer vision | YOLOv11 Object Detection          | Free   | Free   | per image          |
| Computer vision | YOLOv11 Image Segmentation          | Free   | Free   | per image          |

## Feedback

Please send us your questions, feedback and suggestions to improve the service:

- On the OVHcloud [Discord server](https://discord.gg/ovhcloud)

If you need training or technical assistance to implement our solutions, contact your sales representative or click on [this link](/links/professional-services) to get a quote and ask our Professional Services experts for a custom analysis of your project.