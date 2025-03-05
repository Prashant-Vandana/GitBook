---
description: >-
  Learn how to configure the advanced setting section in Nightfall policies
  created for Microsoft OneDrive.
---

# Configure Advanced Settings for OneDrive

This stage allows you to select notification channels if a policy violation occurs. The notification alerts are sent at two levels.

### Admin Alerting <a href="#admin-alerting" id="admin-alerting"></a>

This section allows you to send notifications to Nightfall users. The various alert methods are as follows. You must first turn on the toggle switch to use an alert method.

{% hint style="info" %}
The alert configurations configured in this section describe the process of creating alerts at the policy level. Policy-level alerts apply only to the policy on which they are configured. To configure an alert on all the OneDrive policies, you must configure alerts at the integration level. To learn more about how to configure integration-level policies for the OneDrive integration, read [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-microsoft-365/nightfall-for-onedrive/configuring-integration-alerts).
{% endhint %}

The steps to configure alert channels for policy-level integration are the same as in the case of integration-level alerts. You can refer to [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-microsoft-365/nightfall-for-onedrive/configuring-integration-alerts#configure-alerts-at-the-integration-level) for steps.&#x20;

### Automated Actions

Automated actions allow you to configure automated remediation actions when sensitive data is found in OneDrive. Nightfall supports the following automated actions for OneDrive DLP.&#x20;

* **Restrict to Owner**: This action suspends the current file permissions and restricts the access of the file only to its owner.&#x20;
* **Delete Document**: The action permanently deletes the file from OneDrive.
* **Move to Recycle Bin**: This action deletes the file from OneDrive. Users can recover the file from OneDrive's recycle bin.&#x20;

To enable the automated actions you must turn on the respective toggle switch.

<figure><img src="../../../.gitbook/assets/image (935).png" alt=""><figcaption></figcaption></figure>

You can also set the timeframe as to when an automated action must be implemented. You can choose to implement the action immediately after discovering sensitive data or after some time has elapsed.&#x20;

<figure><img src="../../../.gitbook/assets/GIF Recording 2024-04-23 at 4.34.38 PM (1).gif" alt=""><figcaption></figcaption></figure>

### Conflict Management in Automated Actions&#x20;

Automated actions in policies can sometimes conflict. This article explains how Nightfall manages these conflicts.

Conflicts can arise in two main scenarios:

1. All the automated actions are configured in a single policy.
2. Multiple policies with different automated actions were violated simultaneously within the same file, message or record.&#x20;

When conflicts occur, Nightfall implements the most severe automated action. The priority order to manage conflicts in OneDrive is as follows.

1. Delete (highest priority)
2. Move to Recycle Bin (Medium priority)
3. Restrict to Owner (lowest priority)

If you create three policies and enable the **Delete** action in first policy, **Move to Recycle Bin** action in second policy, and **Restrict to Owner** action in the third policy, and if all of the 3 policies are violated, in this case, the **Delete** action is applied.&#x20;

Also, if you delete the first policy in which the **Delete** action is enabled, and then if both the remaining policies are violated, the **Move to Recycle Bin** action is applied.

If you enable all the three actions in a single policy, and if the policy is violated, the **Delete** action is applied.&#x20;

### End-User Notifications <a href="#end-user-notification" id="end-user-notification"></a>

This section allows you to configure notifications to be sent to the end user whose actions triggered the violation.

#### Custom Message <a href="#custom-message" id="custom-message"></a>

Enter a custom message to be sent to the end user. This message is sent in an Email. You can modify the default message provided by Nightfall and draft your message. The total character length allowed is 1000 characters. You can also add hyperlinks in the custom message. The syntax is \<link | text >. For example, to hyperlink [https://www.nightfall.ai](https://www.nightfall.ai/) with the text **Nightfall website**, you must write  \
<[https://www.nightfall.ai](https://www.nightfall.ai/) | Nightfall website>.

<figure><img src="../../../.gitbook/assets/image (852).png" alt=""><figcaption></figcaption></figure>

#### Automation <a href="#automation" id="automation"></a>

The automation settings allow you to send notifications to end users. You can select one or both the notification methods. You can select either Email, Teams, or Slack as an automated notification method to notify the end-users. You must select the respective check box to use the notification method. You must first turn the toggle switch to use this option.

<figure><img src="../../../.gitbook/assets/image (1004).png" alt=""><figcaption></figcaption></figure>

#### End-User Remediations <a href="#end-user-remediation" id="end-user-remediation"></a>

End-user remediation (also known as Human Firewall) allows you to configure remediation measures that end users can take, when a violation is detected on their OneDrive files. You must turn on the toggle switch to use this option. End-users receive the remediation actions either in an email, the selected Slack channel, or as a Teams messsage, as an action item. The available actions in that Email depend upon the actions that you select in this section. The various available remediation actions for end-users are as follows.

* **Delete File:**  The action permanently deletes the file from OneDrive. You can use this action here only if it is not enabled in  [#automated-actions](advanced_settings.md#automated-actions "mention").
* **Move to Recycle Bin:** This action deletes the file from OneDrive. Users can recover the file from OneDrive's recycle bin. You can use this action here only if it is not enabled in  [#automated-actions](advanced_settings.md#automated-actions "mention").
* **Restrict to Owner:** This action suspends the current file permissions and restricts the access of the file only to its owner. You can use this action here only if it is not enabled in  [#automated-actions](advanced_settings.md#automated-actions "mention").
* **Report as False Positive with Business Justification**: This action allows end users to report false positive alerts and provide a business justification as to why the alert is considered to be false positive.
* **Report as False Positive**: This action allows end users to report false positive alerts.

<figure><img src="../../../.gitbook/assets/image (937).png" alt=""><figcaption></figcaption></figure>

When end-users report alerts as false positive, you can choose the resolution method to be either Automatic or manual.&#x20;

<figure><img src="../../../.gitbook/assets/image (860).png" alt=""><figcaption></figcaption></figure>

If end-users do not take any remediation action, you can set the frequency at which they must receive the notifications to take action.

<figure><img src="../../../.gitbook/assets/image (862).png" alt=""><figcaption></figcaption></figure>
