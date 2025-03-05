---
description: Tips for improving finding accuracy.
---

# How can I reduce false positives in my findings?

Our models learn from diverse data sets, aim for high accuracy, and often perform well. However, customer data sometimes contains new patterns. Think of our models as capable students who excel in some subjects but still have unavoidable gaps in their knowledge. New data may expose gaps.

By reporting these misses, you directly help close knowledge gaps and improve alerting for your company and others.

**Reporting misidentified findings**

If your company is a member of our ML training program, [annotate the false positive in the Violations UI](https://help.nightfall.ai/nightfall-ai/dashboards_violations/nightfall-violations#annotating-findings). Your annotated sample will be added to our ML data set and used in upcoming model re-training.

If not an ML training program member, please send us anonymized samples without changing the key pattern.

Reach out to [support@nightfall.ai](mailto:support@nightfall.ai) for more information about our ML training program.

If the customer needs a fix urgently, many cases can be addressed by [extending a Nightfall detector](https://help.nightfall.ai/nightfall-ai/detection-engine/creating-custom-detectors/extend-a-nightfall-detector). if you need help, please don’t hesitate to ask for help.

**Reporting missed sensitive data.**

Please provide us with anonymized samples without changing the key pattern.

If anonymization is impossible, coordinate with us to send the data using a secure tool like [Keybase](https://keybase.io/).

With the Nightfall Detection Engine, there are various ways you can improve the accuracy of detection:

1. Share your false positives with Nightfall[.](mailto:support@nightfall.ai) We'll identify the issue and retrain our models. If your company is a member of our ML training program,  [annotate the false positive in the Violations UI](https://help.nightfall.ai/nightfall-ai/dashboards_violations/nightfall-violations#annotating-findings). Your annotated sample will be added to our ML data set and used in upcoming model re-training. If not an ML training program member, please send [us](https://www.notion.so/ecb337d83dd04cb9bda7b498cc14d706?pvs=21) anonymized samples without changing the key pattern. Reach out to [support@nightfall.ai](mailto:support@nightfall.ai) for more information about our ML training program.
2. Modify the detector using an exclusion rule recognizing known test or mock values. Read more about _exclusion rules_ in [How do I use Exclusion Rules?](https://help.nightfall.ai/nightfall-ai/detection-engine/detection-engine-faqs/how-do-i-use-exclusion-rules)
3. Modify the detector using a context rule recognizing common patterns in the text surrounding the sensitive token. Read more about _context rules_ in [**How do I use Context Rules?**](https://help.nightfall.ai/nightfall-ai/detection-engine/detection-engine-faqs/how-do-i-use-context-rules)
4. Increase the detector's minimum confidence to “Likely” or “Very Likely”. Read more about detector _confidence levels_ in [**What do different “Confidence Levels” mean?**](https://help.nightfall.ai/nightfall-ai/detection-engine/detection-engine-faqs/what-do-different-confidence-levels-mean)
5. Set up the Detection Rule’s to trigger when each entity type is found. Common Entities such as names, addresses, phone numbers, and emails are found everywhere and are generally not sensitive unless found in combination.
6. Set up policies appropriate to the scanned data source - i.e. integration, channel, folder, instance, etc. For example with Slack Enterprise, you can enable or disable detection in private channels, direct messages by channel ID, workspace ID, or in all private channels & DMs. Reach out to [support@nightfall.ai](mailto:support@nightfall.ai) and we will help.
7. Increase the Detection Rule’s minimum number of findings threshold. For example, when trying to detect phone list sharing, set you detection rule to ony trigger alerts when seeing 10 or more person names and phone numbers.
