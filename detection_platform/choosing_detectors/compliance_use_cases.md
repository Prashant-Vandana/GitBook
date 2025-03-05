---
description: >-
  Organizational compliance is one of the leading drivers that require DLP
  tooling such as Nightfall. These are the recommended configurations for each
  compliance framework.
---

# Compliance Use Cases

<table><thead><tr><th width="249.33333333333331">Compliance</th><th>Configuration</th><th>Considerations</th></tr></thead><tbody><tr><td>HIPAA Compliance</td><td><ul><li>Use the <a href="../../nightfall_compliance/phi_hipaa.md"><strong>Protected Health Information (PHI)</strong></a> detector</li><li>Set Minimum Confidence level to <strong>Likely</strong></li><li>Set alert to trigger on <strong>Any</strong> Detectors</li></ul><p><br></p></td><td><ul><li>Depending on the type of healthcare organization, disclosure of personal information may disclose PHI (e.g., a sufficiently uniquely named person going to a health provider like an AIDS clinic would likely disclose the person’s PHI).</li></ul></td></tr><tr><td>PCI Compliance - Text</td><td><ul><li>Use the <strong>Credit Card Number</strong></li><li>Set Minimum Confidence level to <strong>Likely</strong></li><li>Set alert to trigger on <strong>Any</strong> Detectors</li></ul><p><br></p></td><td><ul><li>For greater rigor, set on each of your locale’s detection rules alongside the <strong>Person Name</strong> detector configured to trigger with All Detectors, per:<img src="https://lh4.googleusercontent.com/LnOMqaaiU88kK7vK2Sz-Vc6Qb5cDD_QC8-PQtW3XrovBpYCGmw2RjLTlaY5uo-_lfAgaQTgSGA1_5qUALzgaucR9z4iWC-QPXrTgM6DmD_-lOkEyeJU3wSBu9VPrlwjLvyCZDpGVJ_PqZggLS9rFgQw" alt=""></li></ul></td></tr><tr><td>PCI/PII Compliance - Images</td><td><p></p><ul><li>Use the <strong>Drivers License Image</strong>, <strong>Passport Image</strong>, <strong>US Social Security Image</strong>, <strong>Credit Card Image</strong> detectors</li></ul><ul><li>Set Minimum Confidence level to <strong>Very</strong> <strong>Likely</strong></li></ul><ul><li>Set alert to trigger on <strong>Any</strong> Detectors</li></ul></td><td><p></p><p>These detectors analyze the layout and formatting of content within images, accurately identifying government-issued ID documents from any nation and payment cards from any institution.</p></td></tr><tr><td>ACH Compliance</td><td><ul><li>Use the <strong>US Bank Routing</strong> and <strong>Person Name</strong> detectors</li><li>Set Minimum Confidence level to <strong>Likely</strong></li><li>Set alert to trigger on <strong>All</strong> Detectors</li></ul></td><td><br></td></tr><tr><td>GLBA Compliance </td><td><ul><li>Use the <strong>SWIFT</strong> and <strong>US Bank Routing</strong> detectors</li><li>Set Minimum Confidence level to <strong>Likely</strong></li><li>Set alert to trigger on <strong>Any</strong> Detectors</li></ul></td><td><br></td></tr><tr><td>ISO 27001 Compliance for v2022</td><td><p></p><ul><li><p>Enable all <a href="https://docs.nightfall.ai/docs/detector-glossary#secrets"><strong>Secrets</strong></a> detectors:</p><ul><li>API key</li><li>Cryptographic key</li><li>Database Connection String</li><li>GCP credentials</li><li>Password in code</li></ul></li></ul><ul><li>Set Minimum Confidence level to <strong>Likely</strong></li><li>Set alert to trigger on <strong>Any</strong> Detectors</li></ul></td><td><br></td></tr></tbody></table>



Other detectors that exist are not recommended for use for the above compliance frameworks. For all use cases, Nightfall further recommends:

* Tune and amend Minimum Confidence over time in accordance with your violations and data set
* Scoping should cover all locations where the sensitive data should not be disclosed
* Using Exclusion Rules to reduce false positives and fine-tune alerts
* Reporting false positives for machine learning training to support@nightfall.ai
