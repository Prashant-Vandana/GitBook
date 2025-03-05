---
description: Learn how you can configure integration level alerts in Microsoft Teams.
---

# Configure Alerts for Microsoft Teams

The Nightfall for OneDrive integration supports the configuration of alerts at the policy level and at the integration level. Alerts can be sent in Microsoft Teams by using the following alert destinations.

* [Slack](https://help.nightfall.ai/sensitive-data-protection/microsoft-365/nightfall-for-microsoft-teams/configuring-integration-alerts#configuring-slack-as-an-alert-channel)&#x20;
* [Microsoft Teams](https://help.nightfall.ai/sensitive-data-protection/microsoft-365/nightfall-for-microsoft-teams/configuring-integration-alerts#configuring-ms-teams-as-an-alert-channel)
* [Email](https://help.nightfall.ai/sensitive-data-protection/microsoft-365/nightfall-for-microsoft-teams/configuring-integration-alerts#configuring-email-as-an-alert-channel)
* [Webhook](https://help.nightfall.ai/sensitive-data-protection/microsoft-365/nightfall-for-microsoft-teams/configuring-integration-alerts#configuring-webhook-as-an-alert-channel)
* [Jira Tickets](https://help.nightfall.ai/sensitive-data-protection/microsoft-365/nightfall-for-microsoft-teams/configuring-integration-alerts#configuring-jira-as-an-alert-channel)

<figure><img src="../../.gitbook/assets/image (923).png" alt=""><figcaption></figcaption></figure>

When you configure alert settings at the integration level, the alert settings apply to all the policies, created for the OneDrive integration. However, when you configure alert settings specifically for a policy, which is created in the OneDrive integration, the alert settings are applicable only for that specific policy.&#x20;

This document explains how to configure alerts at the integration level. To learn about how to configure alerts at the policy level, read [this document](../../gmail/policies/advanced_settings.md#admin-alerting).

## Prerequisites

* To use Slack as an alert platform, you must first perform the required Slack configurations. You can refer to [this document](https://help.nightfall.ai/nightfall-ai/detection/setting-up-slack-as-an-alert-channel-in-nightfall) to learn more about how to configure Slack as an Alert platform.&#x20;
* To use Webhook as an alert platform, you must first perform the required Webhook configurations. You can refer to [this document](https://help.nightfall.ai/nightfall-ai/operationalizing-dlp/integrating-with-security-tools/integrating-with-siem#configuring-outgoing-webhooks)[ ](https://help.nightfall.ai/nightfall-ai/operationalizing-dlp/integrating-with-security-tools/integrating-with-siem#configuring-outgoing-webhooks)to learn more about how to configure Webhook as an Alert platform. &#x20;
* To use JIRA as an alert platform, you must have the DLP for the JIRA app installed from the [Atlassian Marketplace](https://marketplace.atlassian.com/apps/1226823/dlp-for-jira-nightfall-ai?tab=overview\&hosting=cloud). You can read more about the DLP for JIRA integration [here](https://help.nightfall.ai/nightfall-ai/nightfall-for-jira/getting-started/installing-nightfall-for-jira).&#x20;
* To use MS Teams as an alert platform, you must install the MS Teams alert app in your MS Teams application. You can read more about this setup in the [alerting\_to\_ms\_teams.md](../../nightfall_alert_platform/alerting_to_ms_teams.md "mention") document.

## Configure Alerts at the Integration Level&#x20;

You can configure alerts at the integration level once you have installed the Nightfall for OneDrive DLP  integration.&#x20;

To configure alerts at the integration level:

1. Navigate to the **Microsoft 365** integration.
2. Scroll down to the **Teams Alerting** section.
3. You can configure one or multiple alert channels.&#x20;

<figure><img src="../../.gitbook/assets/GIF Recording 2024-05-01 at 1.03.01 PM.gif" alt=""><figcaption></figcaption></figure>

### Configuring Slack as an Alert Channel

1. To configure Slack as an alert channel, click **+ Slack channel**.

<figure><img src="../../.gitbook/assets/image (840).png" alt=""><figcaption></figcaption></figure>

2. In the **Slack alert channel** field, enter the name of the Slack channel in which you wish to receive the alerts.&#x20;
3. Click **Save**.&#x20;

<figure><img src="../../.gitbook/assets/image (842).png" alt=""><figcaption></figcaption></figure>

A confirmation pop-up box is displayed to confirm if the Slack channel (entered in the second step) must be used only for OneDrive DLP integration or all the Nightfall integrations.&#x20;

4. Select **No, only integration level** to use the Slack channel only for OneDrive DLP, or select **Yes, please** to use the selected Slack channel for all the Nightfall integrations.&#x20;

<figure><img src="../../.gitbook/assets/image (843).png" alt=""><figcaption></figcaption></figure>

### Configuring MS Teams as an Alert Channel

1. Click **+ Microsoft Teams**.

<figure><img src="../../.gitbook/assets/image (924).png" alt=""><figcaption></figcaption></figure>

The **Team** and **Channel** drop-down menus are displayed.&#x20;

<figure><img src="../../.gitbook/assets/image (925).png" alt=""><figcaption></figcaption></figure>

2. Select the required team and/or channel to which the notifications must be sent.
3. Click **Save**.

<figure><img src="../../.gitbook/assets/GIF Recording 2024-04-23 at 3.20.24 PM.gif" alt=""><figcaption></figcaption></figure>

### Configuring Email as an Alert Channel

1. Click **+ Email**.

<figure><img src="../../.gitbook/assets/image (844).png" alt=""><figcaption></figcaption></figure>

2. Enter the Email ID of the recipient who should receive the notification&#x73;**.**&#x20;
3. Click **Save.**&#x20;

<figure><img src="../../.gitbook/assets/imageedit_8_4300516314.png" alt=""><figcaption></figcaption></figure>

A confirmation pop-up box is displayed to confirm if the Email ID (entered in the second step) must be used only for OneDrive DLP integration or all the Nightfall integrations.&#x20;

4. Select **No, only integration level** to use the Slack channel only for One Drive DLP, or select **Yes, please** to use the selected Slack channel for all the Nightfall integrations.&#x20;

<figure><img src="../../.gitbook/assets/image (162).png" alt=""><figcaption></figcaption></figure>

### Configuring Webhook as an Alert Channel

1. Click **+ Webhook**.
2. Enter the Webhook URL.
3. Click **Test**. If the test result is not successful, check the Webhook URL.
4. (Optional) Click **Add Header** to add headers.&#x20;
5. Click **Save**.

<figure><img src="../../.gitbook/assets/imageedit_13_9673272543.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
When you configure alerts to a Webhook, Nightfall AI sends occasional posts to:

* To validate that the Webhook is properly configured before the policy is saved.
* Periodically thereafter to ensure that the Webhook is still valid.

The response to the test Webhooks is `200` status code if successful.

An example of Webhook request is as follows.

<pre class="language-json"><code class="lang-json"><strong>{
</strong>  "service": "nightfall",
  "test": true,
  "timestamp": "2024-03-07T23:18:39Z"
}
</code></pre>

This is part of alert event consumption and can be ignored.&#x20;
{% endhint %}

### **Configuring Jira as an Alert Channel**

1. Click **+ Jira Ticket.**
2. Select a JIRA project from the **Jira Project** drop-down menu.
3. Select an issue type from the **Issue Type** drop-down menu.&#x20;
4. (Optional) Add comments to be added in the JIRA ticket.&#x20;
5. Click **Save changes**.

<figure><img src="../../.gitbook/assets/image (847).png" alt=""><figcaption></figcaption></figure>

A confirmation pop-up box is displayed to confirm if the JIRA settings configured for the OneDrive DLP integration must be applied to all the other Nightfall integrations too.&#x20;

6. Select **No, only integration level** to use the configurations only for OneDrive DLP, or select **Yes, please** to use the selected JIRA configurations for all the Nightfall integrations.&#x20;

<figure><img src="../../.gitbook/assets/image (848).png" alt=""><figcaption></figcaption></figure>

## Configure End-User Notification

When an Event is triggered, Nightfall sends a notification to the end-user whose actions triggered the Event. While notifying the end-user, Nightfall also sends a text message. You can draft the text message to be sent to the end-user. This message applies to all the policies. Click **Save changes** once done.

<figure><img src="../../.gitbook/assets/image (838).png" alt=""><figcaption></figcaption></figure>
