---
description: >-
  Use sample data sets provided by Nightfall to test Nightfall's detection
  capabilities.
---

# Nightfall Sample Data Sets

The following datasets can be used to test Nightfall's advanced AI-based detection capabilities. The data has been fully de-identified and can be used to test any data loss prevention (DLP) platform.

### Protected Health Information (PHI)

Nightfall's genAI-based model outperforms traditional entity-based detectors by detecting PHI entities in patient healthcare-related documents.

```
The patient, Anthony Smith (DOB 05/10/1993), presents with a sustained elevated heart rate. 
The patient has a past medical history of atrial fibrillation. 
Attending Physician: Harwood, Andrew MD 
```

{% file src="../.gitbook/assets/nightfall_ai_phi_demo_dataset.zip" %}

### API Keys

Nightfall AI's fine-tuned API key detection LLM detects secrets with high precision and dramatically reduces false positives.

```
import stripe stripe.api_key = "sk_live_4eC39HqLyjWDarjtT1zdp7dcTYooMQauvdEDq54NiTphI7jx"
stripe.Charge.create( amount=2000, currency="usd", source="tok_amex", # obtained with Stripe.js description="Charge for jenny.rosen@example.com" )
```

{% file src="../.gitbook/assets/nightfall_ai_api_key_demo_dataset (2).zip" %}

_Testing note:_ If a key status is marked as ‘Active’, please rotate the key immediately. Not all vendors provide an "Inactive" response code. In these cases or if the vendor service is offline, the finding status will be marked ‘Unverified’.

### Passwords

Nightfall AI detects passwords shared in conversational text and code.&#x20;

```
Alex, Here are the credentials to get onto the new training platform. 
loginid=fitnessFreak99 passphrase=Activ3Life22!
```

{% file src="../.gitbook/assets/nightfall_ai_passwords_demo_dataset (2).zip" %}

### Cryptographic Keys

This sample dataset demonstrates Nightfall's ability to detect cryptographic keys.&#x20;

{% file src="../.gitbook/assets/nightfall_ai_crypto_key_demo_dataset.zip" %}

### PII (Personally Identifiable Information)

This sample dataset demonstrates Nightfall's ability to detect PII with high precision and low noise in text, spreadsheets, and screen grabs. Samples include names, U.S. social security numbers, and driver's licenses.

```
Hi Support - My name is Julie Walsh. I tried to purchase a life insurance policy online yesterday however the site said, "an unexpected error occurred." 
I tried to pay with a credit card. My DOB is 02-10-97 and SSN is 523-23-6145. Could you take a look on your end?
```

{% file src="../.gitbook/assets/nightfall_ai_pii_demo_dataset.zip" %}

### Financial - Credit Card Numbers and Banking Info

This sample dataset demonstrates Nightfall's ability to detect sensitive banking and payment information with high precision and low noise in text, spreadsheets, and screen grabs. Samples include positive and negative examples of credit card numbers, routing numbers, IBAN codes, and SWIFT codes.

```
Hi Support - This is Julie Walsh. I tried to purchase an electric bike using my credit card 6771-8979-6102-7961. 
The app is telling me the card was declined. Could you take a look on your end?
```

{% file src="../.gitbook/assets/nightfall_ai_pci_banking_demo_dataset (4).zip" %}

### Image ID Documents (ID Cards, Passports, Credit Cards, etc as images)

Nightfall’s computer vision (CV) transformer model outperforms legacy Optical Character Recognition (OCR) text scanning to identify driver’s licenses, passports, credit cards, and US social security cards even though images may be degraded (rotated, glossy, low contrast, blurry, skewed, or cropped).\


<figure><img src="../.gitbook/assets/657810889367bc55feabd1f8_image-detector.gif" alt="" width="375"><figcaption></figcaption></figure>

{% file src="../.gitbook/assets/nightfall_ai_image_ID_document_demo_dataset.zip" %}
Image ID Sample Dataset
{% endfile %}
