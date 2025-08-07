---
description: >-
  Learn the various permissions available to the security analyst role in
  Nightfall.
---

# Security Analyst Role

The Security Analyst role allows users to view Dashboard, generate reports from Dashboards, view DLP violations, view exfiltration and posture management events, and view detectors.&#x20;

The Nightfall app view for a user with this role is as shown in the following image.&#x20;

<figure><img src="../../.gitbook/assets/image (1017).png" alt=""><figcaption></figcaption></figure>

## Permissions Associated with Security Analyst Role

A user with Security Analyst Role has the following permissions

### View Dashboard and Create Reports

With the **Dashboard** and **Reportin**g permissions, users to view data on the Dashboard, apply filters to the dashboard data, and also generate reports from the Dashboard data.&#x20;

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Take Actions on DLP Violations

With the **DLP Violations** permission, users can take appropriate actions on the DLP violations. They can also share the violation data and export it as a CSV file.&#x20;

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Preview the DLP Violations Content

With the **Content Preview** permission, users can preview the content of the DLP Violations page. The sensitive data is redacted. Also, Security analysts cannot download the file containing sensitive data (even if the download button is active).

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure>

{% hint style="info" %}
The main point of difference between the Security analyst role and the Security events manager role is that users with the Security analyst role can view redacted content of DLP violations page. However, content is not redacted for users with the Security Events manager role. &#x20;
{% endhint %}

### Exfiltration/Posture Management and Encryption Events

With the **Exfiltration** permission, users can filter event data, share event data, view historic events data, and  take actions on Posture management, Exfiltration, and encryption events.&#x20;

<figure><img src="../../.gitbook/assets/image (1023).png" alt=""><figcaption></figcaption></figure>

### View Detectors

With the **Detectors** permission, users can view all the detectors, view detectors that belong to a specific category, filter the list of detectors, search a detector, and copy the UUID of a detector.&#x20;

<figure><img src="../../.gitbook/assets/image (1024).png" alt=""><figcaption></figcaption></figure>
