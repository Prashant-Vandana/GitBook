---
description: Learn how you can get started with the Nightfall DLP for GenAI apps.
---

# Overview

Nightfall DLP plugin for browsers can ensure security and compliance when using GenAI apps. You can install this plugin on the **Google Chrome,** any **chromium** based browser, and **Mozilla Firefox**. &#x20;

Once you install the browser plugin you can:

* Configure policies with granular detection rules, detector tuning, and custom detectors
* Create and enforce tenant-specific policies using pre-built detectors
* Enable the safe use of GenAI apps instead of blocking employee productivity&#x20;

The plug in can detect over 100 sensitive data types using Nightfall’s industry-leading ML-trained detectors. It automatically detects PII, PCI, PHI, secrets, and credentials including API keys and certificates, and keeps your data compliant with industry frameworks like ISO-27001, SOC 2, and HIPAA.

The plugin also redacts sensitive data before it’s proliferated into LLMs like OpenAI by intercepting sensitive PII, PCI, PHI before the information is submitted through real-time, end-user remediation.

## Supported GenAI Apps

Nightfall DLP supports the following GenAI apps.&#x20;

* [ChatGPT](https://chatgpt.com/)
* [Microsoft Copilot ](https://copilot.microsoft.com/)
* [Google Gemini](https://gemini.google.com/)
* [DeepSeek AI](https://www.deepseek.com/)
* [Claude](https://claude.ai/new)
* [Grok](https://grok.com/)
* [Perplexity AI](https://www.perplexity.ai/)

{% hint style="info" %}
Important:

* In case of ChatGPT, Nightfall provides a built in integration. You can use this integration to create policies for ChatGPT to monitor specific type of sensitive data based on detection rules, view policy violations in Nightfall and assess the risk score for each of the violation.&#x20;
* Any policy created for the ChatGPT integration IS APPLICABLE to other GenAI apps as well. For instance, if you create a policy in ChatGPT to monitor if API keys are being used in ChatGPT and if an user uses an API key in Claude, Perplexity, or any other GenAI app, Nightfall can still detect and alert the user.&#x20;
{% endhint %}

You can monitor violations from the Nightfall console, receive automated alerts to Slack, email, or SIEM of choice, and receive context-rich alerts and remediate violations in real time.

* [installation](installation/ "mention")
* [policies](policies/ "mention")
