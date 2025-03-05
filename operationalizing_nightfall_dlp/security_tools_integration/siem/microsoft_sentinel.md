---
description: Learn how to integrate Nightfall with Microsoft Sentinel.
---

# Integrating with Microsoft Sentinel

Microsoft Sentinel is Microsoft's SIEM tool which is part of the Microsoft Azure suite. You can use Sentinel as a SIEM tool and send Nightfall alerts to this tool.&#x20;

## Sentinel Data Connectors

To ingest any data into Microsoft Sentinel, you must use a data connector. A Sentinel data connector is a data pipeline which transfers data (alerts, incidents, and so on) from a specific source to Sentinel. Microsoft provides many out of the box data connectors to ingest data into Sentinel.

## Configure Sentinel as Webhook

To use Sentinel as a Webhook and send alerts from Nightfall to Sentinel, you must first configure Sentinel as a webhook. To configure sentinel as a webhook, you must create a custom connector in Sentinel, since there is no out of the box connector for Nightfall AI in Sentinel. Microsoft provides multiple ways in which you can create custom connectors. To learn more about how to create a custom connector, you can refer to this [Microsoft documentation](https://learn.microsoft.com/en-us/azure/sentinel/create-custom-connector).&#x20;

## Configure Outgoing Webhook

Once you create a custom connector in Sentinel, you must configure the Webhook endpoint in Nightfall.&#x20;

1. Click **Integrations** in Nightfall.
2. Click **Manage** for the required integration.&#x20;

<figure><img src="../../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

3. Scroll down to the alerting section and click **+ Webhook**.&#x20;

<figure><img src="../../../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

4. Enter the Sentinel URL obtained in the [#configure-sentinel-as-webhook](microsoft_sentinel.md#configure-sentinel-as-webhook "mention") section.

<figure><img src="../../../.gitbook/assets/image (1139).png" alt="" width="563"><figcaption></figcaption></figure>

5. Click **Test** to verify the URL.&#x20;

<figure><img src="../../../.gitbook/assets/image (1140).png" alt=""><figcaption></figcaption></figure>

You must receive a message as shown in the following image.

<figure><img src="../../../.gitbook/assets/image (1141).png" alt="" width="563"><figcaption></figcaption></figure>

6. Check your webhook if you received a POST message from Nightfall. If no POST message is generated, verify your Webhook URL and try again.
7. (Optional) Click **Add Header** to add authentication parameters.&#x20;
8. Enter the authentication parameters (key value format) under the **key** and **value** columns, respectively.
9. Click the unlock icon to obfuscate the key value pair.&#x20;

<figure><img src="../../../.gitbook/assets/image (1142).png" alt="" width="563"><figcaption></figcaption></figure>

10. Click **Save**.

## Viewing Alert Data in Sentinel

Once you configure Sentinel as a Webhook, Nightfall sends alert notifications to Sentinel. You can view these notifications in Sentinel. To learn more about how to view visual data in Sentinel, you can refer to this [Microsoft documentation](https://learn.microsoft.com/en-us/azure/sentinel/get-visibility). To learn more querying logs using Microsoft's Kusto Query Language, refer to this [Microsoft documentation](https://learn.microsoft.com/en-us/azure/sentinel/kusto-overview).&#x20;
