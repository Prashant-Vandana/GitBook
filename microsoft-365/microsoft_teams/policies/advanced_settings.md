---
description: >-
  Learn how to configure the advanced setting section in Nightfall policies
  created for Microsoft Teams.
---

# Configure Advanced Settings in Microsoft Teams

This stage allows you to select notification channels if a policy violation occurs. The notification alerts are sent at two levels.&#x20;

## Admin Alerting

{% hint style="info" %}
The alert configurations configured in this section describe the process of creating alerts at the policy level. Policy-level alerts apply only to the policy on which they are configured. To configure an alert on all the MSTeams policies, you must configure alerts at the integration level. To learn more about how to configure integration-level policies for the OneDrive integration, read [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-microsoft-365/nightfall-for-microsoft-teams/configuring-integration-alerts).
{% endhint %}

The steps to configure alert channels for policy-level integration are the same as in the case of integration-level alerts. You can refer to [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-microsoft-365/nightfall-for-microsoft-teams/configuring-integration-alerts#configure-alerts-at-the-integration-level) for steps.

## End User Notifications

This section allows you to configure notifications to be sent to the end user whose actions triggered the violation.&#x20;

* **Custom Message**: Enter a custom message to be sent to the end user. This message is sent in an Email. You can modify the default message provided by Nightfall and draft your message. The total character length allowed is 1000 characters. You can also add hyperlinks in the custom message. The syntax is \<link | text >. For example, to hyperlink [https://www.nightfall.ai](https://www.nightfall.ai/) with the text **Nightfall website**, you must write <[https://www.nightfall.ai](https://www.nightfall.ai/) | Nightfall website>.

<figure><img src="../../../.gitbook/assets/image (249).png" alt=""><figcaption></figcaption></figure>

* **Automation**: You can select either Email, Teams, or Slack as an automated notification method to notify the end-users. You must select the respective check box to use the notification method. You must first turn the toggle switch to use this option.

<figure><img src="../../../.gitbook/assets/image (250).png" alt=""><figcaption></figcaption></figure>

## End User Remediation

The End-user remediation (also known as Human Firewall) section allows you to configure remediation measures that end users can take when a violation is detected on their MS Teams operations. You must turn on the toggle switch to use this option. The various available options are as follows.

* **Report as False Positive with Business Justification**: This option allows end users to report false positive alerts and provide a business justification as to why the alert is considered to be false positive.&#x20;
* **Report as False Positive**: This option allows end users to report false positive alerts.

<figure><img src="../../../.gitbook/assets/image (251).png" alt=""><figcaption></figcaption></figure>

* **When a Violation is Reported as False Positive**: You can use this option to set actions to be taken when a violation is reported as false positive by the end-user. You can either set the remediation to be automatic or manual.&#x20;

<figure><img src="../../../.gitbook/assets/image (252).png" alt=""><figcaption></figcaption></figure>

* **Remind Every (until Violation expires)**: You can use this option to set a reminder for the end-user to take action on the violation. You can choose to remind the end user every 24, 48, or 72 hours.

<figure><img src="../../../.gitbook/assets/image (253).png" alt=""><figcaption></figcaption></figure>
