---
description: Exclude certain tokens from detection to suit your business logic
---

# How do I use Exclusion Rules?

Exclusion Rules, also known as an allowlist, help you reduce false positives in your sensitive findings by ignoring content from detection, or “allowing” it to pass through without being flagged.

For example, let’s say you are using the Email Address detector and you don’t want any corporate domains of “@example.com” to be detected by Nightfall. You can add “\*@example.com” as a regex Exclusion Rule.

You can add in a list of known safe tokens as a dictionary or craft a regular expression. A dictionary is a list of literal values, for example, a list of dummy credit card numbers or API keys. Regular expressions are known patterns to match against, for example if you want to allow all emails of a given domain as in the example above. Regular expressions follow RE2 syntax listed [here](https://github.com/google/re2/wiki/Syntax). You can test your regular expression [here](https://regex101.com/).

Exclusion Rules can be added on to any detector (either pre-made by Nightfall or off your own custom regular expression or “regex”) to omit certain “tokens” or items from resulting in detection events.

Here’s how you can build your own Exclusion Rule and attach it to a detector:

1. Select the type of Exclusion Rule you would like to use. It can be either a dictionary of words (which may be entered manually or uploaded from a list) or a regex pattern.
2. Select the match type from the dropdown menu on the right, either Partial or Full match.
3. Append your Exclusion Rule to your custom detector by clicking the "Save" button in the lower right.

[![](<../../.gitbook/assets/Exlcusion UI Refresh - Dictionary (1).png>)](https://nightfall.intercom-attachments-7.com/i/o/277336861/2c87f8da998d5373f4fbed45/urgtYtKlK3UzkH0nn93nBaHiNdttE27Z4U2c6kIivsKA9FSNdF25h0d_D5eoOxpawPOx6KLwry9gP-lYvuQwsvCNaTjW0yyMsRKkz0j30byz2Tj4xh7DPJDa_CwyHrc88Itrp42R)[![](<../../.gitbook/assets/Exclusion UI Refresh- RegEx.png>)](https://nightfall.intercom-attachments-7.com/i/o/277336868/34341250f1b6eb9df8732cc8/3yq7nmBDZfjqw2LDBceILavdGY2dg_-4yfR76TJzS-iwr3pDnINYK5wNfpMxvpSCirGEU-450UFzUxMGhaWYGLusL4wfYqEOalF7fUVT_jor5VA988gQkHyIdJk9gb7vH-HrtAED)
