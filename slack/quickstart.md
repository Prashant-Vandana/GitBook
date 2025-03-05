---
description: >-
  Learn how to set up your integration with Slack so that you can scan and
  protect sensitive data across your Slack workspace.
---

# Nightfall for Slack: Quick Start

Welcome to Nightfall! This guide is intended to help you install and set up Nightfall in a matter of minutes on your own. Within 24 hours of you signing on to be a customer, you will receive an invitation in your inbox to access your newly created account.

Once you receive your account, review the following pages in this guide to get set up.

## **Installation**

Get ready to install by reviewing the [Requirements](getting_started/requirements/). Go through the installation flow, depending on your Slack plan type:

* [Slack Pro](getting_started/install/slack_pro.md)
* [Slack Enterprise ](getting_started/install/slack_enterprise.md)

## Configuring Detection

Next, use the Detection Wizard to set up the right Detection Rules for your organization in your Nightfall dashboard. You can learn more about and access the **Detection Wizard** [**here**](https://help.nightfall.ai/nightfall-ai/detection-engine/detectors).

Once you’ve generated your Detection Rules with the Wizard, configure them on your Nightfall Dashboard.

On the [Detection Rules page](https://app.nightfall.ai/detection-engine/detection-rules), copy the Detection Rule UUIDs that you wish to use for DLP scanning.

## **Configuring Policies**

**Configuring a policy, review the Configuring Policies**[ ](slack_pro_policy/)**section, including:**

1. How to [create a policy](https://help.nightfall.ai/sensitive-data-protection/slack/slack_pro_policy)
2. Defining the policy [scope](https://help.nightfall.ai/sensitive-data-protection/slack/slack_pro_policy/scope)
3. Selecting [detection rules ](https://help.nightfall.ai/sensitive-data-protection/slack/slack_pro_policy/detection_rules)that you configured above
4. Determining what [automated actions](https://help.nightfall.ai/sensitive-data-protection/slack/slack_pro_policy/automated_actions) you would like to take
5. Configuring the [advanced settings](https://help.nightfall.ai/sensitive-data-protection/slack/slack_pro_policy/advanced_settings).
6. [Risk configuration ](https://help.nightfall.ai/sensitive-data-protection/slack/slack_pro_policy/policy_risk)and policy nomenclature

## Configuring Alerts

Nightfall allows multiple methods of receiving alerts, via Slack, email, webhooks, or Jira tickets. Review the Configuring Alerts section to learn more.

## Test Detection

To confirm that sensitive data is getting scanned by Nightfall, you can run a few tests with Nightfall-provided sample data. In doing so, you will see Violations populate on the Nightfall dashboard on [the Violations page](https://app.nightfall.ai/violations). You'll also start to see high-level metrics aggregate on [the Nightfall Dashboard page](https://app.nightfall.ai/dashboard).

To test detection, we recommend the following tutorials:

1. [Learn How Detection Works](../detection_platform/overview_platform.md)
2. [Use Sample Data from the Nightfall Library to Test Detection](../nightfall_policy_templates/sample_data.md)
3. [Learn How to Evaluate Detection Results](../detection_platform/evaluate_nightfall_detection.md)

**Congratulations - you are all set up. You’ve now successfully connected and tested Nightfall for Slack!**&#x20;

If you have any questions, check out the[ Frequently Asked Questions ](slack-faqs/)section for support.

