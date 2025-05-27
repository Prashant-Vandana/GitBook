---
description: Learn how to create a policy for ChatGPT apps from within Nightfall.
---

# Creating GenAI Policies from Nightfall Console

Once you install the GenAI app, you must create policies in Nightfall to monitor the prompts being sent to Gen AI apps.&#x20;

The policy creation involves the following stages.

[integration.md](integration.md "mention")

[detection\_rules.md](detection_rules.md "mention")

[advanced\_settings.md](advanced_settings.md "mention")

[risk\_score.md](risk_score.md "mention")

{% hint style="warning" %}
**Important**

* In Copilot, Nightfall does not automatically redact the sensitive data present in your prompts. Nightfall identifies the sensitive data in your prompt. You must either manually redact the sensitive data before submitting the prompt to Copilot or provide a justification as to why the data is not sensitive in nature.
* In Claude AI, Nightfall only monitors the AI application; if you submit a prompt with sensitive data, it is neither redacted nor identified. However, a Nightfall Event is generated in the Nightfall Events page and the notifications (if configured) are sent to the stakeholders.   &#x20;
{% endhint %}

