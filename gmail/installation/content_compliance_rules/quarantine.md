---
description: >-
  Learn how to create a quarantime content compliance rule in the Google
  Workspace.
---

# Configure Content Compliance Rule - Quarantine

The Quarantine compliance rule quarantines the email that contains sensitive data.&#x20;

{% hint style="info" %}
**Important**

You must configure this rule only if you wish to use the quarantine automated action.
{% endhint %}

## Prerequisites

In the Nightfall UI, navigate to **Integrations** from the left navigation bar and click the **Manage** button for the Gmail integration.

<figure><img src="../../../.gitbook/assets/image (1152).png" alt=""><figcaption></figcaption></figure>

All the headers and expressions required to create the compliance rules are available in the **Installation** section under Gmail settings as displayed in the image below. Keep this screen open to copy/paste the headers as you create the content compliance rules in Google Workspace. We will refer to this page as the **Gmail settings** page throughout the document.&#x20;

<figure><img src="../../../.gitbook/assets/image (1153).png" alt=""><figcaption></figcaption></figure>

## Content Compliance - Quaranatine

1. Navigate to the Compliance page of the Google Workspace (ignore this step if you are already there else refer to steps 1-6 of the [monitroring.md](monitroring.md "mention") document to navigate to the compliance section).&#x20;
2. Scroll down to the **Content Compliance** section and click **ADD ANOTHER RULE**. (If you have not created any Compliance rule previously, the button might be displayed as **CONFIGURE**).

<figure><img src="../../../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

### Step 1 - Email Messages to Affect

1. Enter a name for the compliance rule ("Quarantine Rule" is added as the name in this document).&#x20;
2. Select **Outbound** and **Internal - Sending** checkboxes in the **Email messages to affect** section.

{% hint style="info" %}
If you select only the **Outbound** check box, only those emails that are routed out of your organization to external domains, are scanned. If you wish to scan internal emails (emails that are sent between the employees of your organization). you must select the **Internal - Sending** check box.
{% endhint %}

### Step 2 - Add Expressions

1. Select the **If ANY of the following match the message** option.
2. Click **Add**.

<figure><img src="../../../.gitbook/assets/image (118).png" alt="" width="563"><figcaption></figcaption></figure>

3. In the **Add** **setting** dialog box, select the **Advanced Content** **match** option.
4. In the **Location** drop-down menu, select **Full headers**.
5. In the **Match type** drop-down menu, select **Contains text**.
6. Navigate to the **Gmail settings** page on the Nightfall UI and copy the value from the **Header** field, located under the **Quarantine Content Compliance Rule (Optional)** section.
7. Return to the Google Admin Workspace window and paste the copied value in the **Content** field. Nightfall updates the headers for all emails that need to be quarantined with “x-nightfall-quarantine”, once they are processed and before they are routed back to Gmail. This enables Gmail to quarantine the emails with this header.
8. Click **SAVE**.

<figure><img src="../../../.gitbook/assets/image (119).png" alt="" width="563"><figcaption></figcaption></figure>

### Step 3 - Add Quarantine Header

1. In stage 3, select **Quarantine message.**
2. (Optional) Select the **Notify sender when mail is quarantined** check box to notify the sender when their email is quarantined.&#x20;
3. Click **SAVE**.

<figure><img src="../../../.gitbook/assets/image (120).png" alt="" width="563"><figcaption></figcaption></figure>
