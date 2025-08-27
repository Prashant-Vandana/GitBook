---
description: Learn how to configure the Scope section for Zendesk.
---

# Configure Scope for Zendesk

The Scope stage allows you to select the Zendesk tenant in which the policy can be created.&#x20;

To configure Policy Scope:

1. Click **+ Add Instances** and select an instance.
2. Select one of the following options under the **Include in Monitoring** section. The scope of this policy is limited to only those categories of tickets which are selected in this section.

* **New:** This option adds all the newly created tickets to be monitored.
* **Pending:** This option adds all the pending tickets to be monitored.
* **Open:** This option adds all the open tickets to be monitored.
* **Solved:** This option adds all the solved tickets to be monitored.

3. To select all the tickets, click **Select All**.
4. Select the tags to be included from the **Tags Inclusion** section. Only tickets which have the selected tags are monitored by Nightfall.&#x20;

The **Exclude from Monitoring** section allows you to exclude Groups and Agents from the policy scope. It is optional and you can proceed without configuring this section, if you wish to maintain the scope of the policy to all the Groups and Agents, selected in Step 2.

5. Select the Groups and Agents to be excluded.

* **Groups Exclusion**: This option displays a drop-down menu of all the Groups selected in Step 2. You can select any Group to exclude it from the scope of the policy.
* **Agents (User) Exclusion**: This option displays a drop-down menu of all the Agents (basically users) selected in Step 2. You can select any Agent to exclude them from the scope of the policy.
* **Tags Exclusion**: This option displays a drop-down menu of all the tags in your Zendesk account. You can select tickets with specific tags to be excluded from being moniored.

6. Click **Next**.

<figure><img src="../../.gitbook/assets/3 (6).png" alt="" width="563"><figcaption></figcaption></figure>

## Example Scenario

Consider that you wish to scan all the tickets irrespective of their status. However, there is a specific group called **Support.** You do not wish to scan tickets from this group (assuming it's an internal support group). You can accomplish this by using the **Groups Exclusion** field as shown in the following image.&#x20;

Similarly, you can also exclude a specific user by using the **Agents Exclusion** field.&#x20;
