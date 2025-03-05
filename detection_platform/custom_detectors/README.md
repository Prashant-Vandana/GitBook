---
description: Learn how to create custom detectors in Nightfall.
---

# Creating Custom Detectors

Nightfall allows you to create custom detectors that match your organization's requirements. If none of the existing Nightfall detectors match your requirements, you can use this option to create a custom detector.&#x20;

Nightfall provides you with four types of custom detectors.&#x20;

* **Dictionary**: This Detector allows you to upload a text file. The text file must have a specific token which is sensitive data for your organization. The Detector looks for this token in all the data and if a match is found, it flags it as sensitive data found.&#x20;
* **File Type**: This Detector allows you to select a [MIME](https://www.geeksforgeeks.org/multipurpose-internet-mail-extension-mime-protocol/) (Multipurpose Internet mail extension). (roughly speaking, every file on the Internet is recognized by its format which is called MIME). The Detector scans all your data to check if it has a file with the selected MIME type.
* **File Fingerprint**: This Detector accepts a file as input. You can add all the content that you feel is sensitive to your organization. The detector uses this file as the base and scans your data to check if any matching content is present. If found, it flags it as sensitive data.&#x20;
* **Regular Expression**: This Detector allows you to define regular expressions matching the [RE2 syntax](https://github.com/google/re2/wiki/Syntax/). The Detector scans all your data to find any content that matches the regular expression. If found, it flags it as sensitive data.&#x20;
* **Extend a Nightfall Detector**: This Detector type allows you to customize an out-of-the-box Detector by defining Context Rules and Token rules.

{% hint style="info" %}
Apart from the above custom Detectors, you can also use the **Request a new detector** option to request an entirely new custom Detector created by Nightfall.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
To view only custom detectors created by you, click the CUSTOM filter in the left pane.&#x20;
{% endhint %}

<figure><img src="../../.gitbook/assets/image (63).png" alt="" width="563"><figcaption></figcaption></figure>

To learn more about how to create each of the custom detectors, you can refer to the following documents.&#x20;

* [dictionary\_detector.md](dictionary_detector.md "mention")
* [file\_type\_detector.md](file_type_detector.md "mention")
* [file\_fingerprint\_detector.md](file_fingerprint_detector.md "mention")
* [regexp\_detector.md](regexp_detector.md "mention")
* [extend\_nightfall\_detector.md](extend_nightfall_detector.md "mention")

