---
description: Learn more about various status of Nightfall Events.
---

# Event Status

The Status of an Event implies the current state of the Event. For instance, an Event whose status displays **Notified**, implies that the end-user whose actions caused the violation has been notified about their actions. They must now take appropriate actions.&#x20;

When a new Event is created in Nightfall, the status is **Active**. The status of the violation gets modified by one of the following methods.

* **Automatically**: If you have configured either Admin alerting, end-user alerting, or have allowed end-user remediation, the status of the violation changes automatically.
* **Manually**: If you apply an action on a Violation manually either from the Violations page or from any other platform, the status of the violation changes accordingly.&#x20;

## Status List

The various Status available in Nightfall are listed as follows.

### Active

This status implies that the Event is newly created and no action (not even notification about the Event) is implemented.

### Acknowledged

This status implies that the Nightfall admin has viewed acknowledged the Event. A further action needs to be taken in future.

### Notified

This status implies that the end-users have been notified about their actions that caused the Event.&#x20;

### Redacted

This status implies that the sensitive data that triggered the Event, is redacted.&#x20;

### Quarantined

This status implies that the entity (file, email, and so on) that contains the sensitive data is quarantined from rest of the data.

### Accepted

### Rejected

### Scheduled

### Removed Internal Users

This status implies that the access to the file or entity that contains sensitive data is no longer accessible to the internal users of the organization.

### Removed External Users

This status implies that the access to the file or entity that contains sensitive data is no longer accessible to the external users who are not part of your organization.

### Link Settings Changed

This status implies that the file's (that contains sensitive data) access permissions have been modified.&#x20;

### Deleted

This status implies that the file or the entity that contained the sensitive data is deleted.

### Ignored

This status implies that the Nightfall admin has ignored the Event either because its false positive or because they wish to look into it in the later.

### Disabled Download

This status implies that the file that contains sensitive data has been disabled from downloading. This prevents any user from downloading the file.

### Marked as Private

This status implies that the file or the entity containing sensitive data is marked as private.

### Attachment Deleted

This status implies that the attachment that contains sensitive data has been deleted.&#x20;

### Sent to JIRA

This status implies that a new JIRA ticket has been created to represent this Event.&#x20;

### Encrypted

This status implies that the sensitive data has been encrypted. &#x20;

### Blocked

This status implies that the entity containing the sensitive data has been encrypted. &#x20;

### Input Requested

This status implies that a notification has been sent to the end-user requesting justification for their actions that caused the Event.&#x20;

### Input Received

This status implies that the end-user has provided justification of their action(s) that triggered the Event.

### Restricted to Owner

This status implies that the access to the file containing sensitive data is now restricted only to the owner of the file.

### Deleted File

This status implies that the file containing sensitive data is deleted. &#x20;

### Moved to Recycle Bin

This implies that the entity containing sensitive data is moved to recycle bin.

### Quarantined Email

This status implies that the email has been quarantined. A Nightfall admin must visit the quarantine settings in Gmail and take an action accordingly. This status is applicable only to Gmail.

### Released Email

This status implies that the email was sent to the recipient after scanning. There were no actions taken on the email. This status is applicable only to Gmail.

### Pending

These are the violations which have been notified to the end-users. However no action has been taken by the end-users or any other user.&#x20;

### Resolved

This status implies that the sensitive data issue in the Event has been addressed and thus the Event is resolved.

### Expired

This status implies that the Event has expired since no action has been taken even after the stipulated time period.&#x20;



