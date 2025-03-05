---
description: >-
  Learn how you can configure the Scope section while creating a policy in
  Nightfall for JIRA.
---

# Configure Scope in Nightfall for JIRA

Nightfall can scan all Jira item types (Tickets, Attachments, and Comments). Scans will include archived items, but not deleted items. Only fields of type free-text fields are scanned: Summary (title), Description (body), Labels, and all custom fields. Fields such as Assignee, and Reporter, are not scanned.

To configure Policy Scope:

1. Click **+ Add Instances** and select an instance.
2. Select one of the following options under the **Include in Monitoring** section. The scope of this policy is limited to only those categories of tickets which are selected in this section.

* **All Projects:** This option ensures that all the projects in your JIRA environment are monitored by Nightfall.
* **Choose Projects**: This option allows you to select the projects in your JIRA environment that you wish to be monitored by Nightfall.

The **Exclude from Monitoring** section allows you to exclude Projects. You can use this option to exclude projects if you have selected the **All Projects** option in Step 2.&#x20;

Click **Next**.

<figure><img src="../../.gitbook/assets/GIF Recording 2023-11-19 at 6.43.48 PM.gif" alt=""><figcaption></figcaption></figure>
