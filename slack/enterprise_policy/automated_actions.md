---
description: >-
  Learn the process of configuring automated actions while creating a Nightfall
  policy for the Slack Enterprise edition.
---

# Configure Automated Actions in Slack Enterprise

This section describes the various actions that Nightfall takes automatically when a violation is detected. You must turn on the toggle switch to enable an action. You can also set the timeline as to when an action must be taken (immediately after detecting a violation or after some time).

Currently, Nightfall supports the **Delete Message**, **Delete File**, **Quarantine**, and **Redact** automated actions for the Slack enterprise edition.&#x20;

You must first turn on the toggle switch to enable any of the automated actions.

Once you enable the toggle switch, you can configure when the action must be applied.&#x20;

If you select **immediately**, the action is implemented automatically after the sensitive data is detected.&#x20;

If you select **After**, you must also set the time frame as to when exactly the action must be applied, after detecting the sensitive data.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

The available actions are described as follows.

## Delete Message

The delete action automatically deletes the message that contains sensitive data. This is a permanent action and cannot be reverted.&#x20;

## Delete File

The delete action automatically deletes the attachment(s) that contains sensitive data. This is a permanent action and cannot be reverted.&#x20;

## Redact

The Redact action replaces the sensitive data with an asterisk, except for the first two characters. This is a permanent action and cannot be reverted.&#x20;

## Quarantine

When a message is quarantined, there is a new message in the quarantine alert channel (`nightfall-quarantine-slack` by default). This channel notifies that a new quarantine message is generated. The actual message or attachment is deleted from the original channel and added to the quarantine content channel (`nightfall-content-slack` by default). When a Slack message is Quarantined, Slack Workspace administrator must review the Quarantined messages and take one of the following actions:

* **Accept:** If the message is accepted in the notification quarantine channel (`nightfall-quarantine-slack` by default), it is deleted from the content channel (`nightfall-content-slack` by default) and sent to the original recipient channel.&#x20;
* **Reject**: If the message is rejected from the notification quarantine channel (`nightfall-quarantine-slack` by default), it is deleted forever from the content channel (`nightfall-content-slack` by default). &#x20;





&#x20;
