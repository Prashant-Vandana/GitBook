---
description: >-
  Learn how to create a monitoring content compliance rule in the Google
  Workspace.
hidden: true
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
---

# Create Content Compliance Rule - Monitoring

{% hint style="info" %}
This document is only applicable to existing customers who have already setup Gmail DLP at least once. If you are a new customer and setting up Gmail DLP for the first time, refer [this documentation](https://help.nightfall.ai/gmail/installation/content_compliance_rules/monitroring).
{% endhint %}

The first content compliance rule is used to monitor all outgoing emails.&#x20;

{% hint style="info" %}
**Important**

It is mandatory for you to create this rule to monitor outgoing emails for sensitive data.&#x20;
{% endhint %}

## Prerequisites

In the Nightfall UI, navigate to **Integrations** from the left navigation bar and click the **Manage** button for the Gmail integration.&#x20;

<figure><img src="../../../.gitbook/assets/image (1151).png" alt=""><figcaption></figcaption></figure>

All the headers and expressions required to create the compliance rules are available in the **Installation** section under Gmail settings as displayed in the image below. Keep this screen open to copy/paste the headers as you create the content compliance rules in Google Workspace. We will refer to this page as the **Gmail settings** page throughout the document.&#x20;

<figure><img src="../../../.gitbook/assets/image (106).png" alt=""><figcaption></figcaption></figure>

## Content Compliance

The steps to create content compliance rule are as follows.&#x20;

1. Login to your Google Workspace with an admin account.
2. Navigate to the admin console.&#x20;
3. From the left menu, expand **Apps** > **Google Workspace > Gmail.**
4. Scroll down and click **Compliance**.

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
When you click **Compliance**, you can view the list of Organization Units (OUs) on the left of the screen (see image below). You can directly configure the compliance rules and routing rules on your production OU (OU at the top most level) by selecting the same.&#x20;

However, Nightfall recommends that you initially configure the rules on a subset OU (one of the nested OUs) which has a small set of users. When you click on a nested OU, the rules are created only for the nested OU that you select. Once you verify that the configuration is working as expected on the nested OU, you can configure the compliance rules on the production OU.&#x20;
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (105).png" alt="" width="563"><figcaption></figcaption></figure>

5. Scroll down to the **Content Compliance** section and click **ADD ANOTHER RULE**. (If you have not created any Compliance rule previously, the button might be displayed as **CONFIGURE**).

<figure><img src="../../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

### **Step 1 - Email Messages to Affect**

1. Enter a name for the compliance rule. For example, Nightfall DLP.
2. Select **Outbound** and **Internal - Sending** checkboxes in the **Email messages to affect** section.

<figure><img src="../../../.gitbook/assets/image (941).png" alt="" width="563"><figcaption></figcaption></figure>

{% hint style="info" %}
If you select only the **Outbound** check box, only those emails that are routed out of your organization to external domains, are scanned. If you wish to scan internal emails (emails that are sent between the employees of your organization). you must select the **Internal - Sending** check box.
{% endhint %}

### Step 2 - Add Expressions

1. In step 2 of the content compliance rule, select the **If ALL of the following match the message** option.
2. You need to **add two expressions in step 2 of content compliance rule.** Click **ADD**.

<figure><img src="../../../.gitbook/assets/image (108).png" alt="" width="563"><figcaption></figcaption></figure>

3. In the **Add** **setting** dialog box, select the **Advanced Content** match option.
4. In the **Location** drop-down menu, select **Sender header.**
5. In the **Match** **type** drop-down menu select **Matches Regex.**
6. Navigate to the **Gmail settings** page on the Nightfall UI, refer to the regular expression format defined under the **Monitoring Content Compliance Rule** section, and create a regular expression that matches your organization name.

{% hint style="info" %}
For example, if your organization name is Contoso.com, you can create the regular expression as `.*@contoso\.com$`

If you are using multiple domains to send emails from your organization and you need to scan outgoing emails from all those domains for sensitive data, you can use a regular expression to specify multiple domains as illustrated in installation instructions in the Nightfall console. For example, `(.`_`@domain-name.extension$|.`_`@domain-name.extension$)`
{% endhint %}

7. In the **Regexp** field, enter the regular expression to match your organization name.
8. Click **SAVE**.

<figure><img src="../../../.gitbook/assets/image (109).png" alt="" width="563"><figcaption></figcaption></figure>

9. You can now add a second expression in step 2 of the content compliance rul&#x65;**.** Click **Add**.
10. Select **Advanced content match** in the drop-down menu.
11. In the **Location** drop-down menu, select **Full headers**.
12. &#x20;In the **Match** **type** drop-down menu select **Not Contains text.**
13. Navigate to the **Gmail settings** page on the Nightfall UI and copy the value from the **Header** field, located under the **Full Header** section.&#x20;
14. Return to the Google Admin Workspace window and paste the copied value in the **Content** field.
15. Click **SAVE**.

<figure><img src="../../../.gitbook/assets/image (110).png" alt="" width="563"><figcaption></figcaption></figure>

The condition expression is created as follows. This expression ensures that all the emails that are not yet scanned by Nightfall are scanned.

<figure><img src="../../../.gitbook/assets/image (173).png" alt="" width="563"><figcaption></figcaption></figure>

### Step 3 - Modify Message and Add Custom Headers

1. In step 3, select **Modify message**.
2. Under the **Headers** section, select the **Add X-Gm-Original-To header** check box.
3. &#x20;Select the **Add custom headers** check box. The **Custom headers** section is displayed once you select this check box.
4. Click **ADD** under **Custom headers** to add a new custom header.

<figure><img src="../../../.gitbook/assets/image (112).png" alt="" width="563"><figcaption></figcaption></figure>

There are two fields; **Header key** and **Header value**.

<figure><img src="../../../.gitbook/assets/image (228).png" alt="" width="563"><figcaption></figcaption></figure>

5. Navigate to the **Gmail settings** page on the Nightfall UI and copy the value from the **Authentication** field, located under the **Messaging Modification** section.
6. Return to the Google Admin Workspace window and paste the copied value in the **Header key** fiel&#x64;**.**&#x20;
7. Navigate to the **Gmail settings** page on the Nightfall UI and copy the value from the **Nightfall UUID** field, located under the **Messaging Modification** section.
8. Return to the Google Admin Workspace window and paste the copied value in the **Header value** field.&#x20;
9. Click **SAVE**.

<figure><img src="../../../.gitbook/assets/image (113).png" alt="" width="563"><figcaption></figcaption></figure>

10. Scroll down to the **Envelope recipient** section and select the **Change envelope** recipient check box. A **Replace recipient** radio button field is displayed.
11. Navigate to the **Gmail settings** page on the Nightfall UI and copy the value from the **Change envelope recipient with** field, located under the **Messaging Modification** section.
12. Return to the Google Admin Workspace window and paste the copied value in the **Replace recipient** field. This is the email address to which emails must be routed for scanning.

<figure><img src="../../../.gitbook/assets/image (1304).png" alt="" width="375"><figcaption></figcaption></figure>

13. Scroll down to the **Encryption (onward delivery only)** section and select the **Require secure transport (TLS)** check box.&#x20;
14. Click **SAVE**.

<figure><img src="../../../.gitbook/assets/image (1305).png" alt="" width="563"><figcaption></figcaption></figure>



