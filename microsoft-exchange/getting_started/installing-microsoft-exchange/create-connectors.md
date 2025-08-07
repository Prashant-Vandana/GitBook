# Create Connectors

Microsoft Exchange uses connectors to manage inbound and outbound email flow. You must create an outbound connector that defines the Nightfall server to which emails must be redirected for scanning, and an inbound connector that defines how to identify emails scanned and routed to Exchange by Nightfall.

## Create Outbound Connector

1. Navigate to the **Exchange admin center** page from your Exchange account. &#x20;
2. Expand **Mail flow** and select **Connectors**.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfUfwVjmYZAza24drOlcDekE_Q7_n8V87eWMcDRW_qIWlMa3LdGghdYDqLXGsMs1nQ9rfunW7ap7Z_foGUwZBmeFedrIpQi_2Fg2ODRYOi4GxdBm6G0zcp09X5fm1_9rnvaBXuUBQ?key=gXxqXq4O-toSF3b-7YIbPg" alt="" width="563"><figcaption></figcaption></figure>

3. Click **Add a Connector**.
4. Select **Office 365** in the Connection from section.
5. Select **Partner Organization** in the **Connection to** section.
6. Click **Next**.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXdhhdetxpwpWWlnEPnyX_URrID1N167InL2XxRKrMwk2CyaDOvIlkgBu3rhAZJYeKljqLFoQ00HmxHGBLvu8H29agICDq2FZR0cDgQ_D7UGC1aVTZPrBidgofOiheXeTq8j_azjFA?key=gXxqXq4O-toSF3b-7YIbPg" alt="" width="563"><figcaption></figcaption></figure>

7. Enter a name for the connector.&#x20;
8. (Optional) Enter a description for the connector.&#x20;
9. Ensure that the **Turn it on** check box is selected.&#x20;
10. Select the **Only when I have a transport rule set up that redirects messages to this connector** radio option.
11. Click **Next**.
12. Select the **Route email through these smart hosts** option.
13. Enter the following host domain and click **+** to add it.

```html
2r2xfv8u7uz5.fips.qbns.mail-manager-smtp.amazonaws.com
```

14. Click **Next**.&#x20;
15. &#x20;Do not modify security settings. Click **Next**. &#x20;
16. &#x20;Enter [m365-exchangeonline@nightfall.ai](mailto:m365-exchangeonline@nightfall.ai) as the validation Email and click **Validate**.&#x20;
17. Click **Next** once the validation is successful.
18. Click **Create Connector**.

## Create Inbound Connector

1. Click **Add a Connector**.
2. Select **Your organization's email serve**r in the **Connection from** section.
3. Click Next.
4. Enter a name for the connector.&#x20;
5. (Optional) Enter a description for the connector.&#x20;
6. Ensure that the **Turn it on** and the **Retain internal Exchange email headers** check boxes are selected.&#x20;
7. Select the **By verifying that the IP address of the sending server matches one of the following IP addresses**, which belong exclusively to your organization option.
8. Obtain the IP addresses by executing the following steps.&#x20;
   1. Log in to Nightfall.
   2. Click **Integrations** from the left menu.
   3. Click **Manage** on the **Exchange Online** widget.
   4. Click **Deployment Guide** on **Exchange Online**.&#x20;

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

&#x20;      e. Note down the IP addresses  present in the 4th point under **Step 2.**

<figure><img src="../../../.gitbook/assets/image (3) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

9. Enter the IP addresses. Click **+** after entering each IP address.
10. Click **Next**.&#x20;
11. Click **Create Connector**.
