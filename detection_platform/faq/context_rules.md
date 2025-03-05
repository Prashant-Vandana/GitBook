---
description: Customize finding confidence to suit your business logic
---

# How do I use Context Rules?

Context Rules are a way to tune detectors and increase their sensitivity by up-weighting or down-weighting detection of a sensitive finding based on its surrounding context. Contrary to Exclusion Rules, which will disqualify “tokens” or items from detection, Context Rules are a way to increase or decrease the Confidence Level in your detections if there are certain types of tokens, also known as “hot words”, that surround the sensitive token.

For example, let’s say you are detecting the Social Security Number “489-36-8350”. If you see “MyCo Test SSN is 489-36-8350” you may want to lower the Confidence Level of this alert because you know this is a test or invalid SSN. Alternatively if you see “MyCo Customer SSN: 489-36-8350” you may want to upweight this confidence level because you know that at your company SSNs are real when they are formatted in this way. In this way, Context Rules help adapt detectors to specific business context relevant to you.

Context Rules are based on a regular expression (a known pattern to match against, also known as a “regex”) that you can create. They follow RE2 syntax listed [here](https://github.com/google/re2/wiki/Syntax). You can test your regular expression [here](https://regoio.herokuapp.com/).

Context Rules can be added to any detector (either pre-made by Nightfall or to your own custom regex). You can control how many characters surrounding a finding define its context, and adjust how the original confidence level is affected by this context.

Here’s how you can build your own Context Rule and attach it to a detector:

1. Enter a regex pattern for your context rule. If you wish the pattern to be case sensitive, check the box to the right of the input window.
2. Define the window to be considered as context by specifying the number of characters away to look for your regex pattern and whether to consider context before the discovered token, after it, or both.
3. Define the confidence adjustment for your context rule from the dropdown menu. If your context rule is triggered, the finding will automatically be adjusted to your selected confidence level.
4. Add your Context Rule to the detector by clicking the "Save" button in the lower right.

[![](<../../.gitbook/assets/New Context Rule Rev.png>)](https://nightfall.intercom-attachments-7.com/i/o/277232625/602c8560e7798cb9670dccd4/hGEpMlFh8WboVlyWTiWk1dz7_QbzpUAK8PLDlfb9SsJiqkkKYbXDsjb9u50l7FNPsefxfDdjcfnrDN1j_BjGci6rbkE87J-riByL3c3WEKdi6eYwUramqBNVQcMF7ZGmtkECW7Gc)
