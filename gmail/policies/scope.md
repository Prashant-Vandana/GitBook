---
description: Learn how to configure the Scope section for Gmail.
---

# Configure Scope for Gmail

The Gmail Scope configuration page allows you to set filters to perform the following tasks.

* **Monitor or Exclude Monitoring of Emails sent by Specific Users and Groups**: You can set up the Gmail scope to monitor only the required emails that were sent by either specific users or from a user group ID. Similarly, you can also choose to exclude certain user and group mail IDs from being monitored.
* **Monitor or Exclude Monitoring of Emails sent to Specific Recipients and Domains**: You can choose specific email IDs that you wish to monitor or skip monitoring.&#x20;

The Scope section is divided into the following two sub-sections.

* **Senders**: Select this option if you wish to monitor or exclude monitoring of outgoing mails from specific users or user groups.&#x20;
* **Recipients**: Select this option to monitor or exclude monitoring of emails sent to specific recipients. The recipients can be a user or a user group. Additionally, you can also choose to exclude an entire domain. All the emails sent to the mail IDs of the excluded domain(s) are not monitored by Nightfall.

<figure><img src="../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>

## Key principles and Priority Order in Which Filters are Evaluated

### Key Principles:

* Exclusions are evaluated before inclusions
* Recipient filters are validated before the sender filters
* User-level filters take priority over group-level filters
* Domain-level filters, for recipients, have the highest priority
* If no filters match, the default action is to scan the email

### Priority order for filters

{% hint style="success" %}
**Important**

The following list represents both the order and priority in which filters are evaluated when multiple filters are configured in a policy. Filters higher on the list take precedence over those lower down.
{% endhint %}

1. Recipient Domain Exclusions
2. Recipient Domain Inclusions
3. Recipient User Exclusions
4. Sender User Exclusions
5. Sender Group Exclusions
6. Recipient User Inclusions
7. Sender User Inclusions
8. Sender Group Inclusions
9. Default to scan all emails, if no other filters apply&#x20;

Now, let's take a look at an example scenario to describe the behavior.

**Example Scenario**:

A marketing team member ([sender@company.com](mailto:sender@company.com)) sends an email to:

* [team@company.com](mailto:team@company.com)
* [ceo@company.com](mailto:ceo@company.com)
* [contact@external-partner.com](mailto:contact@external-partner.com)&#x20;

Let's examine how different filter configurations would affect this email:

1. **Recipient Domain Exclusions**:
   * If configured: external-partner.com is excluded&#x20;
   * Result: Email will still be scanned because not all recipients are in the excluded domain.
2. **Recipient Domain Inclusions**:

* If configured: external-partner.com is included&#x20;
* Result: Email will be scanned given one of the domain is included.

3. **Recipient User Exclusions**:

* If configured: ceo@company.com is excluded
* Result: Email will still be scanned because not all recipients are excluded.

4. **Sender User Exclusions**:

* If configured: sender@company.com is excluded
* Result: Email won't be scanned, regardless of recipients.

5. **Sender Group Exclusions**:

* If configured: Marketing group is excluded
* Result: Email won't be scanned if sender is in the Marketing group.

6. **Recipient User Inclusions**:

* If configured: team@company.com is included
* Result: Email will be scanned because at least one recipient is included.

7. **Sender User Inclusions**:

* If configured: sender@company.com is included
* Result: Email will be scanned due to sender inclusion.

8. **Sender Group Inclusions**:

* If configured: Marketing group is included
* Result: Email will be scanned if sender is in the Marketing group.

9. **Default to scan all emails**:

* If no other filters apply, the email will be scanned.

{% hint style="info" %}
**Notes**:

* The first matching filter as per the priority listed above determines if the email is scanned.
* For recipient-based filters, ALL recipients must match for exclusions, but ANY match triggers inclusions such that the email is scanned.
{% endhint %}

This priority order ensures that the most specific and restrictive rules are applied first, allowing for precise control over email scanning while maintaining a clear hierarchy for conflict resolution when multiple filters are in place.

## Configuring Senders

The **Senders** section is used to configure specific email IDs that must be monitored or excluded from monitoring. The mail IDs of individual users and user group mail IDs can be configured.&#x20;

To configure the Sender section, you must select the **Sender** option by clicking the **Add Filter** drop-down menu.

Once you select the **Sender** option, you can configure **Users** and **User groups**.

### Users Configuration

* **Monitor all:** Select this option to monitor all the emails sent by users whose data was synced from an IdP through the [Directory Sync](https://help.nightfall.ai/nightfall-ai/nightfall-settings/directory-sync) feature.
* **Monitor specific**: Select this filter to monitor all the emails being sent by specific user(s). Once you select this option, you must also select specific user(s) from the search bar. Nightfall populates the name and email IDs of all the users whose data was synced from an IdP through the [Directory Sync](https://help.nightfall.ai/nightfall-ai/nightfall-settings/directory-sync) feature. You must select the required users' mail IDs. All the emails sent by selected users are monitored by Nightfall for sensitive data.
* **Monitor all, except**: Select this filter to exclude user(s). Emails sent by the excluded users are not monitored by the policy. Once you select this option, you must also select specific user(s) from the search bar. Nightfall populates the name and email IDs of all the users whose data was synced from an IdP through the [Directory Sync](https://help.nightfall.ai/nightfall-ai/nightfall-settings/directory-sync) feature. You must select the required user groups. The emails sent by selected users are not monitored by Nightfall.

<figure><img src="../../.gitbook/assets/image (94).png" alt="" width="563"><figcaption></figcaption></figure>

### User Groups Configuration

* **Monitor all:** Select this option to monitor all the emails sent by users whose data was synced from an IdP through the [Directory Sync](https://help.nightfall.ai/nightfall-ai/nightfall-settings/directory-sync) feature.
* **Monitor Specific**: Select this option to monitor all the emails being sent from specific user group mail IDs. Nightfall populates the name and email IDs of all the user groups whose data was synced from an IdP through the [Directory Sync](https://help.nightfall.ai/nightfall-ai/nightfall-settings/directory-sync) feature. You must select the required user group mail IDs. All the emails sent from the selected user group mail IDs are monitored by Nightfall for sensitive data.
* **Monitor all, except**: Select this option to exclude user group(s). Emails sent from the excluded user group mail IDs are not monitored by the policy. Once you select this option, you must also select specific user group(s) from the search bar. Nightfall populates the name and email IDs of all the user groups whose data was synced from an IdP through the [Directory Sync](https://help.nightfall.ai/nightfall-ai/nightfall-settings/directory-sync) feature. You must select the required user groups. The emails sent from the selected user group mail IDs are not monitored by Nightfall.

<figure><img src="../../.gitbook/assets/image (660).png" alt="" width="563"><figcaption></figcaption></figure>

## Configuring Recipients and Domains

The Recipients and Domains section allows you to monitor or exclude monitoring of emails sent to specific recipients. Additionally, you can also exclude monitoring of an entire domain.&#x20;

You can perform the following operations on the recipients section:

* Monitor emails sent to specific recipients. Recipients can be internal/external or users/user groups.
* Exclude monitoring of emails sent to specific recipients. Recipients can be internal/external or users/user groups.
* Include or exclude monitoring of all the mails sent to the email IDs of a specific domain.&#x20;

To configure the Recipient section, you must select the **Recipients** option by clicking the **Add** **Filter** drop-down menu.&#x20;

Once you select the **Recipient** option, you must configure the internal and external Recipients, and the Domains sections.&#x20;

### Internal Recipients

* **Only Include**: Select this option to monitor emails sent to specific recipient email IDs which are generally part of your organization. The email IDs can belong to a user or a user group. Once you select this option, you must also select specific users or group(s) from the search bar. Nightfall populates the name and email IDs of all the users and user groups whose data was synced from an IdP through the [Directory Sync](https://help.nightfall.ai/nightfall-ai/nightfall-settings/directory-sync) feature. You must select the required user(s) and user group(s). All the emails sent to the selected user or user group email IDs are monitored by Nightfall for sensitive data. &#x20;
* **Exclude**: Select this option to exclude the monitoring of emails sent to specific recipient email IDs. The email IDs can belong to a user or a user group. Once you select this option, you must also select specific users or group(s) from the search bar. Nightfall populates the name and email IDs of all the users and user groups whose data was synced from an IdP through the [Directory Sync](https://help.nightfall.ai/nightfall-ai/nightfall-settings/directory-sync) feature. You must select the required user(s) and user group(s). All the emails sent to the selected user or user group email IDs are not monitored by Nightfall for sensitive data.  &#x20;

<figure><img src="../../.gitbook/assets/image (85).png" alt="" width="563"><figcaption></figcaption></figure>

### External Recipients

* **Only Include**: Select this option to monitor emails sent to specific external recipient email IDs. The email IDs can belong to a user or a user group. Once you select this option, you must also enter the email ID of users or group(s) and hit the enter key.  All the emails sent to the external user or user group email IDs are monitored by Nightfall for sensitive data. &#x20;
* **Exclude**: Select this option to exclude the monitoring of emails sent to specific external recipient email IDs. The email IDs can belong to a user or a user group. Once you select this option, you must also enter the email ID of users or group(s) and hit the enter key. All the emails sent to the external user or user group email IDs are not monitored by Nightfall for sensitive data.&#x20;

### Domains

The Domains section allows you to include or exclude an entire domain from being monitored. All the mails sent to the email IDs of the excluded domain are not monitored by Nightfall. Similarly, all the emails sent to the email ID of the included domain are monitored by Nightfall.&#x20;

* **Only Include**: Select this option to monitor emails sent to specific domain(s). All the email IDs which belong to the included domain(s) are monitored by Nightfall. Once you select this option, you must also enter the domain name (example contoso.com) and hit the enter key.  All the emails sent to email ID(s) that belong to the selected domain(s) are monitored by Nightfall for sensitive data. &#x20;
* **Exclude**: Select this option to exclude the monitoring of emails sent to specific domain(s). All the email IDs which belong to the excluded domain(s) are not monitored by Nightfall. Once you select this option, you must also enter the domain name (example contoso.com) and hit the enter key.  All the emails sent to email ID(s) that belong to the excluded domain(s) are not monitored by Nightfall for sensitive data.  &#x20;

<figure><img src="../../.gitbook/assets/image (84).png" alt="" width="563"><figcaption></figcaption></figure>



\


\
