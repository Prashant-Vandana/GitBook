---
description: Learn about typical cases of Nightfall
---

# Why does Nightfall sometimes miss to report SSN, credit card number, and so on?

Social security numbers (SSNs) are a common data type we scan for. You may notice 9-digit numbers in your data that resemble SSNs. If you lower your detection rule confidence to possible, these numbers will appear in your dashboard.

However, over 90% of 9-digit numbers are typically false positives that don't require action. Numbers formatted like SSNs are often used as internal IDs - for tickets, service calls, events, dispatches, transactions, etc. They can also be valid driver's licenses or bank account numbers.

With more context, our models can better determine if a 9-digit number is likely an SSN. For example, when a number appears in a sentence or tabular data with a descriptive header, our confidence in predicting it as an SSN increases to likely or very likely.

Providing contextual cues helps our models accurately identify SSNs and avoid false positives. We continue improving our algorithms to balance detection with precision.

The same thinking applies to other alpha-numeric info types like credit card numbers and passport numbers.

Please reach out if you have any further questions!
