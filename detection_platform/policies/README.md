---
description: Learn how to create policies in Nightfall.
---

# Creating Policies

{% hint style="info" %}
This document applies only to the Nightfall SaaS application customer. If you are a Nightfall Firewall for AI customer, refer to [this document](https://help.nightfall.ai/nightfall-developer-platform/getting-started-with-developer-platform/creating-policies).&#x20;
{% endhint %}

## Background Knowledge

An Integration in Nightfall refers to a SaaS application in which your organization's data resides. This SaaS application can be Google Drive, JIRA, Notion, GitHub, and so on. The sensitive data residing in these applications is highly prone to data leakage, accidentally by your employees.

You can connect your SaaS applications to Nightfall by adding them as integrations. Once a SaaS application is added as an integration, Nightfall continuously scans it to check if there is any sensitive data leakage.

## Understanding Policies

A Policy in Nightfall allows you to define a specific part of your integration or the entire integration to be monitored for sensitive data leakage, by Nightfall. Apart from monitoring your environment, Policies in Nightfall also allow you to configure alerts and automatic actions if Nightfall discovers sensitive information in the integration being scanned.&#x20;

Once you create a policy, if there is any instance of data leakage, Nightfall sends notifications to the audience configured by you in the policy. It also takes automated actions, configured by you in the policy. If you have disabled automated actions and no action is taken by you, Nightfall also sends reminders, as per the frequency set by you in the policy. All these actions are done automatically by Nightfall, as per the policy settings, configured by you.&#x20;

A Policy in Nightfall is always associated with integration. You can create multiple policies on a single integration. Before creating a policy for an integration, you must first ensure that the integration is added to Nightfall.

## Policy Stages

A Nightfall Policy has multiple stages. You can configure various settings like adding specific sections of integration to be scanned, configuring alert notifications, end-user actions, and so on. The various stages of a policy are described in the following document.

[integration.md](integration.md "mention")

[scope.md](scope.md "mention")

[detection\_rules.md](detection_rules.md "mention")

[advanced\_settings.md](advanced_settings.md "mention")

[risk\_score.md](risk_score.md "mention")

