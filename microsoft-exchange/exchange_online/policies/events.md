---
description: >-
  Learn how to handle Nightfall Events that were created as a result of
  sensitive data leak in Microsoft Exchange.
---

# Manage Exchange Events

This document explains the impact on end-users and Microsoft Exchange admins when the automated actions in Exchange DLP (Block, Quarantine, or Encrypt) are implemented.&#x20;

## Block

When an Email is blocked, the end user receives an Email from Nightfall that informs them that their Email was blocked. The status of the Event is also automatically changed to Blocked when the Email is blocked.

## Quarantine

When an email is quarantined, it is stored separately in a secure server. A Microsoft Exchange admin must visit the server, review the quarantined email, and decide as to whether the email must be allowed to travel to the recipient or be blocked. You can refer to this [Microsoft documentation ](https://learn.microsoft.com/en-us/defender-office-365/quarantine-admin-manage-messages-files#view-quarantined-email-details)to learn more about how admin users can view quarantine emails. End-users  can also perform certain actions on quarantined emails based on the settings configured. You can refer to this [Microsoft documentation](https://learn.microsoft.com/en-us/defender-office-365/quarantine-end-user) to learn more about what actions end-users can take on quarantined emails.

## Encrypt

When an Email is encrypted, an additional event is created in the [Nightfall data encryption](https://help.nightfall.ai/data-encryption/gmail/encryption-events-page), apart from the regular event created in Nightfall detection and response. The email is delivered to the recipient. An event is logged in Nightfall detection and response with the Status **Encrypted**.&#x20;

## Understanding Exchange DLP Events

When an end user violates a policy in Exchange DLP, an Event is generated based on the notification settings configured by you in the policy configurations. To learn more about Events, see [sdp\_events](../../../dashboard/sdp_events/ "mention").

To view the Events from the Nightfall Console:

1. Click **Detection and Response** from the left pane.
2. (Optional) Modify the days filter to view Events prior to last 7 days. By default the Events recorded in the **Last 7 Days** are displayed.
3. Apply filters to view only the **Exchange Online** Events.

<figure><img src="../../../.gitbook/assets/image.png" alt="" width="563"><figcaption></figcaption></figure>

Once you filter the Events to view only the Confluence Events, you can refer to the [#event-list-view](../../../dashboard/sdp_events/#event-list-view "mention") section to learn more about the available options.&#x20;

4. Click on any of the Events to view details of an Event. You may click anywhere in the row of an Event that you wish to inspect. Details will be present via a side panel.

## Event Actions

Nightfall allows you to take various action on Events. When you take an action on an Event, the status of the Event changes accordingly. To learn more about Event status, refer to the [status.md](../../../dashboard/sdp_events/status.md "mention") document.

In Exchange, you can take actions either from the Event list view page or the Event detail view page. On the Event list view page, you can click the ellipsis menu to view the available list of actions.&#x20;

<figure><img src="../../../.gitbook/assets/image (1295).png" alt=""><figcaption></figcaption></figure>

On the Event detail view, you can view the applicable actions from the actions section at the bottom.

To view the complete list of actions, applicable to all the integrations, you can refer to the [event\_actions.md](../../../dashboard/sdp_events/event_actions.md "mention") document.&#x20;

The list of actions supported for Confluence are as follows. Some of these actions are common to other integrations as well.&#x20;

* **Copy Event Link**: The action copies the link to the Event. You can save or send this link to directly open the Event. This action is available only on the Event detail view.
* **Ignore**: The ignore action flags Nightfall to ignore all the findings in the Event and may be taken if you find the findings false positive. This action marks the Event as resolved and moves it to the Resolved section. You can undo this action.&#x20;
* **Acknowledge**:  You can take this action to notify other users that you have looked into this Event and will take suitable action in future.&#x20;
* **Notify Email**: This action notifies the end user who added the sensitive data file to the OneDrive about the event,  through email.
* **Notify Slack**: This action notifies the end user who added the sensitive data file to the OneDrive about the event,  through Slack.
* **Send to JIRA**: This action creates a JIRA ticket for the Event. You can pick a project and Issue type while creating the JIRA ticket and can assign the JIRA ticket to the end-user.
* **Resolve**: This action must be taken when the sensitive data is removed completely. This action resolves the Event.



