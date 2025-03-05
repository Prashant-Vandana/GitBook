---
description: Learn more about PCI compliance and how Nightfall helps with it.
---

# PCI Compliance + DLP

Payment card industry (PCI) compliance is mandated by credit card companies to help ensure the security of credit card transactions in the payments industry. Payment card industry compliance refers to the technical and operational standards that businesses follow to secure and protect credit card data provided by cardholders and transmitted through card processing transactions.&#x20;

Financial data, especially credit card numbers, pose an obvious DLP risk. Banks, financial institutions, and others concerned with protecting financial data typically use Nightfall’s payment card detectors.

#### PCI DSS Version 3.2.1 <a href="#docs-internal-guid-39f52358-7fff-b8f3-1ab9-4d18ee5e5b46" id="docs-internal-guid-39f52358-7fff-b8f3-1ab9-4d18ee5e5b46"></a>

Appendix 3.2.6 states the requirement for DLP applicable to ALL PCI-covered entities, making this the strongest case for Nightfall. As written:

* Appendix 3.2.6 - Mechanisms are implemented for detecting and preventing clear text PAN from leaving the cardholder environment.
* Note that PCI’s example given explicitly states DLP: “Mechanisms to detect and prevent unauthorized loss of cleartext PAN \[credit card number] may include the use of appropriate tools such as data loss prevention (DLP) solutions as well as manual processes and procedures.”

The following PCI DSS sections further supported the need for a DLP:

**3. Protect Stored account Data.** specified that cardholder data must be protected at rest. Nightfall can identify when such data is being stored somewhere where unauthorized access has or may occur.

**7. Restrict access to system components and cardholder data by business need to know.** Same as above point. Nightfall can determine when need-to-know access might be violated.

**10. Log and monitor all access to system components and cardholder data.** Same as above, while Nightfall is not an access control, within certain integrations Nightfall can help determine who has had access to a specific piece of data.

**12. Support information security with organizational policies and programs.** Nightfall can help teams build enforceable information security policies.

\


