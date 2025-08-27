---
description: >-
  Learn how to configure the advanced settings section in Nightfall policies
  created for MS SharePoint.
---

# Configure Advanced Settings in SharePoint

This stage allows you to select notification channels if a policy violation occurs. The notification alerts are sent at two levels.

## Admin Alerting

The alert configurations configured in this section describe the process of creating alerts at the policy level. Policy-level alerts apply only to the policy on which they are configured. To configure an alert on all the SharePoint policies, you must configure alerts at the integration level. To learn more about how to configure integration-level policies for the SharePoint integration, read[ this document](https://help.nightfall.ai/nightfall-ai/gmail-dlp/configuring-integration-alerts).

The steps to configure alert channels for policy-level integration are the same as in the case of integration-level alerts. You can refer to[ this document](https://help.nightfall.ai/nightfall-ai/gmail-dlp/configuring-integration-alerts#configure-alerts-at-the-integration-level) for steps.

### Automated Actions

Automated actions allow you to configure automated remediation actions when sensitive data is found in an Email. Nightfall supports two automated actions for SharePoint DLP.&#x20;

**Restrict to Owner**: This action restricts the file access only to the owner of the file.&#x20;

**Move to Recycle Bin**: This action moves the file to the recycle bin. You can recover the file from, the recycle bin later.

**Delete Document**: This action deletes the document from SharePoint.&#x20;

### Conflict Management in Automated Actions

A conflict among automated actions can occur in one of the following scenarios.

* All the automated actions are configured in a single policy.
* Multiple policies with different automated actions were violated simultaneously within the same file or record.&#x20;

When a conflict occurs, Nightfall implements the most severe action. In case of SharePoint, the priority order to manage conflicts is as follows.

1. Delete&#x20;
2. Move to Recycle Bin
3. Restrict to Owner

## End-User Notification

This section allows you to configure notifications to be sent to the end user whose actions\
triggered the violation.

### Custom Message

Enter a custom message to be sent to the end user. This message is sent in an Email. You can modify\
the default message provided by Nightfall and draft your message. The total character length allowed\
is 1000 characters. You can also add hyperlinks in the custom message. The syntax is \<link | text >.\
For example, to hyperlink https://www.nightfall.ai with the text Nightfall website, you must write&#x20;

`<https://www.nightfall.ai | Nightfall website>`.

### Automation

The automation settings allow you to send notifications to end users. You can select one or\
both the notification methods. You must first turn on the toggle switch to use the automation\
option. The automation notification channels are as follows.

* **Email**: This option sends an Email to the user who sent the email with sensitive data.
* **Slack**: This option sends a Slack message to the SharePoint user who sent the email with sensitive data.

### End-User Remediation

End-user remediation (also known as Human Firewall) allows you to configure remediation\
measures that end users can take, when a violation is detected on their SharePoint Emails. You\
must turn on the toggle switch to use this option. End-users receive the remediation actions\
in an Email as an action item. The available actions in that Email depend upon the actions that\
you select in this section. The various available remediation actions for end-users are as follows.

* **Report as False Positive with Business Justification**: This option allows end users to report false positive alerts and provide a business justification as to why the alert is considered to be false positive.
* **Report as False Positive**: This option allows end users to report false positive alerts.

When end-users report alerts as false positives, you can choose the resolution method to be either Automatic or manual. If end-users do not take any remediation action, you can set the frequency at which they must receive the notifications to take action.

\
