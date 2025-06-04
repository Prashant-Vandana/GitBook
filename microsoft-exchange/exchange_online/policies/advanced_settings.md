---
description: >-
  Learn how to configure the advanced settings section in Nightfall policies
  created for MS Exchange.
---

# Configure Advanced Settings in Exchange

This stage allows you to select notification channels if a policy violation occurs. The notification alerts are sent at two levels.

## Admin Alerting

The alert configurations configured in this section describe the process of creating alerts at the policy level. Policy-level alerts apply only to the policy on which they are configured. To configure an alert on all the Exchange policies, you must configure alerts at the integration level. To learn more about how to configure integration-level policies for the Exchange integration, read[ this document](https://help.nightfall.ai/nightfall-ai/gmail-dlp/configuring-integration-alerts).

The steps to configure alert channels for policy-level integration are the same as in the case of integration-level alerts. You can refer to[ this document](https://help.nightfall.ai/nightfall-ai/gmail-dlp/configuring-integration-alerts#configure-alerts-at-the-integration-level) for steps.

### Automated Actions

Automated actions allow you to configure automated remediation actions when sensitive data is found in an Email. Nightfall supports two automated actions for Exchange DLP.&#x20;

**Block**: The Block action blocks the Email and prevents it from being sent to the recipient. The sender receives a notification email that states that their Email was not sent to the recipient.&#x20;

**Quarantine Email**: The quarantine action guarantees the email which has sensitive data. A Nightfall admin can review the quarantined Email to check if data is sensitive and then take a call as to whether the Email must be sent to the recipient or blocked permanently.&#x20;

**Encrypt Email**: The encrypt action securely encrypts the contents of the email. When the encryption action is applied a new Event is created in the Nightfall Encryption Events page.&#x20;

If you enable the encryption action, additionally you can also configure the following settings.

* **Disable Forward**: Prevents forwarding or adding recipients in Nightfall Secure Reader.
* **Set Expiration Date**: Automatically sets a date after which the email becomes inaccessible to recipients.
* **Persistent Protection on Attachments**: Ensures attachments are only accessible via the secure reader, preventing downloads.

### Conflict Management in Automated Actions

Conflicts can arise in two main scenarios:

* All the automated actions are configured in a single policy.
* Multiple policies with different automated actions were violated simultaneously within the same file, message or record.&#x20;

When conflicts occur, Nightfall implements the most severe automated action. The priority order to manage conflicts in Exchange is as follows.

1. Encryption
2. Block&#x20;
3. Quarantine

If you create three policies and enable the encrypt action in first policy, Block in second policy, and Quarantine in the third policy, and if all of the 3 policies are violated, in this case, the encrypted action is enabled on the Event (and not Block or Quarantine).&#x20;

Also, if you delete the first policy in which the encrypt action is enabled, and then if both the remaining policies are violated, the Block action is enabled (and not Quarantine).

If you enable all the three actions in a single policy, and if the policy is violated, the encryption action is applied.&#x20;

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
* **Slack**: This option sends a Slack message to the Exchange user who sent the email with sensitive data.

### End-User Remediation

End-user remediation (also known as Human Firewall) allows you to configure remediation\
measures that end users can take, when a violation is detected on their Exchange Emails. You\
must turn on the toggle switch to use this option. End-users receive the remediation actions\
in an Email as an action item. The available actions in that Email depend upon the actions that\
you select in this section. The various available remediation actions for end-users are as follows.

* **Report as False Positive with Business Justification**: This option allows end users to report false positive alerts and provide a business justification as to why the alert is considered to be false positive.
* **Report as False Positive**: This option allows end users to report false positive alerts.

When end-users report alerts as false positives, you can choose the resolution method to be either Automatic or manual. If end-users do not take any remediation action, you can set the frequency at which they must receive the notifications to take action.

\
