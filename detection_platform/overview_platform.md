---
description: Understand how detection works in Nightfall.
---

# Detection Platform Overview

## **What is machine learning?**

Each machine learning detector is a model, which is trained using curated datasets to recognize sensitive data tokens based on certain characteristics (e.g. structure) and on surrounding context (e.g. preceding words). Machine learning models have the ability to automatically learn and improve from experience, without being explicitly programmed - giving them broader scope and higher accuracy than hard-programmed models (such as r[egular expressions](faq/regex_library.md)).&#x20;

## **How do Nightfall’s detectors leverage machine learning?**

Nightfall’s detectors are trained via machine learning to recognize many potential permutations of sensitive data tokens, and also to recognize and assess the surrounding context. The ability to recognize a variety of data structures and context gives Nightfall’s detection far more scope and accuracy than traditional regular expression (regex)-based detection. Nightfall’s internal team of machine learning engineers and data scientists are continuously developing new machine learning-based detectors, and they also handle the ongoing maintenance and training of our detection engine to continually improve accuracy and results.

## **Understanding Accuracy**

A little background on measuring accuracy will be helpful to understand before you embark on your detector optimization journey. Accuracy is the ability of a detector to correctly flag sensitive content and not flag content that is not sensitive.&#x20;

No detector is 100% accurate, and it is possible to have a discrepancy between information that is actually sensitive, and information that is flagged by a detector as sensitive. For example, a detector may incorrectly assess a piece of sensitive content as nonsensitive (this would be a false positive). The various result types you may get, based on the actual versus assessed sensitivity of content, are illustrated below.\


|                               |                     | **Is the Content Actually Sensitive?**                                                                                 |                                                                                                                            |                                                                                                                 |
| ----------------------------- | ------------------- | ---------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
|                               |                     | **Yes (“Positive”)**                                                                                                   | **No (“Negative”)**                                                                                                        | **Row Total:**                                                                                                  |
| **Was the detector flagged?** | Yes (“Positive”)    | True Positive (TP)                                                                                                     | False Positive (FP)                                                                                                        | <p><strong>TP + FP</strong> <br></p><p><strong>(total number of content items flagged by detector)</strong></p> |
| **No (“Negative”)**           | False Negative (FN) | True Negative (TN)                                                                                                     | <p>FN + TN<br></p><p>(total number of content items not flagged by detector)</p>                                           |                                                                                                                 |
|                               | **Column Total:**   | <p><strong>TP + FN</strong><br></p><p><strong>(total number of content items that are actually sensitive)</strong></p> | <p><strong>FP + TN</strong><br></p><p><strong>(total number of content items that are actually not sensitive)</strong></p> | <p><strong>TP + FP + FN + TN</strong><br></p><p><strong>(total number of content items)</strong></p>            |

**Accuracy = (TP + TN) / (TP + TN + FP + FN)**

**Sensitivity = TP / (TP + FN)**

**Specificity = TN / (FP + TN)**

Your organization will, of course, want sensitive data detection to be as accurate as possible. However, it’s important to understand that there is always a tradeoff between accurately identifying true positives (sensitivity) versus accurately identifying true negatives (specificity). &#x20;

* Sensitivity (also known as: recall, hit rate, or true positive rate \[TPR]) is the ability of a detector to correctly identify content with sensitive findings.&#x20;
* Specificity (also known as: selectivity, true negative rate \[TNR]) is the ability of a detector to correctly identify content without sensitive data.&#x20;

The tradeoff between sensitivity and specificity occurs because you must choose whether to optimize a detector toward or away from flagging information. Higher sensitivities mean lower specificities and vice versa. For example, to optimize for sensitivity, you may enable more detectors at lower minimum confidences to catch more true positives. In doing so, you will open yourself up to more false positives, which will lower your specificity.&#x20;

As a result, each organization should spend time optimizing its detectors to strike the right balance between sensitivity and specificity.

## **Confidence Levels**

A confidence level represents Nightfall’s confidence in the accuracy of a given detection. Each detector is a unique model and will have its own confidence level profile. For details on how confidence level is determined for a given detector, please reach out to us.

Confidence may be any of the following values corresponding to the given confidence intervals:

| Likelihood                   | Probability Threshold | Interpretation                                           |
| ---------------------------- | --------------------- | -------------------------------------------------------- |
| POSSIBLE (“Possible”)        | 40%+                  | “It is possible that the data matches the info type.”    |
| LIKELY (“Likely”)            | 60%+                  | “It is likely that the data matches the info type.”      |
| VERY\_LIKELY (“Very Likely”) | 80%+                  | “It is very likely that the data matches the info type.” |

Each info type is unique, so it is not possible to dictate that what yields a “Very Likely” match for one detector, will yield a “Very Likely” result for another. Nonetheless, we can provide some high-level guidance. Generally speaking, higher confidence detections may have certain features that increase confidence in the detection being accurate - some examples of the features include:

* Formatting of token
* Passes validation functions
* Passes substring checks
* Context clues that are indicative of that info type
* Model scoring
