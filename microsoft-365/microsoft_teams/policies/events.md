---
description: >-
  Learn how to handle Nightfall Events that were created as a result of
  sensitive data leak in the Microsoft Teams.
---

# Manage Microsoft Teams Events

When Nightfall detects a violation to one or more MS Teams policies, it reports the violation as an Event. This document describes workflows and options for the MS Teams Events. Furthermore, it is recommended to read the Nightfall Events [sdp\_events](../../../dashboard/sdp_events/ "mention") document before proceeding further.

## Nightfall Events

To view the Events in the Nightfall console:

1. Click **Detection and Response** from the left pane.
2. Filter the data to view only the MS Teams Events.

<figure><img src="../../../.gitbook/assets/image (1266).png" alt=""><figcaption></figcaption></figure>

3. (Optional) To view Events prior to the **Last 7 days**, click on the date filter and choose the appropriate date range upto a max of 180 days.

<figure><img src="../../../.gitbook/assets/image (1253).png" alt=""><figcaption></figcaption></figure>

nce you filter the Events to view only the MS Teams events, you can refer to the [#event-list-view](../../../dashboard/sdp_events/#event-list-view "mention") section to learn more about the available options.&#x20;

4. Click on any of the Events to view details of an Event. You may click anywhere in the row of an Event that you wish to inspect. Details will be present via a side panel.Click the ellipsis menu in the right corner or on the violation to view the list of actions that you can take to initiate the violation.

<figure><img src="../../../.gitbook/assets/image (1254).png" alt=""><figcaption></figcaption></figure>

The side panel (or the Event detail view) is divided into three separate sections. The first section has information about the occurrence of individual findings with a preview. The third section is an activity log for the Event. Both these sections reveal information that is common across all sources/integrations. You can refer to these common sections in the [#event-detail-view](../../../dashboard/sdp_events/#event-detail-view "mention") section.

The second section displays details that are source / integration specific and so the details vary from one integration to the other.&#x20;

### Event Actions

Nightfall allows you to take various action on Events. When you take an action on an Event, the status of the Event changes accordingly. To learn more about Event status, refer to the [status.md](../../../dashboard/sdp_events/status.md "mention") document.

In MS Teams, you can take actions either from the Event list view page or the Event detail view page. On the Event list view page, you can click the ellipsis menu to view the available list of actions.&#x20;

<figure><img src="../../../.gitbook/assets/image (1256).png" alt=""><figcaption></figcaption></figure>

On the Event detail view, you can view the applicable actions from the actions section at the bottom.&#x20;

<figure><img src="../../../.gitbook/assets/image (1257).png" alt="" width="563"><figcaption></figcaption></figure>

The list of actions supported for MS Teams are as follows. Some of these actions are common to other integrations as well.&#x20;

* **Copy Event Link**: The action copies the link to the Event. You can save or send this link to directly open the Event. This action is available only on the Event detail view.
* **View in MS Teams**: This action redirects to the relevant document with sensitive data in the source MS Teams. While this action is available only on the Event detail view, please note that relevant access to the document in source message in MS Teams should be present.
* **Ignore**: The ignore action flags Nightfall to ignore all the findings in the Event and may be taken if you find the findings false positive. This action marks the Event as resolved and moves it to the Resolved section. You can undo this action.&#x20;
* **Acknowledge**:  You can take this action to notify other users that you have looked into this Event and will take suitable action in future.&#x20;
* **Notify Email**: This action notifies the end user who sent the message with sensitive data in MS Teams about the event, through email.
* **Notify Slack**: This action notifies the end user who sent the message with sensitive data in MS Teams about the event, through Slack.
* **Notify Teams**: This action notifies the end user who sent the message with sensitive data in MS Teams about the event, through MS Teams.
* **Send to JIRA**: This action creates a JIRA ticket for the Event. You can pick a project and Issue type while creating the JIRA ticket and can assign the JIRA ticket to the end-user
* **Resolve**: This action must be taken when the sensitive data is removed completely from the source file. This action resolves the Event.&#x20;

{% hint style="info" %}
To learn more about how Nightfall handles Deduplication and Auto Resolution of MS Teams Events, see [#ms-teams](../../../dashboard/sdp_events/deduplication.md#ms-teams "mention").
{% endhint %}



## Email Notification

* If you have configured Email Notification in [Admin Alerting](advanced_settings.md#admin-alerting), Nightfall admins receive the Email notification. This Email allows admins to take actions from within the Email.&#x20;
* If you have configured Email Notification in the Automation section of [End user notification](advanced_settings.md#end-user-notification)[ ](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/configuring-policies/advanced-settings#end-user-notification)settings, end users receive an email from Nightfall. This Email allows end users to take actions from within the Email.&#x20;

<figure><img src="../../../.gitbook/assets/GIF Recording 2023-11-13 at 4.32.02 PM.gif" alt=""><figcaption></figcaption></figure>

## Viewing Notifications in MS Teams

When a violation occurs, the end user who triggered the violation receives an Email to their registered Microsoft account. The Email looks as follows.

<figure><img src="../../../.gitbook/assets/Screenshot 2023-11-15 at 11.55.39 AM.png" alt=""><figcaption></figcaption></figure>

If you have enabled [end-user remediation](https://help.nightfall.ai/nightfall-ai/nightfall-for-ms-teams/configuring-policies/advanced-settings#end-user-remediation) in policy settings, based on the options selected in end-user remediation, end-users can view two options. They can either choose to **Remediate in Teams** or **Report as False Positive**. The options to **Remediate in Teams** or **Report as False Positive** are displayed in the Email only if you have configured them in the [end-user remediation](https://help.nightfall.ai/nightfall-ai/nightfall-for-ms-teams/configuring-policies/advanced-settings#end-user-remediation) section of the policy. &#x20;

<figure><img src="../../../.gitbook/assets/Screenshot 2023-11-15 at 12.15.27 PM.png" alt=""><figcaption></figcaption></figure>

