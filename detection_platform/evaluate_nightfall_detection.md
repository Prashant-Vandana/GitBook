---
description: Learn how to evaluate detection rules in Nightfall.
---

# Evaluating Detection

In order to evaluate the success of your cloud DLP detection, you must first have clarity around your organization’s goals. This will be highly dependent on your organization’s unique circumstances and needs.&#x20;

Here are some guiding questions:

* What sensitive data would you like to detect and which are the highest priorities for each SaaS application?
* What level of risk are you comfortable with? Would you like to alert on only the most risky findings or have visibility into even low-risk data types that may not warrant action?
* How much operational load are you willing to take on? The more granular your approach, the less human discretion will be required in the filtering and remediation steps.
* What are the requirements of any compliance regimes you are accountable to?
* What user strategy would you like to implement?
  * Some potential answers:
    * Minimal impact on user experience, only alerting and monitoring to security staff and notifications to end users to guide towards remediation?
    * Educating and empowering users about DLP best practices?
    * Enforcing DLP through strict controls and automation?

### Testing Detection Rules

Once you have a sense of your goals, we recommend that you optimize your detection during a phased, iterative implementation - start small, and broaden gradually. Typically, the biggest pitfall customers want to avoid during implementation is to get flooded by too many low-priority alerts that become unmanageable - which is typically caused by taking too broad of an approach to detection. By taking the time to optimize your detection gradually during the first few weeks, your team will be set up for ongoing success.&#x20;

For this reason, we have created our Detection Wizard, which is a resource that will recommend the exact configuration to suit your use cases. You can shortcut a lot of legwork in choosing and fine-tuning rules by immediately identifying the recommended and validated configuration that matches your use case.

There is generally little reason to deviate from the Wizard’s recommendations at the outset, but your use case may warrant fine-tuning and broadening your detection logic over time:

We recommend that you select just a few detectors to start out with as recommended by the Wizard, in order to optimize detection of the most critical and high-risk information types.&#x20;

* Once a few detectors and initial detection rules are in place, test some sample data and monitor the results. We suggest you evaluate metrics such as false positive and false negative rates, and assess whether the volume of alerts/results is manageable by your team. You may adjust parameters such as Minimum Confidence and Minimum Number of Findings to optimize the level of alerts through your testing process.
* Then, continue to iterate and modify your detection by adding and optimizing a few more detectors as required. Focus on starting with tighter detection rules (higher confidence levels), and slowly relax or broaden the rules over time.&#x20;

### Sample Data

Nightfall offers a library of [Sample Data](https://help.nightfall.ai/nightfall-ai/nightfall-detection-and-policy-templates/nightfall-sample-data-sets) that we recommend for evaluating DLP technologies.&#x20;

### Evaluating Detection During Tests vs. in the Wild

It’s important to understand that the rate of true positive data “in the wild” tends to be significantly lower than true positive data in a test environment. That’s because, in a test environment, many occurrences of sensitive information will be intentionally planted.&#x20;

As a result, test environments are typically most useful for optimizing sensitivity, or the true positive rate - detection is optimized toward identifying sensitive information as sensitive. While this helps ensure that occurrences of sensitive information are, in fact, correctly flagged, it also means detection is somewhat skewed toward flagging information as sensitive, thus increasing the potential for false positives (see [the tradeoff between sensitivity and specificity](https://help.nightfall.ai/nightfall-ai/detection/how-detection-works#understanding-accuracy)).&#x20;

What this means for you is that if you fine-tune a detection rule in a test environment, you may over-index towards sensitivity rather than specificity, which can result in a higher degree of false positives in the wild. As a result, we highly recommend evaluating detection rules in a production environment rather than a test environment, when possible.

\
