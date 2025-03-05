---
description: >-
  Learn how Nightfall assigns confidence levels to sensitive data
  classifications.
---

# What do different “Confidence Levels” mean?

Detection results are comprised of two parts:

1. A data type **detector** that was scanned for (either a Nightfall detector or a custom regex detector). For example, a Credit Card Number.
2. A **confidence** that the scanned data matches the specific info type. For example, a “Very Likely” match.

Confidence may be any of the following values corresponding to the given intervals:

| **Likelihood**                            | **Probability Threshold** | **Interpretation**                                       |
| ----------------------------------------- | ------------------------- | -------------------------------------------------------- |
| POSSIBLE (“Possible”)                     | 40%+                      | “It is possible that the data matches the info type.”    |
| LIKELY (“Likely”)                         | 60%+                      | “It is likely that the data matches the info type.”      |
| <p>VERY_LIKELY </p><p>(“Very Likely”)</p> | 80%+                      | “It is very likely that the data matches the info type.” |

Each info type is unique, so it is not possible to dictate that what yields a “Very Likely” match for one detector, will yield a “Very Likely” result for another. Nonetheless, we can provide some high-level guidance. Generally speaking, higher confidence detections may have certain features that increase confidence in the detection being accurate - some examples of the features include:

* Formatting of token
* Passes validation functions
* Passes substring checks
* Context clues that are indicative of that info type

You can learn more about these specific features and how detection works in [**How does detection work?**](https://help.nightfall.ai/nightfall-ai/detection-engine/how-detection-works)

Minimum confidence may be specified as part of any condition in the Nightfall Detection Engine. In the Nightfall scan API and Atlassian integrations, the confidence is returned to the end-user as part of the results. In Nightfall’s Slack and GitHub integrations, the confidence is not returned with the results at this time. You can tune the accuracy of the results by adjusting the confidence thresholds in the Nightfall dashboard.

## What should I use for the Minimum Confidence setting in my Detection Rules? <a href="#h_ba96562962" id="h_ba96562962"></a>

For pre-built detectors, a “Possible” confidence level is triggered by the appearance of the token, without considering context, whereas “Likely” and “Very Likely” take context into account. When a custom regex is detected, its Confidence Level is assessed as “Likely” - you may determine how the Confidence Level adjusts from there based on context.

Of course, there is a tradeoff - a lower Confidence Level may result in more noise. **We highly recommend setting the Minimum Confidence of every detector to Likely or Very Likely in order to reduce noise and focus your DLP efforts on priority violations.** Setting your detectors to Possible or below will lead to many more findings and is best suited for scenarios in which risk tolerance is very low, or for special / advanced use cases that involve optimizing for reducing false negatives.

When setting confidence thresholds, also consider how structured the data tends to be. For example, a Social Security Number or Credit Card Number has a very typical structure and false positives may be less likely - so you could decrease the confidence threshold in order to implement a very conservative policy. On the other hand, less structured data such as Names could result in more false positives, and thus you may want to increase the confidence threshold.
