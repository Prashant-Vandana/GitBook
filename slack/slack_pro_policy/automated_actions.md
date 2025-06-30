---
description: >-
  Learn the process of configuring automated actions in the Slack Pro and
  Business+ editions while creating a Nightfall policy.
---

# Configure Automated Actions in Slack Pro and Slack Business+

This section describes the various actions that Nightfall automatically takes when a violation is detected. To enable an action, you must turn on the toggle switch. Additionally, you can set a timeline for when the action should be taken—either immediately after detecting a violation or after a specified delay.

Currently, Nightfall supports the **Delete Message** and **Delete File** automated actions for the Slack Pro and Business+ editions.

To enable any of the automated actions, you must first turn on the toggle switch. Once the toggle switch is enabled, you can configure the timing for the action. If you select **immediately**, the action is executed as soon as sensitive data is detected.&#x20;

<figure><img src="../../.gitbook/assets/image (3) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

If you select **After**, you must also set the time frame when the action must be applied, after detecting the sensitive data.

<figure><img src="../../.gitbook/assets/image (895).png" alt=""><figcaption></figcaption></figure>

The actions are described as follows.

## Delete Message

This action automatically deletes the Slack message that contains sensitive data.&#x20;

## Delete File

This action automatically deletes the Slack attachments that contains sensitive data.&#x20;
