---
title: AI Endpoints - Create a code assistant with Continue
excerpt: Build your own code assistant directly in VSCode or JetBrains IDEs using the Continue plugin
updated: 2025-04-28
---

> [!primary]
>
> AI Endpoints is covered by the **[OVHcloud AI Endpoints Conditions](https://storage.gra.cloud.ovh.net/v1/AUTH_325716a587c64897acbef9a4a4726e38/contracts/48743bf-AI_Endpoints-ALL-1.1.pdf)** and the **[OVHcloud Public Cloud Special Conditions](https://storage.gra.cloud.ovh.net/v1/AUTH_325716a587c64897acbef9a4a4726e38/contracts/d2a208c-Conditions_particulieres_OVH_Stack-WE-9.0.pdf)**.
>

## Introduction

Want more control over your code assistant? Looking to integrate your own LLM configuration and use models hosted on **[AI Endpoints](https://endpoints.ai.cloud.ovh.net/)**?

This tutorial shows you how to build your own developer assistant using **[Continue](https://www.continue.dev/)**, an open-source IDE plugin that works with both VSCode and JetBrains IDEs, in combination with OVHcloud.

Continue lets you plug in your own LLMs, enabling full control over which models you use and how they interact with your code.

## Requirements

- A [Public Cloud project](/links/public-cloud/public-cloud) in your OVHcloud account
- An access token for **OVHcloud AI Endpoints**. To create an API token, follow the instructions in the [AI Endpoints - Getting Started](/pages/public_cloud/ai_machine_learning/endpoints_guide_01_getting_started) guide.

## Instructions

### Install Continue

Continue is distributed as an IDE plugin and supports:

- Visual Studio Code
- JetBrains IDEs (e.g. IntelliJ, PyCharm)

Follow the [official Continue installation instructions](https://docs.continue.dev/docs/getting-started/install) for your IDE.

Once installed, Continue will share the same configuration across your IDEs.

### Configure Continue with AI Endpoints

Continue uses a JSON-based configuration file to manage:

- Chatbot tool models
- Tab autocomplete models

You can customize this configuration file to connect the plugin to AI Endpoints:

```json
{
  "tabAutocompleteModel": {
    "title": "Qwen2.5-Coder-32B-Instruct",
    "model": "Qwen2.5-Coder-32B-Instruct",
    "apiBase": "https://qwen-2-5-coder-32b-instruct.endpoints.kepler.ai.cloud.ovh.net/api/openai_compat/v1",
    "provider": "openai",
    "useLegacyCompletionsEndpoint": true,
    "apiKey": "<your API key>"
  },
  "models": [
    {
      "title": "Meta-Llama-3_3-70B-Instruct",
      "model": "Meta-Llama-3_3-70B-Instruct",
      "apiBase": "https://llama-3-3-70b-instruct.endpoints.kepler.ai.cloud.ovh.net/api/openai_compat/v1",
      "provider": "openai",
      "useLegacyCompletionsEndpoint": false,
      "apiKey": "<your API key>"
    },
    {
      "title": "Qwen2.5-Coder-32B-Instruct",
      "model": "Qwen2.5-Coder-32B-Instruct",
      "apiBase": "https://qwen-2-5-coder-32b-instruct.endpoints.kepler.ai.cloud.ovh.net/api/openai_compat/v1",
      "provider": "openai",
      "useLegacyCompletionsEndpoint": false,
      "apiKey": "<your API key>"
    }
  ] 
  // ... 
}
```

### Tab Completion Configuration

You can define only one model for tab autocomplete. Choose any model from the Code LLM category in AI Endpoints. Here's a quick example:

```json
{
  "tabAutocompleteModel": {
    "title": "Qwen2.5-Coder-32B-Instruct",
    "model": "Qwen2.5-Coder-32B-Instruct",
    "apiBase": "https://qwen-2-5-coder-32b-instruct.endpoints.kepler.ai.cloud.ovh.net/api/openai_compat/v1",
    "provider": "openai",
    "useLegacyCompletionsEndpoint": true,
    "apiKey": "<your API key>"
  }
}
```

### Chatbot Configuration

For the chatbot tool, you can define multiple models. Try out different LLMs and choose the one that best fits your use case. You can switch between them easily in the IDE UI.

### Try It Out

Once Continue is configured with your AI Endpoints, you're ready to test both features:

**Chatbot Tool**

Use the chatbot sidebar to ask for help, generate code, or refactor logic with any of your configured models.

![image](images/chatbot.gif){.thumbnail}

**Tab Completion Tool**

Just start typing in your editor. The autocomplete model will complete code as you go — powered by your custom-configured model from AI Endpoints.

![image](images/tab-completion.gif){.thumbnail}

## Conclusion

By using Continue and AI Endpoints, you now have access to a fully customizable code assistant, support for cutting-edge open-source large language models such as Qwen, Mixtral, and LLaMA 3, and the ability to manage your own configuration and resources on AI Endpoints.

If you need training or technical assistance to implement our solutions, contact your sales representative or click on [this link](/links/professional-services) to get a quote and ask our Professional Services experts for a custom analysis of your project.

## Feedback

Please feel free to send us your questions, feedback, and suggestions regarding AI Endpoints and its features:

- In the #ai-endpoints channel of the OVHcloud [Discord server](https://discord.gg/ovhcloud), where you can engage with the community and OVHcloud team members.
