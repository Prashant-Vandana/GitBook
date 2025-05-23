---
description: >-
  Learn how to configure the advanced settings section in Nightfall policies
  created for Notion.
---

# Configure Advanced Settings for Notion

This stage allows you to select notification channels if a policy violation occurs. The advanced settings page consists of the following configurations. &#x20;

[#admin-alerting](advanced_settings.md#admin-alerting "mention"): This section describes the process of setting alerts for Nightfall administrators when a policy violation is detected.

[#automated-actions](advanced_settings.md#automated-actions "mention"): This section describes the automated actions that can be taken when a policy violation is detected.

[#end-user-notification](advanced_settings.md#end-user-notification "mention"): This section describes the process of setting alerts for end users (a person whose action caused a violation) when a policy violation is detected.

## Admin Alerting

{% hint style="info" %}
The alert configurations configured in this section describe the process of creating alerts at the policy level. Policy-level alerts apply only to the policy on which they are configured. To configure an alert on all the Slack policies, you must configure alerts at the integration level. To learn more about how to configure integration-level policies for Slack integration, read [this document](https://help.nightfall.ai/nightfall-ai/notion/configuring-integration-alerts).
{% endhint %}

The steps to configure alert channels for policy-level integration are the same as in the case of integration-level alerts. You can refer to [this document](https://help.nightfall.ai/nightfall-ai/notion/configuring-integration-alerts#configure-alerts-at-the-integration-level) for steps.

## Automated Actions

This section describes the various actions that Nightfall takes automatically when a violation is detected. You must turn on the toggle switch to enable an action. All the automated actions are permanent and cannot be reversed once applied. You can also set the timeline as to when an action must be taken (immediately after detecting a violation or after some time).

The various automated actions are described as follows.

* **Redact**: This action redacts all the sensitive information found in the content of a Notion page. You can turn on the toggle switch to enable this action. \
  \
  You must also select the timeline as to when this action must be taken after a policy violation is detected. You can either choose to take the action immediately after detecting a violation or after a few minutes, hours, or days.&#x20;
* **Delete Attachment**: This action deletes any attachments in the Notion pages that contain sensitive information. You can turn on the toggle switch to enable this action. \
  \
  You must also select the timeline as to when this action must be taken after a policy violation is detected. You can either choose to take the action immediately after detecting a violation or after a few minutes, hours, or days.&#x20;
* **Mark as Private**: This action modifies the status of the Notion page that contains sensitive information. You can either choose to unpublish the webpage or remove guest users from your Notion account, thus ensuring that none of the people from outside your organization are able to view sensitive information on your Notion page.\
  \
  You must also select the timeline as to when this action must be taken after a policy violation is detected. You can either choose to take the action immediately after detecting a violation or after a few minutes, hours, or days.&#x20;

<figure><img src="../../.gitbook/assets/GIF Recording 2023-11-19 at 2.49.37 PM (1).gif" alt=""><figcaption></figcaption></figure>

### Conflict Management in Automated Actions

Conflicts can arise in two main scenarios:

1. All the automated actions are configured in a single policy.
2. Multiple policies with different automated actions were violated simultaneously within the same file, message or record.&#x20;

When conflicts occur, Nightfall implements the most severe automated action. The priority order to manage conflicts in Notion is as follows.

1. Delete Attachment
2. Redact
3. Remove Access

**Conflict resolution**:

* **Delete Attachment** takes precedence over all other actions if an attachment contains sensitive data.
* For conflicts between **Redact** and **Remove Access**:
  * **Unpublished pages**: Only **Redact** is applied
  * **Published pages**: Both **Redact** and **Remove Access** are implemented. The page is unpublished, and sensitive data is redacted in the internal Notion page.

## End User Notification

This section allows you to configure notifications to be sent to the end user whose actions triggered the violation.&#x20;

* **Custom Message**:  Enter a custom message to be sent to the end user. This message is sent in an Email. You can modify the default message provided by Nightfall and draft your message. The total character length allowed is 1000 characters. You can also add hyperlinks in the custom message. The syntax is \<link | text >. For example, to hyperlink [https://www.nightfall.ai](https://www.nightfall.ai/) with the text **Nightfall website**, you must write <[https://www.nightfall.ai](https://www.nightfall.ai/) | Nightfall website> .
* **Automation**: You can either select Email, Slack, or both as an automated notification method. You must turn the toggle switch to use this option. Based on the options selected, end-users receive notification on their Email account associated with Zendesk, or Slack account configured.

## End User Remediation

End-User remediation (also known as Human Firewall) allows you to configure remediation measures that end users can take when a violation is detected on their Zendesk ticket. You must turn on the toggle switch to use this option. The various available options are as follows.

* **Redact:** This action redacts all the sensitive information found in the Zendesk ticket's comments. To allow end-users to implement this action, you must disable it from the [#automated-actions](advanced_settings.md#automated-actions "mention") section.&#x20;
* **Delete Attachment**: This action deletes any attachments in the Zendesk ticket's comments that contain sensitive information. To allow end-users to implement this action, you must disable it from the [#automated-actions](advanced_settings.md#automated-actions "mention") section.
* **Mark as Private:** This action modifies the permission of the comment (on which sensitive information is detected) from public to internal note. To allow end-users to implement this action, you must disable it from the [#automated-actions](advanced_settings.md#automated-actions "mention") section.
* **Report as False Positive with Business Justification**: This option allows end users to report false positive alerts and provide a business justification as to why the alert is considered to be false positive.&#x20;
* **Report as False Positive**: This option allows end users to report false positive alerts.
* **When a Violation is Reported as False Positive**: You can use this option to set actions to be taken when a violation is reported as false positive by the end-user. You can either set the remediation to be automatic or manual.&#x20;
* **Remind Every (until Violation expires)**: You can use this option to set a reminder for the end-user to take action on the violation. You can choose to remind the end user every 24, 48, or 72 hours.

<figure><img src="../../.gitbook/assets/GIF Recording 2023-11-19 at 2.51.13 PM (1).gif" alt=""><figcaption></figcaption></figure>
