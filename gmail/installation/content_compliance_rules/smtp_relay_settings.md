---
description: >-
  Learn how to configure the routing rules for SMTP relay settings in the Google
  Workspace.
---

# Configure Routing Rules - SMTP Relay Settings

Once you create the content compliance rules, you must set up the routing rules to configure SMTP relay settings. This ensures that you receive emails only from Nightfall's trusted IP addresses.&#x20;

## Prerequisites

In the Nightfall UI, navigate to **Integrations** from the left navigation bar and click the **Manage** button for the Gmail integration.

<figure><img src="../../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>

All the headers and expressions required to create the compliance rules are available in the **Installation** section under Gmail settings as displayed in the image below. Keep this screen open to copy/paste the headers as you create the routing rules in Google Workspace. We will refer to this page as the **Gmail settings** page throughout the document.&#x20;

<figure><img src="../../../.gitbook/assets/image (1154).png" alt=""><figcaption></figcaption></figure>

## Configure Routing Rules

To configure routing rules:

1. Login to your Google Workspace with an admin account.
2. Navigate to the admin console.&#x20;
3. From the left menu, expand **Apps** > **Google Workspace > Gmail.**
4. Scroll down and select **Routing**.

<figure><img src="../../../.gitbook/assets/image (278).png" alt=""><figcaption></figcaption></figure>

5. Scroll down to the **SMTP relay service** section and click **ADD ANOTHER RULE** (the button can be displayed as **CONFIGURE** if you have not created any SMTP rules).

<figure><img src="../../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

6. Enter a name for the SMTP rule (the name"Routing" is used in this case).&#x20;
7. Select the **Only accept mail from the specified IP addresses** check box.
8. Click **ADD.**

<figure><img src="../../../.gitbook/assets/image (122).png" alt="" width="563"><figcaption></figcaption></figure>

9. In the **Add Setting** dialog box, enter a description in the **Description** field ("Nightfall IP" is used in this case).&#x20;
10. Navigate to the **Gmail settings** page on the Nightfall UI and copy the value from the **IP Address 1** field, located under the **Routing - SMTP Relay Service** section.
11. Return to the Google Admin Workspace window and paste the copied value in the **Enter IP address/range** field.
12. Click **SAVE**.

<figure><img src="../../../.gitbook/assets/image (282).png" alt=""><figcaption></figcaption></figure>

The IP address is added as shown in the following image.&#x20;

<figure><img src="../../../.gitbook/assets/image (283).png" alt=""><figcaption></figcaption></figure>

13. Repeat steps 8-12 to add the other two Nightfall IP addresses (In step 10, copy the values under **IP address 2** and I**P address 3** fields).
14. Select the **Require TLS encryption** check box.
15. Click **SAVE**.

<figure><img src="../../../.gitbook/assets/image (1010).png" alt="" width="563"><figcaption></figcaption></figure>

