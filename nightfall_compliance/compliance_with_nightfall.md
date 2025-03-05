---
description: >-
  Learn how Nightfall AI-powered data leak prevention (DLP) for SaaS and Cloud
  can help organizations maintain compliance with various global compliance
  frameworks across different industries.
---

# How Nightfall Fits into Compliance Frameworks

This article discusses how Nightfall, the AI-powered data leak prevention (DLP) platform for SaaS and cloud, can help organizations maintain compliance with various global compliance frameworks across different industries. It provides an overview of Nightfall detection and its pre-built detectors. It then delves into specific compliance frameworks such as GDPR, CCPA, HIPAA, HITRUST, PCI, GLBA/FCRA, SOX, ISO 27001, FERPA, CMMC, and FedRAMP/NIST 800-53, and explains how Nightfall can help organizations comply with the specific requirements of each framework. The article also includes links to additional resources for each compliance framework.

Please note that while these specific frameworks and controls may be relevant to DLP, it is essential to consult the full text of these frameworks and any applicable regulations or guidelines to ensure comprehensive compliance with the law. The information presented here should not be considered legal advice or a confirmation of compliance with any specific laws or regulations. Legal advice specific to your situation is recommended to understand the complete obligations and requirements of these frameworks.

## **Nightfall Detection**

Nightfall comes with many pre-built detectors out of the box. You also have the ability to add custom detectors, rules, keywords, and regexes. To explore our pre-built detectors, visit our [Detector Glossary](https://docs.nightfall.ai/docs/detector-glossary).

## Data Privacy

### **GDPR**

The General Data Protection Regulation (GDPR) operates under the principle of data protection by design and by default. This requires organizations to implement appropriate technical and organizational measures to ensure the protection of personal data. Specifically, Data Leak Prevention (DLP) solutions can be used to detect and prevent unauthorized transmission or storage of personal data, such as names, addresses, and personal identification numbers.

The specific controls are:

* Article 32: Security of processing, which requires organizations to implement appropriate technical and organizational measures to ensure a level of security appropriate to the risk. **Nightfall is a control to protect personal data from unauthorized access, alteration, destruction, or accidental loss.**
* Article 5(1)(f): Data minimization, which requires organizations to limit the collection and retention of personal data to what is necessary for the specific purposes for which it is processed. **Nightfall’s realtime monitoring can help organizations to identify and prevent the retention of unnecessary personal data.**
* Article 33: Notification of a personal data breach to the supervisory authority, which requires organizations to report personal data breaches to the appropriate supervisory authority without undue delay and, where feasible, not later than 72 hours after having become aware of it, unless the personal data breach is unlikely to result in a risk to the rights and freedoms of natural persons. **Nightfall’s realtime monitoring enables organizations to detect and respond to personal data breaches in a timely manner.**
* Article 35: Data protection impact assessment (DPIA), which requires organizations to carry out a DPIA when the processing is likely to result in a high risk to the rights and freedoms of natural persons. **Nightfall helps organizations to identify and mitigate risks to personal data by detecting and preventing data breaches.**

### **CCPA**

The California Consumer Privacy Act (CCPA), much like GDPR, requires protecting personal information via reasonable security measures like DLP. Nightfall is a control to detect and prevent the unauthorized transmission or storage of personal information, such as names, addresses, and personal identification numbers.

These specific CCPA sections and controls supported by Nightfall are:

* Section 1798.81.5 of CCPA requires businesses to implement and maintain reasonable security procedures and practices appropriate to the nature of the information to protect personal information from unauthorized access, destruction, use, modification, or disclosure. **Nightfall is a control to protect personal data from unauthorized access, alteration, destruction, or accidental loss.**
* Sections 1798.82 and 1798.83 of CCPA requires businesses to disclose to the California attorney general and California residents of any breach of the security of the system data, including a description of the categories and specific pieces of personal information that were or are reasonably believed to have been the subject of a breach. **Nightfall helps organizations to identify and mitigate risks to personal data by detecting and preventing data breaches.**
* Section 1798.125 of CCPA requires businesses to provide certain rights to California residents regarding their personal information, such as the right to know what personal information is being collected, the right to request deletion of personal information, and the right to opt-out of the sale of personal information. **Nightfall helps organizations to identify and control the collection and sharing of personal information.**

### LGPD

The Lei Geral de Proteção de Dados (LGPD) is the Brazilian data protection law that regulates the processing of personal data. Here are some specific controls and section numbers of the LGPD that are relevant to data leak prevention (DLP) for SaaS:

1. Article 46: This article establishes that the data controller is responsible for adopting security measures to protect personal data against unauthorized access, accidental or unlawful destruction, loss, alteration, communication, or any form of improper or unlawful processing. **Nightfall is a control to protect personal data from unauthorized access, alteration, destruction, or accidental loss.**
2. Article 47: This article states that the data controller must adopt administrative, technical, and security measures to protect personal data, considering the nature, scope, context, and purposes of the processing, as well as the risks and rights involved. **Nightfall is a technical security measure for protecting personal data.**
3. Article 48-A: This article, introduced by Provisional Measure No. 869/2018, requires the data controller to carry out a Data Protection Impact Assessment (DPIA) for processing operations that may present risks to individuals' rights and freedoms. **Nightfall can conduct historical scans that identify sensitive data like PII across SaaS applications.**
4. Article 48-B: Also introduced by Provisional Measure No. 869/2018, this article establishes that the data controller must adopt mechanisms for auditing and demonstrating compliance with data protection regulations. **Nightfall can conduct historical scans that provide reports on sensitive data exposure across SaaS applications.**
5. Article 48-C: This article, introduced by Provisional Measure No. 869/2018, requires the data controller to implement administrative and technical measures to protect personal data, including measures aimed at preventing unauthorized access, accidental or unlawful destruction, loss, alteration, communication, or any form of improper or unlawful processing. **Nightfall is a technical measure to protect sensitive data and can prevent accidental exposure or access through real-time monitoring and remediation.**

### PIPEDA

In the context of the Personal Information Protection and Electronic Documents Act (PIPEDA) in Canada, there are several specific controls that relate to data leak prevention. Here are some of the controls and how they map to data leak prevention:

1. Safeguards Principle (Section 4.7): This principle requires organizations to protect personal information against unauthorized access, disclosure, copying, use, or modification. Implementing technical and organizational measures to prevent data leaks, such as encryption, access controls, and network security, helps ensure compliance with this principle. **Nightfall is a technical measure that prevents data leaks and exposure through real-time monitoring and remediation.**
2. Security Safeguards (Section 4.7.1): This control specifies that organizations must protect personal information using safeguards appropriate to the sensitivity of the information. It includes physical, technological, and organizational security measures to prevent data leaks, such as secure storage, firewalls, intrusion detection systems, and employee training. **Nightfall can remediate sensitive data through different means whether that mean training an employee, redacting it, or deleting it, depending on the sensitivity of the information.**
3. Access Controls (Section 4.7.3): Organizations need to establish controls to limit access to personal information on a need-to-know basis. By implementing user authentication mechanisms, role-based access controls, and strong password policies, organizations can prevent unauthorized access and data leaks. **Nightfall monitors a SaaS environment in real-time so that sensitive data is not exposed in areas that it should not be in and thus contained on a need-to-know basis.**
4. Training and Awareness (Section 4.7.4): This control emphasizes the importance of educating employees about privacy policies, procedures, and best practices to prevent data leaks. Training programs should cover topics like handling sensitive information, recognizing phishing attacks, and secure data disposal. **Nightfall can notify end-users and employees that transmit sensitive data so that coaching is relevant and done in real-time to promote best practices.**
5. Incident Response (Section 4.7.5): Organizations must have procedures in place to respond to and mitigate privacy breaches. This control includes developing an incident response plan, promptly investigating and addressing breaches, and notifying affected individuals and the appropriate authorities. **Nightfall can scan a SaaS environment for sensitive data to determine if data was exposed.**
6. Monitoring and Auditing (Section 4.7.6): Regular monitoring and auditing of security controls help identify and address vulnerabilities that could lead to data leaks. This control involves conducting security assessments, penetration testing, log analysis, and reviewing access logs to detect and prevent unauthorized access or data breaches. **Nightfall can conduct a risk assessment to scan a SaaS environment and understand the nature of sensitive data exposure in the environment.**
7. Disposal and Destruction (Section 4.7.8): Proper disposal of personal information is crucial to prevent unauthorized access and data leaks. Organizations should have policies and procedures for securely destroying or anonymizing personal data when it is no longer required. **Nightfall remediation capabilities including actions like deleting and redacting sensitive data in real-time.**

## **Healthcare**

### **HIPAA**

Data protection is intimated but not explicitly required for HIPAA compliance. It is intimated in the following ways:

* The **Security Rule** requires organizations to use appropriate administrative, physical and technical safeguards to ensure the confidentiality, integrity, and security of sensitive information.
  * **Nightfall provides:**
    * **Administrative safeguards through highly contextualized end-user security awareness and training.**
    * **Technical safeguards by detecting and preventing clear-text personally identifiable information (PI) / protected health information (PHI) from leaving the environment, as well as automated corrective actions that lock down sharing or disallow download and print.** Additionally, Nightfall supports the Audit Control standard by maintaining logs of PHI record creation or dissemination on the systems it monitors.
* Nightfall does not cover the other two rules, namely the Privacy Rule and the Breach Notification Rule. These rules are outside of Nightfall's domain as they respectively govern a patient's access to their records and the processes for managing breaches.

### **HITRUST**

[HITRUST](https://hitrustalliance.net/) (Health Information Trust) is a proprietary cybersecurity framework primarily used by mature healthcare organizations to demonstrate leading security practices. Data protection is explicitly mentioned in multiple sections of the framework.

* **Data Protection & Privacy:**
  * Where possible and technologically feasible, the organization locates and removes/redacts specific PII or uses anonymization and de-identification techniques to allow the use of retained information while reducing its sensitivity and the risk from disclosure. **Nightfall's automated remediation actions, such as deletion and redaction, support this control and serve as an overall risk mitigation for data disclosure.**
  * The organization protects important records, such as contracts, personnel records, financial information, and client/customer information from loss, destruction, and falsification through the implementation of security controls. These controls include access controls, encryption, backups, electronic signatures, locked facilities or containers, among others. **Nightfall's real-time monitoring enables organizations to detect and respond to sensitive data loss.**
* **Transmission Protection:**
  * Before allowing the use of information systems for information exchange, the organization formally addresses multiple safeguards.
  * The organization never sends sensitive information without encryption using end-user messaging technologies (e.g. email, instant messaging, and chat). **Nightfall can monitor SaaS applications that are not approved to confirm that PHI is not transmitted.**
* **Education, Training & Awareness:**
  * Personnel are appropriately trained on leading principles and practices for all types of information exchange (oral, paper and electronic). **Nightfall can assist teams in building enforceable information security policies and provide end-user security awareness and training that is highly contextualized.**

## **Finance**

### **PCI**

PCI stands for Payment Card Industry, and it refers to a set of security standards and regulations designed to protect the sensitive cardholder data during payment card transactions. It ensures that businesses that handle payment card information maintain a secure environment to prevent data breaches and protect customer information. PCI is divided into 12 major sections, with several appendices, and 5 of 12 PCI controls are supported by Nightfall.

#### Version 3.2.1 and 4.0

Of the five sections, Appendix 3.2.6 is the section that most clearly states the requirement for DLP for all PCI-covered entities. As written:

* **Appendix 3.2.6 - Mechanisms are implemented for detecting and preventing cleartext PAN from leaving the cardholder environment.**
* Note that PCI’s example given explicitly states DLP: _“Mechanisms to detect and prevent unauthorized loss of cleartext PAN \[credit card number] may include the use of appropriate tools such as data loss prevention (DLP) solutions as well as manual processes and procedures.”_

The following four PCI DSS sections are also relevant to DLP controls:

* **Section 3: Protect Stored Account Data** specifies that cardholder data must be protected while at rest. Additionally, the requirements state that methods for minimizing risk include not storing cardholder data unless absolutely necessary, truncating cardholder data if the full PAN is not needed, and not sending unprotected PANs using end-user messaging technologies such as email and instant messaging. **Nightfall specifically covers these messaging technologies and can identify when such data is being stored somewhere where unauthorized access has occurred or may occur.**
* **Section 7. Restrict access to system components and cardholder data by business need to know:** This point is the same as the one above. **Nightfall can determine when need-to-know access might be violated.**
* **Section 10. Log and monitor all access to system components and cardholder data:** While Nightfall is not an access control, it can help determine which users have had access to specific pieces of data within certain integrations.
* **Section 12. Support information security with organizational policies and programs** - **Nightfall can help teams build enforceable information security policies. Additionally, it provides end-user security awareness and training that is highly contextualized.**

#### Note on Version 4.0

No changes regarding DLP or additional requirements from prior version 3.2.1.

### **GLBA / FCRA**

The Gramm-Leach-Bliley Act mandates that financial institutions safeguard consumers' personal financial information. Meanwhile, a smaller subset of financial institutions known as [consumer reporting agencies](https://www.consumerfinance.gov/consumer-tools/credit-reports-and-scores/consumer-reporting-companies/companies-list/) must maintain consumers' right to privacy when preparing consumer reports (also known as credit reports) on individuals, as required by the Fair Credit Reporting Act (FCRA). In both cases, the following data points must be protected if they identify an individual:

* Accounts numbers
* Credit card numbers
* Social Security numbers

These regulations are broad in nature and do not include specific enumerated requirements like PCI. However, they are explicit about not exposing customer records and impose fines for infractions (up to $100K per violation). **Nightfall can be used as a compliance control to detect and prevent clear-text personally identifiable, payment, or account information from transmission. It also provides automated corrective actions that can lock down sharing or disallow downloading and printing.**

### **SOX**

Sarbanes-Oxley (SOX) is a financial reporting regulation that applies to publicly traded companies. It was created in response to the Enron collapse, which was caused by creative accounting of financial results. SOX focuses on the principles of integrity, accuracy, and completeness, and requires publicly traded companies to maintain confidentiality of their financial results before reporting.

**Nightfall supports specific SOX requirements by detecting and preventing the movement of financial and accounting information in and out of the organization. It also provides automated corrective actions that restrict sharing and prevent downloading and printing.**

* Section 302 of SOX requires the CEO and CFO to certify the accuracy of the financial statements. This certification requires a control to mitigate unauthorized access, alteration, or sharing of financial data.

Section 404 of SOX requires internal controls that focus on access, confidentiality of financial records, and their testing by management. Data leak prevention (DLP) solutions can be a part of those internal controls to protect sensitive financial data.

## **Tech Services**

### **SOC 2**

#### Version 2017

This version is the only currently accepted version of SOC 2 by AICPA.

For the SOC 2 sections specified, Nightfall supports these requirements through its monitoring, notification, and automated remediation:

* **Confidentiality CC6.7**: _The entity restricts the transmission, movement, and removal of information to authorized internal and external users and processes, and protects it during transmission, movement, or removal to meet the entity’s objectives._ **This requirement specifically mentions data loss protection.** **Nightfall meets the standard to restrict the transmission and movement of data.**
* **Confidentiality CC6.1**: The entity implements logical access security software, infrastructure, and architectures over protected information assets to protect them from security events to meet the entity's objectives. Nightfall protects the following SOC 2 specifically identified sensitive data:
  * Confidential information assets such as personal information.
  * Encryption keys during use, storage, and transmission.
* **Confidentiality CC6.6**: _The entity implements logical access security measures to protect against threats from sources outside its system boundaries._ Nightfall provides coverage of the cloud and protects against personal devices (BYOD) that may be outside the system boundaries, making it a Boundary Protection System. Nightfall also addresses a specific SOC 2 concern by protecting identification and authentication credentials outside of the system boundaries.
* **Confidentiality CC2.2**: _The entity internally communicates information, including objectives and responsibilities for internal control, necessary to support the functioning of internal control._ Nightfall's automated responses to end users provide real-time security awareness training that is highly contextualized to the specific violation identified.

### **ISO 27001**

#### Version 2013

This version of ISO 27001 will no longer be valid after October 31, 2025. It includes limited data protection requirements that are detailed in a control supplement called ISO 27002. Two of these requirements can be supported with Nightfall:

* **11.2.6**: Security of Equipment & Assets Off-Premises
  * Context: In the context of this section, data is considered the asset, and the cloud / SaaS is considered off-premises.
  * Security controls must be applied to off-site assets, which means protecting data (the asset) on the cloud (the off-site / third-party data center). ISO requires the same technical controls as if it were on-site. Nightfall supports the following ISO control sections:
    * 8.1.3 / 8.2.3: Acceptable use of information and systems - this refers to the appropriate handling (i.e., sharing / disclosure) of sensitive data, which is a prime directive of Nightfall.
    * 12.4.1 - 12.4.3: Monitoring of sensitive data use.
    * 16.1.2 - 16.1.3: Information Security Event Reporting.
    * 18.2.2 - 18.2.3: Compliance with policies and standards for information security.
* **13.2.1**: Information Transfer Policies & Procedures
  * Communications must be secure regardless of the system used. Nightfall provides protection for communications over the public internet to various audiences, including Slack, Google Workspace, Jira, Confluence, and other systems. Thus, it is a control that supports the ISO requirement for **confidentiality** by taking into account the type, nature, amount, and sensitivity or classification of the information being transferred.

#### Version 2022

The latest version of ISO 27001 will be required after October 31, 2025. It includes the following new data protection requirements:

* **A.8.12**: Data leakage prevention. The requirement states that “data leakage prevention measures _shall_ be applied to systems, networks, and any other devices that process, store or transmit sensitive information.” **Therefore, it is recommended to use a tool like Nightfall when processing sensitive information, which is almost always the case.**
* In support of the above requirement, Nightfall also serves as a control for:
  * **A.8.10: Information deletion.** Nightfall's automated deletion enables this requirement, which states that "information stored on information systems, devices, or in any other storage media shall be deleted when no longer required."
  * **A.8.11: Data masking.** Nightfall's data masking in protecting data is identified as a specific requirement. The requirement states that "data masking shall be used in accordance with the organization's topic-specific policy on access control and other related topic-specific policies, and business requirements, taking applicable legislation into consideration."
  * **A.8.16: Monitoring activities.** Nightfall is a monitoring control that fits within this requirement, which states that "networks, systems, and applications shall be monitored for anomalous behavior, and appropriate action taken to evaluate potential information security incidents."
* **A.8.28: Secure coding.** Nightfall's protection of secrets and keys, none of which should ever be disclosed in development, supports this ISO requirement. The requirement states that "secure coding principles shall be applied to software development."

## **Education**

### **FERPA**

The Family Educational Rights and Privacy Act (FERPA) directs educational organizations to keep student school records private and confidential. Nightfall can be used to detect and prevent the unauthorized transmission or storage of student education records, such as student names, addresses, grades, transcripts, and other personal information.

While FERPA does not specify control numbers, it does require educational institutions to:

* Ensure that administrative and technical controls are in place to protect student education records from unauthorized access, disclosure, alteration, or destruction. **Nightfall is one such control as it protects personal data from unauthorized access, alteration, destruction, or accidental loss.**
* Limit access to student education records to school officials who have a legitimate educational interest in the records. **Nightfall can detect and prevent unauthorized access.**
* Keep a record of all individuals who have requested or obtained access to student education records, along with the legitimate educational interest that each person has in obtaining the records. **Nightfall can assist educational institutions in maintaining these records and detecting any unauthorized access to student education records.**

## **Government**

### **CMMC**

The Cybersecurity Maturity Model Certification (CMMC) is a framework developed by the Department of Defense (DoD) to protect unclassified information. CMMC's scope is the Defense Industrial Base (DIB), which includes all organizations that support the DoD. This is defined as any organization that enables research and development, design, production, delivery, and maintenance of military weapons systems, subsystems, and components or parts to meet U.S. military requirements. In short, any system or component used by the DoD is covered by CMMC.

**As of May 2023, version 2.0 is required**. CMMC measures maturity and ranks it by levels.

#### Version 2.0

If an organization is at Level 2, it must adhere to all requirements outlined in [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final). Note that in CMMC terminology, CUI stands for Controlled Unclassified Information. Nightfall provides support for these requirements.

* **3.1.3: Control CUI Flow: Control the flow of CUI in accordance with approved authorizations**. Nightfall supports this requirement by monitoring alerts and implementing automated remediations to maintain compliance with authorized CUI sharing on cloud systems.
* **3.8.5 Control access to media containing CUI and maintain accountability for media during transport outside of controlled areas.** Nightfall supports protecting digital CUI. It applies mechanisms to prevent unauthorized loss or access to CUI via monitoring alerts and automated remediations such as access removal.
* **3.13.16 – Data at Rest: Protect the confidentiality of Controlled Unclassified Information (CUI) at rest.** Nightfall’s automated remediation can help maintain confidentiality.

Note that Level 3 requirements have not yet been written. However, an additional requirement is currently under consideration.

* **3.1.3e - Employ secure information transfer solutions to control information flows between security domains on connected systems.** This requirement calls for the use of secure information transfer solutions to control information flows between security domains on connected systems. **Using Data Leak Prevention (DLP) to protect confidential data would satisfy this requirement. Therefore, Nightfall would help meet this requirement.**

### **FedRAMP / NIST 800-53**

NIST 800-53, which forms the basis for FedRAMP, is considered one of the less robust data protection security frameworks because it has fewer controls overall. Nightfall supports two major sections of the NIST CSF.

1. Information Flow:
   1. **AC-4: Information Flow Enforcement -** The information system enforces approved authorizations for controlling the flow of information within the system and between interconnected systems based on organization-defined information flow control policies. **Nightfall enables this control through its policies and automated remediations.**
2. Media Protection (note that the CSF definition of media includes laptops / mobile devices):
   1. **MP-6 -** Employs sanitization mechanisms with the strength and integrity commensurate with the security category or classification of the information. **Nightfall's automated remediations, such as redaction, support this control.**
   2. **MP-7 -** The organization restricts/prohibits the use of system media (in Nightfall's case, cloud systems/storage). **Nightfall's automated sharing changes (e.g., Google Drive) support this control.**
