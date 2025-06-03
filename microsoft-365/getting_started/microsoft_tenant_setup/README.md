---
description: Learn how to setup Microsoft Tenant for Nightfall
---

# Setting up Microsoft Tenant

To set up a Microsoft tenant:

1. Click **Integrations** from the left menu.&#x20;
2. Click **Manage** for **MS Teams**/**OneDrive** (depending on which app you are configuring).
3. Expand the required Microsoft tenant. If you cannot view your Microsoft tenant, click **Add Tenant**.&#x20;

<figure><img src="../../../.gitbook/assets/image (1292).png" alt=""><figcaption></figcaption></figure>

4. Click **Update App Selection**.
5. Click **Connect**. The Microsoft sign-in page displays.
6. Enter the email address and password to sign in to Microsoft 365 administrator login. You may be prompted to perform multi-factor authentication on the Microsoft Authenticator app, if you have setup multi-factor authentication.
7. Upon successful authentication, you can view the following list of permissions that are required by the Nightfall Azure app:
   * Permission to read the organization's details
   * Permission to manage the Azure app permissions and grants for individual services like Microsoft Teams.
   * Permission to read and update Azure applications for individual services like Microsoft Teams
   * Permission to read and update the user profile
8. Click **Accept** and your Microsoft 365 tenant information is added to Nightfall.
9. Select the Microsoft applications you want to monitor. Currently, **OneDrive for Business** and **MS Teams** are the available applications.
10. Click **Save Changes.**                 &#x20;
11. Click **Finish** to complete the tenant setup.

After a successful Directory Sync and M365 tenant registration, you can see that the selected apps (MS Teams, OneDrive) show a **Valid** status, which implies they are ready to be monitored for sensitive data. You may proceed with the policy creation for either MS Teams, or OneDrive.

<figure><img src="../../../.gitbook/assets/image (1299).png" alt="" width="563"><figcaption></figcaption></figure>

If you have not enabled either the OneDrive or the MS Teams application, the **Connect** button is displayed against the app. You can click the **Update App Selection** button to enable to the app.&#x20;

<figure><img src="../../../.gitbook/assets/image (994).png" alt="" width="563"><figcaption></figcaption></figure>

## Deleting a Tenant

You can delete a Microsoft tenant. Before you can delete a tenant, you must ensure that there are no active policies configured for that tenant. After you delete a tenant, you would not create any policies on the deleted tenant and Nightfall would not monitor the deleted tenant.&#x20;

To delete a tenant:

1. Click the delete icon for the required tenant. A delete confirmation window is displayed
2. Click **Yes, please.**&#x20;
3. Click **Connect**.&#x20;
4. Log in to Microsoft 365 by entering your admin credentials.&#x20;
5. The Microsoft sign-in window pop-up is displayed. Select the required option.&#x20;
6. The Nightfall delete confirmation window is displayed. Click **Yes, please delete**.&#x20;
7. The delete confirmation window is displayed. Click **Finish**.

