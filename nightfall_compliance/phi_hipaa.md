---
description: Learn how to ensure HIPAA compliance in your collaborative cloud applications
---

# PHI Detector - More on Nightfall's HIPAA Compliance Detector

The Health Insurance Portability and Accountability Act of 1996 (HIPAA) is a federal law protecting the disclosure of individuals' health information (aka _**protected health information**_ or _**PHI**_).

**Nightfall's PHI detector** identifies PHI with high accuracy and relevancy using 15 PII and healthcare entity detectors combined, as described in Tables 1 & 2.

Table 1: _Nightfall PHI_ _detector_ = _Nightfall PII + Healthcare detectors in specfic combinations_

<table><thead><tr><th>PII Group 1</th><th>PII Group 2</th><th>PII Group 3</th><th width="68" align="center">+</th><th>Health Indicator</th></tr></thead><tbody><tr><td>One or more</td><td>Both</td><td>Both</td><td align="center"><br>+</td><td>One or more</td></tr><tr><td><p></p><ul><li>US Social Security Number (SSN)</li></ul><ul><li>Vehicle Identification Number (VIN)</li><li>Device Identifiers</li><li>Medicare Beneficiary Identifier (MBI)</li><li>US Health Insurance Claim Number</li><li>US Individual Taxpayer Identification Number (ITIN)</li></ul></td><td><ul><li>Person Name</li><li>Date of Birth</li></ul></td><td><ul><li>Person Name</li><li>Street Address</li></ul></td><td align="center"><br>+</td><td><p></p><ul><li>ICD10 Code</li><li>ICD10 Description</li><li>Nation Provider Identifier (NPI)</li><li>FDA Drug Name</li><li>FDA Drug Code</li></ul></td></tr></tbody></table>

Please refer to the [detection\_glossary](../detection_platform/detection_glossary/ "mention") for more information on the individual detectors above.&#x20;

Table 2: _Nightfall PHI detection confidence_

| Detection         | Combination Logic                                                                            |
| ----------------- | -------------------------------------------------------------------------------------------- |
| PHI (Very Likely) | PII Group 1, 2, or 3 _AND_ a Health Identifier are found, all with _Very Likely_ confidence. |
| PHI (Likely)      | PII Group 1, 2, or 3 _AND_ a Health Identifier are found, some with _Likely_ confidence.     |

