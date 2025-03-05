---
description: Learn how to create a Dictionary detector in Nightfall.
---

# Creating Dictionary Detector

A dictionary detector can detect a specific piece of sensitive data (referred to as a token). The token can be any type of sensitive data like a password, API key, IP address, PII, and so on. You must add the token to a file and then upload the file while creating the dictionary. Nightfall scans your data to check if the token present in the uploaded file exists in your data. If a match is found, it fis flagged as sensitive data exposure.&#x20;

To create a Dictionary Detector:

1. Navigate to the Detectors section from the left pane.
2. Click **+ Custom Detector** and select **Dictionary**.&#x20;

<figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

3. Enter a name for your custom Detector in the **Name** field.&#x20;
4. (Optional) Enter a description for the Detector in the **Description** field.
5. Upload or drag and drop the text file which contains a token.
6. (Optional) Select the **Match substrings** check box to match the sub-strings of the text file.
7. Click **Add**.

<figure><img src="../../.gitbook/assets/image (65).png" alt="" width="563"><figcaption></figcaption></figure>
