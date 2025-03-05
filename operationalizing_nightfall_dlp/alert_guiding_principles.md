---
description: Follow Nightfall's best practices for Alert Management and Remediation
---

# Alert Management Guiding Principles

## Sensitive **data cannot live in any of these applications and must be remediated**

As a best practice, any alerts that contain real, sensitive data should be remediated as soon as possible. This will minimize your security risk and will help set the tone for your DLP strategy moving forward. It is also encouraged to [annotate findings](https://help.nightfall.ai/nightfall-ai/dashboards_violations/nightfall-violations#annotating-findings) within the violation for easy reference, efficient collaboration and detector model improvements.

## **No action is needed on sample data, test data, or data used in instructions or guides ("expected data")**

To lessen the load of which alerts need to be remediated, a best practice is to not take action on sample data or test data. Instead you can [annotate](https://help.nightfall.ai/nightfall-ai/dashboards_violations/nightfall-violations#annotating-findings) such data as false positives for easy reference and model improvements.  Remediation should only be a focus for sensitive data that is found through the alerts.&#x20;

## **Acknowledge an alert, when reviewed, to avoid duplication of efforts**

If you already are reviewing an alert, it should be acknowledged to avoid duplicate efforts.

