---
description: Learn about Nightfall detectors.
---

# Detectors

A Detector is a tool that scans any online entity to detect if any sensitive data is present in the entity. An "entity" can refer to any resource on the Internet like a file in Google Drive, ticket data in JIRA, code snippets in GitHub, customer data in Salesforce, and so on.&#x20;

There are two types of detectors; Nightfall Detectors and Custom Detectors.&#x20;

## Nightfall Detectors

Nightfall provides core machine learning-powered detectors known as **Nightfall detectors**. All the detectors provided by Nightfall, are provided out-of-the-box and are present in your Nightfall environment by default. You can navigate to the **Detectors** section in the left menu and select the **BUILT BY NIGHTFALL** option to view all the Detectors provided by Nightfall.&#x20;

<figure><img src="../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

Each Nightfall detector is designed to identify a specific type of sensitive data. For instance, The **Email detector** can identify Email IDs. You can use this detector to check if any Email IDs from your organization are being leaked out on the Internet.&#x20;

Similarly, there are detectors to detect personally identifiable information (PII) from various countries. The PII of each country is unique. For instance, French passport numbers have a different format as compared to German passport numbers. So, if you are a French company that wishes to detect if any of the French passport numbers of your employees or customers are leaked or are prone to be leaked, you can use the **France Passport** detector. Similarly, German companies can use the **Germany Passport** detector.&#x20;

The detectors are classified in terms of the sensitive data that they protect. The various categories under which Nightfall detectors are classified are as follows.

<figure><img src="../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

* **Common Entities:** This category consists of detectors that uniquely identify a person. The detectors in this category are **Name**, **Email**, **Address**, and **Phone number**.&#x20;
* **Content Moderation**: This category consists of detectors that can identify harmful data in images. The detectors in this category are **Violent or Disturbing Image** detector which can detect violent content from images and **Sexually Explicit Image** detector which can identify sexual activity in images.
* **Documents:** This category consists of detectors that can identify sensitive data in images. Some of the detectors in this category are **Credit Card image** detector which can detect credit card numbers from images and **Passport or Visa Image** detector which can detect passport numbers or visa numbers from images.
* **Finance - Banking**: This category consists of detectors that can identify sensitive data related to the financial industry. Some of the detectors in this category are **Canada Bank Account Numbe**r detector which can detect bank account numbers from Canada and the **IBAN code** detector which can detect the IBAN codes.&#x20;
* **Financed - PCI**: This category consists of detectors that can identify sensitive data related to payment cards. **Credit card numbers** is one such detector that falls under this category and identifies the credit card numbers of customers.&#x20;
* **Network/Hardware:** This category consists of detectors that can identify sensitive data related to hardware and networking. The **IP address** detector in this category can identify IP addresses.&#x20;
* **Healthcare:** This category consists of detectors that can identify sensitive data related to the healthcare industry. The **Protected Health Information** (PHI) detector can identify data that can uniquely recognize a person.&#x20;
* **Personally Identifiable Information (PII) - Americas:** This category consists of detectors that can identify sensitive data that can uniquely identify citizens from various countries of the American continent. Some of the detectors in this category are the **Canada Driver License Number** detector which can identify driving license numbers issued to Canadian citizens and residents, **US Driver license** detector which which can identify driving license numbers issued to US citizens and residents.
* **Personally Identifiable Information (PII) - EMEA/AP:** This category consists of detectors that can identify sensitive data that can uniquely identify citizens from various countries in Europe and Asia Pacific. The Indian **Aadhar Card number** detector is a part of this category that can identify the Aadhar numbers of Indian citizens.&#x20;
* **Secrets:** This category consists of detectors that can identify user's sensitive data. The **API key** detector can identify live API keys exposed to the Internet.&#x20;

{% hint style="info" %}
To view the detectors of a specific category, click the category name. All the Nightfall detectors' category names are highlighted in the above image.&#x20;
{% endhint %}

For the complete list of all the detectors present in all the categories, you can view the [detection\_glossary](detection_glossary/ "mention") document.&#x20;

Now that you are aware of all the available detectors, you can choose to use any of the existing Nightfall detectors or create your detector specific to your organization's requirements. If you are not sure of which Nightfall detector to use, view the [choosing\_detectors](choosing_detectors/ "mention") document.&#x20;

If Nightfal detectors can address your organization's requirements and you do not wish to create any custom detectors, you can refer to the [create\_detection\_rules.md](create_detection_rules.md "mention") document, to learn about how to add detectors to a detection rule.

If Nightfall detectors cannot address your organization's requirements, you can create your own detector(s) or customize a Nightfall detector. You can refer to the [custom\_detectors](custom_detectors/ "mention") document to learn about custom detectors.&#x20;



