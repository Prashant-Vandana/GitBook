---
description: Learn how to use Slack as an alert platform in Nightall.
---

# Setting up Slack as an Alert Platform

This document explains how to set up Slack to receive violation alerts. You can create a dedicated Slack channel to receive violation alerts from Nightfall. All the violation messages from policies are sent to the dedicated Slack channel.

### Prerequisites <a href="#av7w4sv0ngr6" id="av7w4sv0ngr6"></a>

* You must have admin permissions for the Slack workspace that you wish to use as an Alert platform in Nightfall.

### Important Information <a href="#w23mbwmw8dzw" id="w23mbwmw8dzw"></a>

You can use Slack as an Alert platform in Nightfall. You can create a Slack channel and configure it as an Alert platform in Nightfall. All the violation notifications are directed towards the dedicated Slack channel that you created, once you complete the configuration.

Apart from provisioning you to use Slack as an Alert platform, Nightfall also provides you a Slack integration. This integration is known as [Nightfall for Slack](https://help.nightfall.ai/nightfall-ai/nightfall-for-slack/nightfall-for-slack-quick-start). This integration ensures that no sensitive data leaks out of your organization through the Slack medium.

The process of using Slack as an alert platform is different for Slack integration and other non-Slack Nightfall integrations.

The following three sections highlight the steps required to set up Slack as an alert platform for Slack and non-Slack integrations.

1. Invite the Nightfall DLP Application to your Slack Channel. This step is only required for the Slack integration in Nightfall.
2. Install Slack as an Alert platform. This step is only required for non-Slack integrations in Nightfall.
3. Invite the Nightfall alerts application to your Slack channel. This step is only required for non-Slack integrations in Nightfall.

### Invite the Nightfall DLP Application to your Slack Channel

This step is only required for the Slack integration in Nightfall.

1. Create a dedicated channel in Slack to receive violation notifications from Nightfall.
2. Navigate to the Slack channel created in the above step.
3. Click **Get channel details**.
4. Click the **Integrations** tab.
5. Click **Add an App** under the Apps section.
6. Search with the term Nightfall in the search bar and select **Nightfall Pro DLP for Slack**.
7. Click **Add to Slack**.

![](<../.gitbook/assets/0 (1).gif>)

You can now navigate to the Slack integration in Nightfall and set this channel as an alert platform for the Slack integration. All violations that occur through Slack are notified through this Slack channel.

### Install Slack as an Alert Platform

This step is only required for non-Slack integrations in Nightfall. To use Slack as an alert platform for non-Slack integration, you must first install Slack as an alert platform.

To set up Slack as an Alert platform:

1. Log in to your Nightfall account.
2. Click **Settings** in the left pane.
3. Click the **Alert Platforms** tab.

<figure><img src="../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

4. Click **Install** for the Slack alert platform.

<figure><img src="../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>

5. Enter the name of your Slack workspace.
6. Click **Continue**.

![](<../.gitbook/assets/4 (1).png>)

6. Enter the Email ID associated with your Slack account.
7. The Nightfall permission request page is displayed. Click **Allow**.

![](<../.gitbook/assets/6 (1).png>)

This completes all the steps. You can verify if your connection was successful by navigating to the Alerts platform page. If you see the **Uninstall** button for Slack, it implies that Slack was successfully installed as an alert platform.

**Important**: Do not click the Uninstall button. It uninstalls the Slack alert platform.

<figure><img src="../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

### Invite the Nightfall Alerts Application to your Slack Channel <a href="#l6ppz15uwzsh" id="l6ppz15uwzsh"></a>

This step is only required for non-Slack integrations in Nightfall. Once you install Slack as an alert platform, you must now invite the Nightfall alerts application to your desired channel in which you wish to receive violation notifications.

1. Create a dedicated channel in Slack to receive violation notifications from Nightfall.
2. Navigate to the Slack channel created in the above step.
3. Click **Get channel details**.
4. Click the **Integrations** tab.
5. Click **Add an App** under the Apps section.
6. Search for the term Nightfall in the search bar.
7. Click **Add** for the **Nightfall Alerts** application.

![](<../.gitbook/assets/8 (1).gif>)

You can now navigate to any non-Slack integration in Nightfall and enter the name of this channel in the Slack alerts section. All the violation alerts from the selected integration are directed towards the Slack channel.

![](<../.gitbook/assets/9 (1).gif>)
