---
description: >-
  Learn the process of configuring advanced settings while creating a Nightfall
  policy in Nightfall for GitHub.
---

# Configure Advanced Settings for GitHub

This stage allows you to select notification channels if a policy violation occurs. The notification alerts are sent at two levels.&#x20;

## Admin Alerting

{% hint style="info" %}
The alert configurations configured in this section describe the process of creating alerts at the policy level. Policy-level alerts apply only to the policy on which they are configured. To configure an alert on all the Slack policies, you must configure alerts at the integration level. To learn more about how to configure integration-level policies for Slack integration, read [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/getting-started).
{% endhint %}

The steps to configure alert channels for policy-level integration are the same as in the case of integration-level alerts. You can refer to [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/getting-started/configuring-integration-alerts#configure-alerts-at-the-integration-level) for steps.

## End-User Notification

This section allows you to configure notifications to be sent to the end user whose actions triggered the violation.&#x20;

### Custom Message

Enter a custom message to be sent to the end user. This message is sent in an Email. You can modify the default message provided by Nightfall and draft your message. The total character length allowed is 1000 characters. You can also add hyperlinks in the custom message. The syntax is \<link | text >. For example, to hyperlink [https://www.nightfall.ai](https://www.nightfall.ai/) with the text **Nightfall website**, you must write \
&#x20; <[https://www.nightfall.ai](https://www.nightfall.ai/) | Nightfall website>.

### Automation

You can select one of the following methods. You must turn the toggle switch to use this option.

* **Via Email:** This option sends an Email to the GitHub developer. If Nightfall cannot detect the Email ID of the developer, the Email ID provided in the **Fallback Email** field is used.
* **Via GitHub**: This option tags the developer in the Pull Request / Commit with the details on the violation. This will also generate a notification that the developer can view in their GitHub profile account.
* **Via Slack**: This option sends a Slack notification to the developer whose GitHub actions triggered an event. The email id of the developer in GitHub and the one used in Slack must be the same for this to work.

{% hint style="info" %}
To learn more about how you can view Notifications in GitHub, see [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/configuring-policies/managing-github-violations#viewing-notifications-in-github).&#x20;
{% endhint %}

### End-User Remediation

End-user remediation (also known as Human Firewall) allows you to configure remediation measures that end users can take, when a violation is detected on their GitHub operations. You must turn on the toggle switch to use this option. The various available options are as follows.

* **Report as False Positive with Business Justification**: This option allows end users to report false positive alerts and provide a business justification as to why the alert is considered to be false positive.&#x20;
* **Report as False Positive**: This option allows end users to report false positive alerts.
* **When a Violation is Reported as False Positive**: You can use this option to set actions to be taken when a violation is reported as false positive by the end-user. You can either set the remediation to be automatic or manual.&#x20;
* **Remind Every (until Violation expires)**: You can use this option to set a reminder for the end-user to take action on the violation. You can choose to remind the end user every 24, 48, or 72 hours.

To understand where end users can see these options, see [GitHub Notifications](https://help.nightfall.ai/github/events#viewing-notifications-in-github).

<figure><img src="../../.gitbook/assets/image (1283).png" alt="" width="563"><figcaption></figcaption></figure>

