# Create MX Record

This process helps Nightfall identify your Exchange online account in Microsoft. This process is executed in the Nightfall console.&#x20;

### Prerequisites

You must execute the following steps to obtain domain name and MX record.

1. In the Microsoft 365 Admin portal, expand **Settings** and select **Domains**.&#x20;
2. Note the Domain name of your organization.&#x20;
3. Click the domain name and select the **DNS records** tab.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXc3hRt3K8Trsk6cqqeTiQ77dfVVUpXDANhbjiDl4XOgQN2IX_3dZnNH9IVNMjF93TvNwqvbLPSqRqVRDByXca4uHTWOMSM-5lWeKbrYU5c0TRwXuSgjGJUgKo13hUC-n0EuE4GksQ?key=gXxqXq4O-toSF3b-7YIbPg" alt="" width="563"><figcaption></figcaption></figure>

4. Navigate to the **Microsoft Exchange** section and click **MX**.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXfR1uemNyjED7DeJrY_VcdNL43IEeEv6LeXp0tSSHRsMcFP0VBF82SZlimKFBqsDlKk-8PpQW-G8CDmpFPV4Y6PeLywrB1ba7MFoYgrn4vGK10r_hJlxivL-30ZePQ8wti7hnOO?key=gXxqXq4O-toSF3b-7YIbPg" alt="" width="563"><figcaption></figcaption></figure>

5. Copy the URL under the **Points to address or Value** column. This is the MX record.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXe8ETSKq8z0hdMDdbRc2zwyURXOzmXmfgWVrMrO5nDiBjec0A5Mr8we_KwyQygV-lLPm9IFNPNHaV5SB0xjZSS9OZ1u4x2t3F-21CHNYyjpcdvfsY7K7E1h8HgOz2f2ls8YIgNilQ?key=gXxqXq4O-toSF3b-7YIbPg" alt=""><figcaption></figcaption></figure>

## Installation Steps

1. Open the **Nightfall app** and navigate to **Integrations**.
2. Click **Manage** for the **Exchange Online** widget. &#x20;
3. Click **Edit MX** record for **Exchange Online**.
4. In the **Domain name** field enter the domain name obtained in the previous section.&#x20;
5. In the **MX Record Submission** field, enter the MX record value obtained in the previous section.&#x20;
6. Click **Add**.
