---
description: >-
  Learn how to handle Nightfall Events that were created as a result of
  sensitive data leak in the Nightfall for Slack Pro and Slack Business+
  editions.
---

# Manage Events for Slack

When an end user violates a policy in Slack, an Event is generated based on the notification settings configured by you in the policy configurations. To learn more about Events, see [sdp\_events](../../dashboard/sdp_events/ "mention").

This document explains where you can find notifications on Slack policy Events and what actions can be taken.

## Nightfall Events

To view Events in the Nightfall Console:

1. Click **Detection and Response** from the left pane.
2. (Optional) Modify the days filter to view Events prior to last 7 days. By default the Events recorded in the **Last 7 Days** are displayed.

<figure><img src="../../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

3. Apply filters to view only the Slack Events.

<figure><img src="../../.gitbook/assets/image (1270).png" alt=""><figcaption></figcaption></figure>



Once you filter the Events to view only the Slack Events, you can refer to the [#event-list-view](../../dashboard/sdp_events/#event-list-view "mention") section to learn more about the available options.&#x20;

4. Click on any of the Events to view details of an Event. You may click anywhere in the row of an Event that you wish to inspect. Details will be present via a side panel.

<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

The side panel (or the Event detail view) is divided into three separate sections. The first section has information about the occurrence of individual findings with a preview. The third section is an activity log for the Event. Both these sections reveal information that is common across all sources/integrations. You can refer to these common sections in the [#event-detail-view](../../dashboard/sdp_events/#event-detail-view "mention") section.

The second section displays details that are source / integration specific and so the details vary from one integration to the other.&#x20;

## Event Actions

Nightfall allows you to take various action on Events. When you take an action on an Event, the status of the Event changes accordingly. To learn more about Event status, refer to the [status.md](../../dashboard/sdp_events/status.md "mention") document.

In Slack, you can take actions either from the Event list view page or the Event detail view page. On the Event list view page, you can click the ellipsis menu to view the available list of actions.&#x20;

<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

On the Event detail view, you can view the applicable actions from the actions section at the bottom.

<figure><img src="../../.gitbook/assets/image (43).png" alt="" width="375"><figcaption></figcaption></figure>

To view the complete list of actions, applicable to all the integrations, you can refer to the [event\_actions.md](../../dashboard/sdp_events/event_actions.md "mention") document.&#x20;

The list of actions supported for Slack are as follows. Some of these actions are common to other integrations as well.&#x20;

* **Copy Event Link**: The action copies the link to the Event. You can save or send this link to directly open the Event. This action is available only on the Event detail view.
* **View in Slack**: This action redirects to the sensitive data in the source Slack account. While this action is available only on the Event detail view, please note that relevant access to the source of sensitive data in Slack should be present.
* **Ignore**: The ignore action flags Nightfall to ignore all the findings in the Event and may be taken if you find the findings false positive. This action marks the Event as resolved and moves it to the Resolved section. You can undo this action.&#x20;
* **Acknowledge**:  You can take this action to notify other users that you have looked into this Event and will take suitable action in future.&#x20;
* **Notify Email**: This action notifies the end user who added the sensitive data file to the OneDrive about the event,  through email.
* **Notify Slack**: This action notifies the end user who added the sensitive data file to the OneDrive about the event,  through Slack.
* **Send to JIRA**: This action creates a JIRA ticket for the Event. You can pick a project and Issue type while creating the JIRA ticket and can assign the JIRA ticket to the end-user.
* **Quarantine:** This action quarantines the message with sensitive data. Click [here](https://help.nightfall.ai/sensitive-data-protection/slack/installation-instructions-nightfall-for-slack-2/automated-actions#quarantine) to learn more about the action. This action is available only in the Slack Enterprise edition.
* **Redact**: This action redacts the sensitive data present in the Slack message. Click [here](https://help.nightfall.ai/sensitive-data-protection/slack/installation-instructions-nightfall-for-slack-2/automated-actions#redact) to learn more about the action. This action is available only in the Slack Enterprise edition.
* **Delete**: This action deletes the sensitive data present in Slack messages or attachments.&#x20;
* **Resolve**: This action must be taken when the sensitive data is removed completely. This action resolves the Event.

## Email Notification

* When a data leak occurs, Slack sends an Email to end users, if they have configured Email as a Notification method in their Slack account.
* Additionally, if you have configured Email Notification in [Admin Alerting](https://help.nightfall.ai/nightfall-ai/nightfall-for-slack/installation-instructions-nightfall-for-slack-1/advanced-settings#admin-alerting), Nightfall admins receive the Email notification as shown in the following image.

<figure><img src="../../.gitbook/assets/image (1183).png" alt=""><figcaption></figcaption></figure>

* If you have configured Email Notification in the Automation section of [End User Notification](https://help.nightfall.ai/nightfall-ai/nightfall-for-slack/installation-instructions-nightfall-for-slack-2/advanced-settings#end-user-notification)[ ](#user-content-fn-1)[^1]settings, end users receive an email from Nightfall. This Email allows end users to take actions from within the Email. The actions are present at the end of the email. The available actions depend on the settings configured by you admin in the [End User Notification](https://help.nightfall.ai/nightfall-ai/nightfall-for-slack/installation-instructions-nightfall-for-slack-1/advanced-settings#end-user-notification) section.

<figure><img src="../../.gitbook/assets/image (1184).png" alt="" width="563"><figcaption></figcaption></figure>

## Viewing Notifications in Slack

If you have configured Slack as a Notification in the Automation section of [End User Notification](https://help.nightfall.ai/nightfall-ai/nightfall-for-slack/installation-instructions-nightfall-for-slack-1/advanced-settings#end-user-notification), end users can view the violation notification from within Slack.&#x20;

[^1]: 
