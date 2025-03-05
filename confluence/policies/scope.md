---
description: >-
  Learn how you can configure the Scope section in a Nightfall for Confluence
  policy.
---

# Configure Scope for Confluence

Nightfall can monitor all your Confluence spaces for sensitive data. However, you can choose to monitor only specific spaces. Additionally, irrespective of whether you have chosen all the spaces or specific spaces for monitoring, Nightfall allows you to exclude specific pages from being monitored, within the selected spaces. You can configure the required spaces and pages within the spaces on the scope page

To configure Policy Scope:

1. Click **+ Add Site** and select a Confluence instance.

<figure><img src="../../.gitbook/assets/image (1169).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If you have configured only a single Confluence site, the configured site is automatically selected and you need not choose from multiple sites. If you wish to monitor multiple Confluence sites, you must create a separate policy for each site.&#x20;
{% endhint %}

Once you choose the site, there are two configurations; **Include In Monitoring** and **Exclude From Monitoring**. The **Include In Monitoring** section allows you to choose specific Confluence Spaces for monitoring. The **Exclude From Monitoring** section is optional and allows you to exclude specific pages from being monitored, from within the selected Spaces.&#x20;

<figure><img src="../../.gitbook/assets/image (1170).png" alt=""><figcaption></figcaption></figure>

## Configure Include in Monitoring Section

By default, all the Spaces are selected for monitoring. To choose only a specific set of Space(s) to be monitored, you must click the **Choose Spaces** radio button.

<figure><img src="../../.gitbook/assets/image (1171).png" alt=""><figcaption></figcaption></figure>

Once you select the Choose Spaces option, a new search field is displayed. This field lists all the Confluence Spaces configured in the selected Confluence site. You can choose the required Space(s).

<figure><img src="../../.gitbook/assets/image (1172).png" alt=""><figcaption></figcaption></figure>

## Configure Exclude From Monitoring Section

This section allows you to exclude specific page(s) (from within the selected Space(s)) from being monitored by Nightfall for sensitive data. You can skip this section if you wish to monitor all the pages from the selected Space(s).&#x20;

Nightfall lists all the pages from the selected Spaces in the drop-down menu. To exclude specific pages, select the required pages from the drop-down menu.

<figure><img src="../../.gitbook/assets/image (1173).png" alt=""><figcaption></figcaption></figure>
