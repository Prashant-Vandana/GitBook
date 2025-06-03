---
description: >-
  Learn how to integrate Nightfall with a SIEM or push violations downstream to
  any alert drain, SOAR tool, BI tool, and more.
---

# Integrating with SIEM

To integrate with a SIEM or push Nightfall alerts downstream, specify a webhook URL in your Nightfall console.

First, configure an incoming webhook in the tool you'd like to send Nightfall alerts into. For example, this could be Splunk, Sumo Logic, LogRhythm, Slack, PagerDuty, etc.

{% tabs %}
{% tab title="LogRhythm" %}
For **LogRhythm** integration, initialize the Webhook Beat by following these [**instructions**](https://docs.logrhythm.com/docs/OCbeats/webhook-beat/initialize-the-webhook-beat).&#x20;

This process will provide you with an HTTPS URL endpoint (as seen in step 4c). Copy this URL as you will use it to complete set up.
{% endtab %}

{% tab title="SumoLogic" %}
For **Sumo Logic** integration, configure an HTTP Logs and Metrics Source via the following [**instructions**](https://help.sumologic.com/03Send-Data/Sources/02Sources-for-Hosted-Collectors/HTTP-Source).

This process will provide you with a URL endpoint (as seen in step 10). Copy this URL as you will use it to complete set up.
{% endtab %}

{% tab title="Splunk" %}
For a **Splunk** integration, configure an HTTP Event Collector within Splunk via the following [**instructions**](https://docs.splunk.com/Documentation/Splunk/8.2.2/Data/UsetheHTTPEventCollector).

This process will provide you with a URL endpoint (as seen in [this step](https://docs.splunk.com/Documentation/Splunk/8.2.2/Data/UsetheHTTPEventCollector#Send_data_to_HTTP_Event_Collector)). Copy this URL as you will use it to complete set up.\


### Authentication via HTTP Header

To authenticate to the HTTP Event Collector, you may add an `Authorization` [http header](./#adding-headers-for-webhooks) as described in the Splunk documentation with your [HTTP Event Collector token](https://docs.splunk.com/Documentation/Splunk/8.2.2/Data/HTTPEventCollectortokenmanagement).

Note that the Authorization HTTP header for HEC requires the "Splunk" keyword before the HEC token.



### Authentication via Query String

It is also possible to add your HEC Token as part of the query string of the Collector URL. This can be done for both Splunk Cloud as well as Enterprise.&#x20;



If you are a Splunk Cloud customer, you will have to reach out to Splunk to enable the "allowQueryStringAuth" flag for your Splunk Cloud instance. This can be done by raising a Support Ticket with Splunk. _This field can only be updated if on a Paid account. For a free/trial account, it will be unavailable._



For Splunk Enterprise, you will have to enable query string authentication for your instance, by following these steps:

Go to $SPLUNK\_HOME/etc/apps/splunk\_httpinput/local/inputs.conf file. Your tokens will appear by name in this file, in the form of http://\<token\_name>.

Within the stanza for each token you want to enable query string authentication, add or change the following setting:

```
allowQueryStringAuth = true
```



Once the flag is enabled, please use the following steps to query the HEC Token within the URL String. For more information on Query string authentication from Splunk, please reference the docs [here](https://docs.splunk.com/Documentation/Splunk/latest/Data/FormateventsforHTTPEventCollector?_ga=2.248963079.1684971225.1643234776-799499204.1642112137).\


You can specify the HEC token as a query string in the URL that you specify in your queries to HEC. This can be done with the format shown below:



```
?token=<hec_token>
```



The following example shows a full Collector URL including a dummy HEC Token appended as a query string: (The example is for an Enterprise instance)



Note: We will be using the `/services/collector/raw endpoint` instead of the `/services/collector/event` endpoint. This is because of the JSON format that webhooks from Nightfall will carry, which will only be accepted with the raw version of the HTTP Event Collector endpoint.\


```
https://mysplunkserver.example.com:8088/services/collector/raw?token=12345678-1234-1234-1234-1234567890AB
```

###

### For Splunk Cloud Customers:

For Splunk Cloud customers, the above example URL will look different including the public facing HEC URL. The endpoint (`/services/collector/raw?token=12345678-1234-1234-1234-1234567890AB`) should remain the same, however. Since you are on a Splunk Cloud instance, this URL should already be visible to the Nightfall console, and you would be able to start using this Webhook URL in the Nightfall console. Please continue with the steps after this section to complete webhook set up.





### **For Splunk Enterprise Customers**:&#x20;

For Splunk Enterprise customers, there are a few extra steps to have the Splunk Collector exposed to the Nightfall webhook console below.

The next step will be exposing the local host and port of the Splunk collector an HTTP Listening tool. This can be done by using an ngrok tunnel or nginx server, for example This is required so that the Enterprise Splunk instance is accessible to Nightfall's webhook from the console. Please make sure that port 8088 (this is the default port for receiving data for HEC) is accessible by navigating to "Global settings" in your Splunk Enterprise instance and enabling it.&#x20;

Steps for setting up a ngrok tunnel can be found [here](https://ngrok.com/docs). If using a ngrok tunnel, the following command would generate a ngrok tunnel listening to the correct port and protocol for the collector:\


`./ngrok http https://localhost:8088`



Once complete, the ngrok tunnel should show you an HTTPS Forwarding address, that can be used as the ngrok host in the following step. (HTTPS is required by Nightfall's webhook URL validation)



Your ngrok tunnel URL with your HEC auth token should now look something like this:



[`https://<NGROK_HOST>/services/collector/raw?token=<YOUR_HEC_TOKEN>`](https://4fe56621b120.ngrok.io/services/collector/raw?token=e5c20168-7e57-41a0-a045-6d08a6a6097b)



This will be your Webhook URL that you can use in the Nightfall console. Now you are all set to integrate alerts from your Nightfall webhook to your ngrok tunnel.
{% endtab %}
{% endtabs %}

## Configuring Outgoing Webhooks

Next, configure the outgoing webhook in Nightfall. This webhook will fire in real-time upon a new event (e.g. a new violation is created).&#x20;

Navigate to the integration for which you would be interested in setting up a webhook for alerts. Webhooks are available all native integrations.

1. Select the **Settings** tab on the top.
2. Click the **Console Audit** tab.&#x20;
3. Click **+ Webhook.**
4. Enter the URL to your webhook endpoint.&#x20;
5. You may send a sample payload to the endpoint that you have entered to verify a successful connection using the **Test** button.

![](<../../../.gitbook/assets/Configure Alter URL with Test Button HTTPS.png>)

### Adding Headers for Webhooks

You may also add HTTP Headers to send authentication tokens or other content using the **Add Headers** button.

<figure><img src="../../../.gitbook/assets/image (1284).png" alt="" width="375"><figcaption></figcaption></figure>

Once your header key and value is entered you may obfuscate it by clicking on the "lock" icon next to the value field for the header. Click the **Save** button to persist your changes to the headers.

When you have completed configuring your Webhook URL and Headers, click the **Save** button.

Going forward, you will now see events sent directly from Nightfall into your SIEM or other solution of choice.

## Nightfall Webhook Event Types

When Nightfall sends a message to the configured Webhook, an event is always included in the message. Nightfall sends the following four types of events listed in the following table.&#x20;

| Event Name        | Event Description                                                                                                                                                                                                   |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `exposure_update` | An alert that triggers if there are new findings or if findings have been removed from the [Nightfall Event](https://help.nightfall.ai/sensitive-data-protection/dashboards_violations/nightfall-events).           |
| `resolution`      | An alert that triggers when the [Nightfall Event](https://help.nightfall.ai/sensitive-data-protection/dashboards_violations/nightfall-events) is resolved.                                                          |
| `violation`       | An alert that triggers when a new [Nightfall Event](https://help.nightfall.ai/sensitive-data-protection/dashboards_violations/nightfall-events) is created.                                                         |
| `remediation`     | An alert that is triggered when any remediation action (eg . Redact, delete) content is taken on the [Nightfall Event](https://help.nightfall.ai/sensitive-data-protection/dashboards_violations/nightfall-events). |

## Webhook Payload Examples

The following are examples of a sample payload for detection rules that were violated, that will be delivered to the webhook. These are examples from each integration, so the specific fields may vary based on the Nightfall product you are using (e.g. Slack, Github, Google Drive Jira, etc.).

{% tabs %}
{% tab title="Slack" %}
<pre><code><strong>{
</strong>  "detectionRulesLink": "https://app.nightfall.ai/detection-engine/detection-rules/",
  "detectionRulesViolated": [
{
  "eventType": "violation",
  "service": "Slack",
  "companyUUID": "0957cfbd-3e71-41e5-a2eb-691668fa5572",
  "fileName": "",
  "foundIn": "Public Channel",
  "who": {
    "username": "",
    "fullName": "aziz_demo",
    "email": "",
    "userID": "U038GT1SKFE"
  },
  "permalink": "https://yoourco.slack.com/archives/C038T5N5GM7/p1668033451531234",
  "violationLink": "https://app.nightfall.ai/violations/fa7c7a95-c46c-4c3d-ab78-2b63cccc1234",
  "violationTime": "2022-11-09T22:37:34.808263861Z",
  "integrationMetadata": {
    "workspaceName": "",
    "channel": "demo",
    "channelID": "C038T5N5GM7"
  },
  "findings": [
    {
      "detectionRule": {
        "uuid": "c983ff3b-a005-45da-b104-1522c0d9c712",
        "name": "HBI Internal Person &#x26; Project Names"
      },
      "policy": {
        "uuid": "3c55d347-34a8-4987-a077-b00e9d70649e",
        "name": "My Slack Policy"
      },
      "detector": {
        "uuid": "293bda1f-00e7-4ac2-b580-2c9512816140",
        "name": "V.I.P List"
      },
      "occurrences": [
        {
          "snippet": "ey Brian did you see Go********** in the building toda"
        }
      ],
      "detectionRuleLink": "https://app.nightfall.ai/detection-engine/detection-rules?selectedDetectionRules=c983ff3b-a005-45da-b104-1522c0d9c712",
      "policyLink": "https://app.nightfall.ai/slack/policies/3c55d347-34a8-4987-a077-b00e9d70649e"
    },
    {
      "detectionRule": {
        "uuid": "29d5f705-6954-4883-a903-3c960ebc3960",
        "name": "My Detection rule"
      },
      "policy": {
        "uuid": "accdb5a7-db06-4614-9495-cdeb74b305cb",
        "name": "My Policy"
      },
      "detector": {
        "uuid": "f480b42c-2724-4264-aa12-79044fa6b1c1",
        "name": "My Dictionary of secret entries"
      },
      "occurrences": [
        {
          "snippet": "ey Brian did you see Go********** in the building toda"
        }
      ],
      "detectionRuleLink": "https://app.nightfall.ai/detection-engine/detection-rules?selectedDetectionRules=29d5f705-6954-4883-a903-3c960ebc3960",
      "policyLink": "https://app.nightfall.ai/slack/policies/accdb5a7-db06-4614-9495-cdeb74b305cb"
    }
  ]
}
</code></pre>
{% endtab %}

{% tab title="Github" %}
```
{
  "detectionRulesLink": "https://app.nightfall.ai/detection-engine/detection-rules",
  "detectionRulesViolated": [
    "dcc6dd2e-0177-4110-ab3d-0778cc1e76d2"
  ],
  "eventType": "violation",
  "message": "Policy Violation Detected",
  "policiesLink": "https://app.nightfall.ai/github/policies",
  "policiesViolated": [
    "8478f262-e54d-423d-b63f-a3e322329eaf"
  ],
  "service": "github",
  "timestamp": "2022-01-26T23:05:35Z",
  "violationId": "6d6639f0-6deb-4b81-ac89-59b4cf9448f4",
  "violationMetadata": {
    "authorEmail": "66931356+awanarslan@users.noreply.github.com",
    "branchName": "main",
    "commitRef": "11755af67b8ef514ce6f3ce13864cce69bbd2b24",
    "confidence": "Very Likely",
    "contentType": "commit",
    "detector": "US social security number (SSN)",
    "filePath": "traptext.txt",
    "lineRangeEnd": 18,
    "lineRangeStart": 18,
    "organizationName": "test-org-aawan",
    "repositoryName": "tst-secret-scan",
    "violationLink": "https://app.nightfall.ai/github/violations/6d6639f0-6deb-4b81-ac89-59b4cf9448f4"
  },
  "violationTime": "2022-01-26T23:05:34Z"
}
```
{% endtab %}

{% tab title="Google Drive" %}
```
{
  "eventType": "violation",
  "service": "Google Drive",
  "companyUUID": "e64d1a72-5488-4f9f-bd8a-059c5e5e7ded",
  "fileName": "Payment tracking",
  "foundIn": "application/vnd.google-apps.document",
  "who": {
    "username": "user@useremail.com",
    "fullName": "",
    "email": "",
    "userID": ""
  },
  "permalink": "https://docs.google.com/document/d/1DSPOp6Xdpz4oguFjAQfdrhHqooC8ZpRxISQUanH1234/edit?usp=drivesdk",
  "violationLink": "https://app.nightfall.ai/violations/049e2ca1-86e8-4601-add1-6aed27701234",
  "violationTime": "2022-11-11T18:46:30.111325042Z",
  "integrationMetadata": {
    "fileOwner": "user@useremail.com",
    "linkSettings": "",
    "existingFindings": null,
    "sharedDriveLink": "https://docs.google.com/document/d/1DSPOp6Xdpz4oguFjAQfdrhHqooC8ZpRxISQUanH1234/edit?usp=drivesdk",
    "sharedDriveName": "",
    "sharedWith": ""
  },
  "findings": [
    {
      "detectionRule": {
        "uuid": "42efe36c-6479-412a-9049-fd8cdf895ced",
        "name": "my test detector rule"
      },
      "policy": {
        "uuid": "9bd2215f-2ab1-4c47-b464-fb401222eb91",
        "name": "Demo Policy"
      },
      "detector": {
        "uuid": "74c1815e-c0c3-4df5-8b1e-6cf98864a454",
        "name": "Credit card number"
      },
      "occurrences": [
        {
          "snippet": "******* credit card 35***************** has been charged"
        }
      ],
      "detectionRuleLink": "https://app.nightfall.ai/detection-engine/detection-rules?selectedDetectionRules=42efe36c-6479-412a-9049-fd8cdf81234",
      "policyLink": "https://app.nightfall.ai/google-drive-dlp/policies/9bd2215f-2ab1-4c47-b464-fb4012221234"
    }
  ]
}
```
{% endtab %}

{% tab title="Jira" %}
```
{
  "eventType": "violation",
  "service": "Confluence",
  "companyUUID": "e64d1a72-5488-4f9f-bd8a-059c5e5e7ded",
  "fileName": "",
  "foundIn": "page",
  "who": {
    "username": "Max Rogers",
    "fullName": "Max Rogers",
    "email": "user@useremail.com",
    "userID": "5f965f1399b42e00697fef67"
  },
  "permalink": "https://myco.atlassian.net/wiki/spaces/ENGG/pages/163955/Brainstorming",
  "violationLink": "https://app.nightfall.ai/violations/b437fb40-df86-47e6-b318-26c8d3d61234",
  "violationTime": "2022-11-11T18:39:37.154475401Z",
  "integrationMetadata": {
    "contentName": "Brainstorming",
    "parentPageName": "",
    "authorID": "5f965f1399b42e00697fef67",
    "contentID": "163955"
  },
  "findings": [
    {
      "detectionRule": {
        "uuid": "42efe36c-6479-412a-9049-fd8cdf895ced",
        "name": "my test detector rule"
      },
      "policy": {
        "uuid": "6f82326e-0a22-4bce-a313-25b234474479",
        "name": "Engg Ravi"
      },
      "detector": {
        "uuid": "74c1815e-c0c3-4df5-8b1e-6cf98864a454",
        "name": "Credit card number"
      },
      "occurrences": [
        {
          "snippet": "edit card tracking - 35*****************\nCredit card tracking"
        },
        {
          "snippet": " to this credit card 35*****************\nBrainstorming method"
        },
        
      ],
      "detectionRuleLink": "https://app.nightfall.ai/detection-engine/detection-rules?selectedDetectionRules=42efe36c-6479-412a-9049-fd8cdf891234",
      "policyLink": "https://app.nightfall.ai/confluence/policies/6f82326e-0a22-4bce-a313-25b234471234"
    }
  ]
}
```
{% endtab %}

{% tab title="Confluence" %}


```
{
  "detectionRulesLink": "https://app.nightfall.ai/detection-engine/detection-rules?selectedDetectionRules=6a86a804-4aa6-41fe-a288-aea9a69b458d",
  "detectionRulesViolated": [
    "6a86a804-4aa6-41fe-a288-aea9a69b458d"
  ],
  "eventType": "violation",
  "message": "Violation detected in confluencedlp",
  "policiesLink": "https://app.nightfall.ai/?intendedRoute=confluence/?policyUUID%5B%5D=ff8bafb7-04ff-4abe-80e0-2bf930c019bf",
  "policiesViolated": [
    "ff8bafb7-04ff-4abe-80e0-2bf930c019bf"
  ],
  "service": "confluencedlp",
  "timestamp": "2022-07-08T14:40:27Z",
  "violationId": "f7e11270-8cf5-42ae-9893-6295661e4730",
  "violationMetadata": {
    "authorId": "62437f828678e9007059b679",
    "authorName": "My User",
    "contentId": "557057",
    "contentTitle": "Detection Testing",
    "contentType": "page",
    "findings": {
      "Credit card number": {
        "VERY_LIKELY": 1
      }
    },
    "permalink": "https://myco.atlassian.net/wiki/spaces/CC/pages/557057/Detection+Testing",
    "snippet": "card, the number is 67*****************. Could you take a lo",
    "workspace": "Myco Central"
  },
  "violationTime": "2022-07-08 14:40:23 +0000 UTC",
  "violationsLink": ""
}
```
{% endtab %}
{% endtabs %}

The following are examples of a sample payload for remediations/actions that were taken on the above mentioned [Nightfall Events](https://help.nightfall.ai/sensitive-data-protection/dashboards_violations/nightfall-events), that will be delivered to the webhook. These are examples from each integration, so the specific fields may vary based on the Nightfall product you are using (e.g. Slack, Github, Google Drive Jira, etc.).



{% tabs %}
{% tab title="Slack" %}


```
{
  "eventType": "remediation",
  "message": "Re: ID 2ec0a7 - Successfully quarantined suspicious message posted by Tehreem Tungekar (tehreem) in #project.",
  "remediationMetadata": {
    "actionType": "quarantine",
    "actionUser": "tehreem",
    "remediationType": "manual"
  },
  "remediationTime": "2022-02-01 18:21:24.173819136 +0000 UTC",
  "service": "slack",
  "timestamp": "2022-02-01T18:22:25Z",
  "violationId": "2ec0a7"
}
```
{% endtab %}

{% tab title="Google Drive" %}


```
{
  "eventType": "remediation",
  "message": "Made file restricted",
  "remediationMetadata": {
    "actionType": "restrict_file",
    "actionUser": "tehreem+sales_enterprise@nightfall.ai",
    "remediationType": "manual"
  },
  "remediationTime": "24 Jan 2022 at 11:54PM UTC",
  "service": "GDrive",
  "timestamp": "2022-01-24T23:54:11Z",
  "violationID": "TGMGNQ"
}
```
{% endtab %}
{% endtabs %}



