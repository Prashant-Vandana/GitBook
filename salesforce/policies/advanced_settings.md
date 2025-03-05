---
description: >-
  Learn how to configure the advanced settings section in Nightfall policies
  created for the Salesforce DLP.
---

# Configure Advanced Settings for Salesforce

This stage allows you to select notification channels if a policy violation occurs. The advanced settings page consists of the following configurations. &#x20;

[#admin-alerting](advanced_settings.md#admin-alerting "mention"): This section describes the process of setting alerts for Nightfall administrators when a policy violation is detected.

[#automated-actions](advanced_settings.md#automated-actions "mention"): This section describes the automated actions that can be taken when a policy violation is detected.

[#end-user-notification](advanced_settings.md#end-user-notification "mention"): This section describes the process of setting alerts for end users (a person whose action caused a violation) when a policy violation is detected.

## Admin Alerting

{% hint style="info" %}
The alert configurations configured in this section describe the process of creating alerts at the policy level. Policy-level alerts apply only to the policy on which they are configured. To configure an alert on all the Slack policies, you must configure alerts at the integration level. To learn more about how to configure integration-level policies for Slack integration, read [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-salesforce/getting-started/configuring-integration-alerts).
{% endhint %}

The steps to configure alert channels for policy-level integration are the same as in the case of integration-level alerts. You can refer to [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-salesforce/getting-started/configuring-integration-alerts#configure-alerts-at-the-integration-level) for steps.

## Automated Actions

This section describes the various actions that Nightfall takes automatically when a violation is detected. You must turn on the toggle switch to enable an action. All the automated actions are permanent and cannot be reversed once applied. You can also set the timeline as to when an action must be taken (immediately after detecting a violation or after some time).

The various automated actions are described as follows.

* **Delete**: This action deletes any attachments or field data in the Salesforce that contains sensitive information. You can turn on the toggle switch to enable this action.\
  \
  You must also select the timeline as to when this action must be taken after a policy violation is detected. You can either choose to take the action immediately after detecting a violation or after a few minutes, hours, or days.

{% hint style="info" %}
**How Delete Action Works for Files in Nightfall DLP for Salesforce**

When you create a new Salesforce file it is considered to be the first version of the file. Every time you edit the file, Salesforce creates a new version of the file that has the latest changes. All the previous versions of the file are also stored by Salesforce.

When Nightfall detects sensitive data in a file, Nightfall overwrites the file and uploads a text file that contains a message on why your file was replaced by the text file. You can contact your Salesforce admin to provide you with the previous version of the file that contains sensitive data. \


Nightfall does not delete the file containing sensitive data because the delete action will delete all the versions of the file.  &#x20;

&#x20;&#x20;
{% endhint %}

{% hint style="warning" %}
The Delete action is not supported for the Salesforce Email object.
{% endhint %}

* **Redact**: This action redacts all the sensitive information found in Salesforce, that is monitored by this policy. You can turn on the toggle switch to enable this action. \
  \
  You must also select the timeline as to when this action must be taken after a policy violation is detected. You can either choose to take the action immediately after detecting a violation or after a few minutes, hours, or days.&#x20;

<figure><img src="../../.gitbook/assets/GIF Recording 2023-12-18 at 6.59.31 PM.gif" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
The Redact action is not applicable to attachments and the Salesforce Email object.
{% endhint %}

### Conflict Management in Automated Actions

Conflicts can arise in two main scenarios:

1. Both the automated actions are configured in a single policy.
2. Multiple policies with different automated actions were violated simultaneously within the same file, message or record.&#x20;

When conflicts occur, Nightfall implements the most severe automated action. The priority order to manage conflicts in Salesforce is as follows.

1. Delete
2. Redact

Nightfall implements the Delete action to resolve the conflict.

## End User Notification

This section allows you to configure notifications to be sent to the end user whose actions triggered the violation.&#x20;

* **Custom Message**: Enter a custom message to be sent to the end user. This message is sent in an Email. You can modify the default message provided by Nightfall and draft your message. The total character length allowed is 1000 characters. You can also add hyperlinks in the custom message. The syntax is \<link | text >. For example, to hyperlink [https://www.nightfall.ai](https://www.nightfall.ai/) with the text **Nightfall website**, you must write <[https://www.nightfall.ai](https://www.nightfall.ai/) | Nightfall website>.
* **Automation**: You can either select Email, Slack, or both as an automated notification method. You must turn the toggle switch to use this option. Based on the options selected, end-users receive notification on their Email account associated with Zendesk, or Slack account configured.

<figure><img src="../../.gitbook/assets/GIF Recording 2023-12-18 at 6.55.17 PM.gif" alt=""><figcaption></figcaption></figure>

## End User Remediation

End-User Remediation (also known as Human Firewall)  allows you to configure remediation measures that end users can take when a violation is detected in their Salesforce orgs. You must turn on the toggle switch to use this option. The various available options are as follows.

* **Delete**: This action deletes any attachments in Salesforce that contain sensitive information. To allow end-users to implement this action, you must disable it from the [#automated-actions](advanced_settings.md#automated-actions "mention") section. The Redact action is not available for the Email object.
* **Redact:** This action redacts all the sensitive information found in Salesforce. To allow end-users to implement this action, you must disable it from the [#automated-actions](advanced_settings.md#automated-actions "mention") section. The Redact action is not available for the Email object and attachments.
* **Report as False Positive with Business Justification**: This option allows end users to report false positive alerts and provide a business justification as to why the alert is considered to be false positive.&#x20;
* **Report as False Positive**: This option allows end users to report false positive alerts.
* **When a Violation is Reported as False Positive**: You can use this option to set actions to be taken when a violation is reported as false positive by the end-user. You can either set the remediation to be automatic or manual.&#x20;
* **Remind Every (until Violation expires)**: You can use this option to set a reminder for the end-user to take action on the violation. You can choose to remind the end user every 24, 48, or 72 hours.

<figure><img src="../../.gitbook/assets/GIF Recording 2023-12-18 at 7.04.19 PM.gif" alt=""><figcaption></figcaption></figure>
