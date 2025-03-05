---
description: >-
  Learn about various factors to be considered while choosing a Nightfall
  detector.
---

# Choosing a Nightfall Detector

One of the first things you’ll do to get started with Nightfall is to choose which detectors you want to use. Ultimately, you will organize your chosen Detectors into [Detection Rules](../create_detection_rules.md) in order to apply them to your cloud applications and infrastructure - but beforehand, we recommend that you carefully assess your needs and goals for sensitive data detection. Below, we suggest a few questions to ask yourself as you determine which detectors to leverage.

**What data do you want to detect?**

As discussed above, there is always a tradeoff between sensitivity and specificity. You want to plan your Detection Rules carefully to strike the right balance of accuracy without too much noise. The main question to ask yourself at this stage is what data you want to look for.&#x20;

* Do you have a specific concern around a particular type of data (e.g. from a previous DLP issue)? In this case, you may be able to target a limited set of detectors.
* Do you want to implement a very broad DLP process, and don’t have a sense of which data might be problematic? Doing so will require more detectors, and thus means you may find a higher number of violations and/or noise.

Try to limit your detectors to data that you know or suspect are tracked or shared at your organization. For example, if you never discuss or store Vehicle Identification Numbers, then you likely do not need to set up a detector for that type of data.

**How severe are the consequences of data leakage?**

Some detectors will give more false positives due to their nature (e.g. widely occurring data types such as Dates, or less structured data types such as Names). In order to avoid excessive noise, you should weigh the relative risk of data exposure. For example, it may be problematic for your organization to leak Credit Card Numbers, but not Dates.&#x20;

**How much does the data’s context matter?**

Another way to eliminate noise is to create specific Detection Rules that scan for combinations of data types. For example, it may be problematic for your organization to have Dates appearing alongside Names, but not for Dates to appear alone.
