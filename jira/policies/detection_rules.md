---
description: >-
  Learn how you can select the required detection rules while creating a policy
  in Nightfall for JIRA.
---

# Select Detection Rules in Nightfall for JIRA

Now you must create the detection rules that define the types of sensitive data that Nightfall scans and capture any violations.

A detection rule can be one detector or a combination of detectors and confidence levels/findings that will define a violation or finding and record it. The following table defines the rules for detectors.

To learn more about Detection Rules and how to set them up, refer [Detection Rules](https://app.nightfall.ai/detection-engine/detection-rules).

Nightfall recommends configuring a simple detection rule to start as shown below.

| Detector                  | Minimum Confidence | Minimum Count |
| ------------------------- | ------------------ | ------------- |
| Credit Card Number        | Likely             | 1             |
| US Social Security Number | Likely             | 1             |
| API Key                   | Likely             | 1             |

To select detection rules, select a detection rule from the list of rules that are displayed and then select one of the following options.

* **All Detection Rules**: Select this option to include all the detection rules in the policy.
* **Selected Detection Rules**: Select this option to include only that detection rule in the policy that you selected above.
* **Unselected Detection Rules**: Select this option to include all the other detection rules in the policy, that you did not select above.

Click **Next**.&#x20;

<figure><img src="../../.gitbook/assets/GIF Recording 2023-11-19 at 6.44.33 PM.gif" alt=""><figcaption></figcaption></figure>
