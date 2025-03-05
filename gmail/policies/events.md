---
description: >-
  Learn how to handle Nightfall Events that were created as a result of
  sensitive data leak in the Gmail DLP.
---

# Manage Gmail Events

When an end user violates a policy in Gmail by sending out an Email with sensitive data, an Event is generated based on the notification settings configured by you in the policy configurations.&#x20;

This document explains where you can find Events on Gmail policy violations and what actions can be taken.

## Nightfall Events

To view Events in the Nightfall Console:

1. Click **Detection and Response** from the left pane.
2. (Optional) Modify the days filter to view Events prior to last 7 days. By default the Events recorded in the **Last 7 Days** are displayed.

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

3. Apply filters to view only the Gmail Events.

<figure><img src="../../.gitbook/assets/image (1272).png" alt="" width="563"><figcaption></figcaption></figure>

4. (Optional) To view historic alerts, set the date filter appropriately.

<figure><img src="../../.gitbook/assets/image (337).png" alt=""><figcaption></figcaption></figure>

Once you filter the Events to view only the Slack Events, you can refer to the [#event-list-view](../../dashboard/sdp_events/#event-list-view "mention") section to learn more about the available options.&#x20;

4. Click on any of the Events to view details of an Event. You may click anywhere in the row of an Event that you wish to inspect. Details will be present via a side panel.

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

The side panel (or the Event detail view) is divided into three separate sections. The first section has information about the occurrence of individual findings with a preview. The third section is an activity log for the Event. Both these sections reveal information that is common across all sources/integrations. You can refer to these common sections in the [#event-detail-view](../../dashboard/sdp_events/#event-detail-view "mention") section.

The second section displays details that are source / integration specific and so the details vary from one integration to the other.&#x20;

## Event Actions

Nightfall allows you to take various action on Events. When you take an action on an Event, the status of the Event changes accordingly. To learn more about Event status, refer to the [status.md](../../dashboard/sdp_events/status.md "mention") document.

In JIRA, you can take actions either from the Event list view page or the Event detail view page. On the Event list view page, you can click the ellipsis menu to view the available list of actions.&#x20;

<figure><img src="../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

On the Event detail view, you can view the applicable actions from the actions section at the bottom.

<figure><img src="../../.gitbook/assets/image (54).png" alt="" width="375"><figcaption></figcaption></figure>

To view the complete list of actions, applicable to all the integrations, you can refer to the [event\_actions.md](../../dashboard/sdp_events/event_actions.md "mention") document.&#x20;

The list of actions supported for Slack are as follows. Some of these actions are common to other integrations as well.&#x20;

* **Copy Event Link**: The action copies the link to the Event. You can save or send this link to directly open the Event. This action is available only on the Event detail view.
* **Ignore**: The ignore action flags Nightfall to ignore all the findings in the Event and may be taken if you find the findings false positive. This action marks the Event as resolved and moves it to the Resolved section. You can undo this action.&#x20;
* **Acknowledge**:  You can take this action to notify other users that you have looked into this Event and will take suitable action in future.&#x20;
* **Notify Email**: This action notifies the end user who added the sensitive data file to the OneDrive about the event,  through email.
* **Notify Slack**: This action notifies the end user who added the sensitive data file to the OneDrive about the event,  through Slack.
* **Send to JIRA**: This action creates a JIRA ticket for the Event. You can pick a project and Issue type while creating the JIRA ticket and can assign the JIRA ticket to the end-user.
* **Resolve**: This action must be taken when the sensitive data is removed completely. This action resolves the Event.

The actions like Encrypt email, Block Email, and Quarantine Email can be configured in the policy settings. To learn more about these actions, click [here](https://help.nightfall.ai/sensitive-data-protection/gmail-dlp/gmail-policies/advanced-settings#automated-actions).&#x20;

## Email Notifications

* If you have configured Email Notification in [Admin Alerting](advanced_settings.md#admin-alerting), Nightfall admins receive the Email notification. This Email allows admins to take actions from within the Email.&#x20;
* If you have configured Email Notification in the Automation section of [End user notification](advanced_settings.md#end-user-notification)[ ](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/configuring-policies/advanced-settings#end-user-notification)settings, end users receive an email from Nightfall. This notification allows end users to take remedial actions from within the Email. The available remedial actions depend on the settings configured in the [end-user remediation](https://help.nightfall.ai/nightfall-ai/gmail-dlp/gmail-policies/advanced-settings#end-user-remediation) section.

<figure><img src="../../.gitbook/assets/image (333).png" alt=""><figcaption></figcaption></figure>



