---
description: Learn about Nightfall secret detection.
---

# Secrets Detection

### **Nightfall's** **API Key Detector**&#x20;

Nightfall's API key supports generic API key detection plus vendor-specific and use-case-specific keys. Nightfall attempts to validate the key status of vendor-specific keys and JWT tokens.&#x20;

| Vendor Support                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Token Support                                                                                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>• AWS </p><p>• Azure </p><p>• Coinbase</p><p>• Confluence</p><p>• Confluent</p><p>• Databricks</p><p>• Datadog</p><p>• ElasticSearch</p><p>• Facebook<br>• GCP - Google Cloud</p><p>• Google API - All other Google Services</p><p>• GitHub</p><p>• GitLab </p><p>• Hugging Face</p><p>• JIRA</p><p>• Nightfall </p><p>• Notion</p><p>• Okta</p><p>• OpenAI</p><p>• PagerDuty</p><p>• Paypal </p><p>• Plaid</p><p>• Postmark</p><p>• Postman</p><p>• Rapid API</p><p>• Salesforce</p><p>• Sendgrid</p><p>• Slack</p><p>• Snyk</p><p>• Square</p><p>• Stripe</p><p>• Twitter</p><p>• Twilio</p><p>• Zapier</p> | <p><br><br></p><p>• Authentication Token</p><p>• CSRF Token</p><p>• OAuth Token</p><p>• Generic API Key</p><p>• Generic Token</p><p>• JWT</p><p>• Private Key</p><p>• Refresh Token</p><p>• Session Token</p><p></p><p></p><p></p> |

### [**Nightfall's Cryptographic Key Detector**](https://docs.nightfall.ai/docs/detector-glossary#secrets)&#x20;

Nightfall identifies and validates popular crypto keys for locking or unlocking cryptographic functions, including authentication, authorization, and encryption.

| <p>• DSA Private Key </p><p>• RSA Private Key </p> | <p>• EC Private Key </p><p>• OpenSSH Private Key </p><p>• Private Key </p> | <p>• Encrypted Private Key </p><p>• PGP Private Key Block</p> |
| -------------------------------------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------------- |

You can send us a request for new Secrets detectors directly in [Nightfall](https://app.nightfall.ai/detection-engine/detectors).&#x20;
