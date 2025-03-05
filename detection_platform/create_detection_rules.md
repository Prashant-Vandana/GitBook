---
description: Learn the process of creating detection rules in Nightfall.
---

# Create Detection Rules

As described in the [Broken link](broken-reference "mention") once you have finalised the the Detectors to be used or created custom detectors which leverage your organization's sensitive data security requirements, you must add the detectors to a detection rule and then add the detection rule to a policy. You cannot use detectors directly. Detectors become useful only when you add them to a Detection rule and then add the detection rule to a policy.&#x20;

You can add multiple detectors to a single detection rule. Nightfall does not restrict you on the type of detector that can be added to a detection rule. You can add both, a custom detector and a Nightfall detector to the same detection rule.&#x20;

You can create multiple detection rules to detect different types of sensitive data. For example, you can add the Password detector to a Detection rule and use it to detect password leaks. You can add the API key detector to another detection rule and use it for detecting API key leaks.&#x20;

Once you add all the required detectors to the detection rule, Nightfall allows you to test the detection rule in the Nightfall Playground. You can use the Nightfall playground only for testing if the detection rule works as expected. Once you confirm that the detection rule works as expected, you must add the detection rule to policy to leverage your data security requirements. Conversely, you can also have a single detection rule in which you add both Password and API key detectors.&#x20;

You can access the Detection rules page by clicking **Detection** from the left pane and then clicking **Detection Rules**. To create a new Detection rule, you must click the **+ New Detection Rule** button the top right corner.&#x20;

<figure><img src="../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
If you wish to get guidelines from Nightfall on what detectors must be included in your detection rules, refer to the [detection\_rules.md](../nightfall_policy_templates/detection_rules.md "mention") document.&#x20;
{% endhint %}

## Adding Detectors to Detection Rule

You can add a Detector to the Detection rule by executing the following steps.&#x20;

1. Click the **+ New Detection Rule** button the top right corner.
2. Enter a name for the detection rule in the **Name** field.
3. (Optional) Enter a description for the detection rule in the **Description** field.&#x20;
4. Click **+ Add Detectors** to add detectors to the detection rule.

<figure><img src="../.gitbook/assets/image (352).png" alt=""><figcaption></figcaption></figure>

5. Select the check box for the detectors that you wish to add to the detection rule. You can use the filters to view only the Nightfall detectors or the custom detectors or the search bar to search detectors.&#x20;
6. Click **Add**.

<figure><img src="../.gitbook/assets/image (353).png" alt=""><figcaption></figcaption></figure>

You can see that the selected detectors are added to the detection rule. In the following image two detectors have been added to the Detection rule.&#x20;

<figure><img src="../.gitbook/assets/image (354).png" alt=""><figcaption></figcaption></figure>

## Detection Rule Settings

Once you add the required detectors to the detection rules, you can se that there are three columns; **Scope**, **Minimum Confidence**, and **Minimum # of Findings**. These settings define the weightage of the detector in the detection rule. You must configure these settings for each detector.&#x20;

These settings are explained in the following sub-sections.

### Scope

The Scope setting allows you to define which part of the data the detector must scan. You can configure this setting to scan either the name of the file, the contents of the file or both.&#x20;

<figure><img src="../.gitbook/assets/image (355).png" alt=""><figcaption></figcaption></figure>

If you select the **Content** option, this detector only scans the content of the files and not the name of the file, and vice versa, if you select **File Name**. However, if you select **Both**, the detector scans the file name as well the contents of the file.&#x20;

For example, if the API key detector has to scan a Google Drive file and if you select, **File Name**, then the detector only scans the name of the file to check if the name has any API key. Similarly, if you select **Content**, then the detector only scans the content of the file and not the name. If you select **Both**, then the detector scans both; the name and the contents of the file.&#x20;

{% hint style="success" %}
**Important**

If you wish to scan content that is not part of any file, you must either select the **Content** or **Both** option.

For example, if you wish to scan direct messages or group messages from Slack or MS Teams, these messages are not part of any files. In such cases, if you select the **File Name** option, the detector does not detect any violation because it considers direct messages as Content not part of any file. Hence to scan such types of content you must select either **Content** or **Both** options.&#x20;
{% endhint %}

### Minimum Confidence

The minimum confidence setting defines the probability of a detector's findings being actual violations. Nightfall provides you with three Minimum Confidence settings; Possible, Likely, and Very Likely. &#x20;

<figure><img src="../.gitbook/assets/image (356).png" alt=""><figcaption></figcaption></figure>

The **Possible** option indicates that there is a **40-60%** chance of the Detector's finding being an actual case of data leak, Similarly, the **Likely** option indicates that there is a **61-80%** chance of the Detector's finding being an actual case of data leak. The **Very Likely** option indicates that there is a **81-100%** chance of the Detector's finding being an actual case of data leak.

You can set the Minimum Confidence setting for each detector. When the detector detects any data leak, it is logged in the [sdp\_events](../dashboard/sdp_events/ "mention") page with the Minimum Confidence setting configured here.&#x20;

### Minimum Number of Findings &#x20;

This setting defines the minimum number of data leak cases that a detector must encounter for it to be considered as a Violation by the Detection rule. You must configure this setting for each detector.   For example, if you set this setting to 10, the detection rule does not consider the first 9 occurences of data leak encountered by the detector. Detection engine starts considering the 10th and all subsequent cases of data leak to be actual case of violations.&#x20;

## Applying Logical Operators Between Detectors

If a detection rule has a single detector and if that detector detects a data leak, the detection rule is triggered and it is logged as a Finding.&#x20;

However, when you have multiple detectors in detection rule, you can choose to trigger the detection rule when any of the detector detects a data leak or when all the detectors detect a data leak.&#x20;

<figure><img src="../.gitbook/assets/image (357).png" alt=""><figcaption></figcaption></figure>

As you can see in the above image, you can choose the flag a Finding of the detection rule either when any single detector detects a data leak or when all the detectors of the detection rule detect a data leak.&#x20;

## Understanding When the Detection Rule Triggers

<figure><img src="../.gitbook/assets/image (358).png" alt=""><figcaption></figcaption></figure>

The above image has two detectors. The following statements hold good.&#x20;

* The Scope of both the detectors is set to scan the file content and file name.&#x20;
* When any of these detectors detect a data leak, it is logged as a Finding in the Violations page and tagged as Very Likely.&#x20;
* The minimum number of findings for each detector is 1. So even if there is a single case of a data leak, a detector rule considers it as a finding.
* The detection rule is triggered even if a single detector detects a data leak.

## Testing Detection Rules in Nightfall Playground

Once you create the detection rule, it is highly recommended that you test the rule to ensure that it returns the expected results, when added to policies. Nightfall provides you with a Playground to test the detection rules.&#x20;

### Prerequisites to use Nightfall Playground

* You must have an API key to use the Nightfall Playground. You can [refer to this document](https://help.nightfall.ai/nightfall-developer-platform/getting-started-with-developer-platform/creating-api-key) to learn about how to create an API key.
* You must have some sample data to test the Detection rule. This [Nightfall document](https://help.nightfall.ai/nightfall-ai/nightfall-detection-and-policy-templates/nightfall-sample-data-sets) has various types of sample data sets that you can use.&#x20;

### Capturing Detection Rule UUID

Each Detection rule in Nightfall has a UUID. This is a unique ID assigned to each detector when it is created. You cannot edit the UUID of any detector. You must capture this UUID to use it in Playground to test the detection rule.

To capture Detection rule UUID:

1. Navigate to Detection rules.
2. Click the detection rule whose UUID has to be captured.&#x20;
3. Click the UUID to copy it.

<figure><img src="../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>

### Using the Nightfall Playground

To use the Nightfall playground:

1. Navigate to the [Nightfall playground](https://playground.nightfall.ai/).
2. Use either the **I'm Scanning Text** or **I'm Scanning Files** tab based on whether you wish to scan text or file.

<figure><img src="../.gitbook/assets/image (734).png" alt=""><figcaption><p><br></p></figcaption></figure>

{% tabs %}
{% tab title="Scanning Text" %}
1. Replace the existing sample data with your sample data in **Step 1: Payload.**

<figure><img src="../.gitbook/assets/image (741).png" alt=""><figcaption></figcaption></figure>



2. Skip **Step 2: Pick Detection rule**.&#x20;
3. Expand **Advanced Detection Settings (Optional)**

<figure><img src="../.gitbook/assets/image (742).png" alt=""><figcaption></figcaption></figure>

4. Paste the Nightfall API key in the **Nightfall API Key** field.&#x20;
5. Paste the Detection rule UUID in the **Detection Rules** field.&#x20;
6. Click **Start Scan.**

<figure><img src="../.gitbook/assets/image (743).png" alt=""><figcaption></figcaption></figure>

If sensitive data is found in the sample data, the Findings section looks as shown in the following image.

<figure><img src="../.gitbook/assets/image (744).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Scanning Files" %}
1. Paste the file URL or upload the file in **Step 1: Files to scan**.&#x20;

<figure><img src="../.gitbook/assets/image (745).png" alt=""><figcaption></figcaption></figure>

2. Enter the Email to which the scan results must be sent in the **Step 2: Email** field.

<figure><img src="../.gitbook/assets/image (746).png" alt=""><figcaption></figcaption></figure>

3. Skip **Step 2: Pick Detection rule**.&#x20;
4. Expand **Advanced Detection Settings (Optional)**

<figure><img src="../.gitbook/assets/image (747).png" alt=""><figcaption></figcaption></figure>



5. Paste the Nightfall API key in the **Nightfall API Key** field.&#x20;
6. Paste the Detection rule UUID in the **Detection Rules** field.&#x20;
7. Click **Start Scan.**

<figure><img src="../.gitbook/assets/image (748).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}







###



