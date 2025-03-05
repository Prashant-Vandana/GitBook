---
description: >-
  Use this to understand the language nuances when using Nightfall for text
  recognition and classification.
---

# Which languages does Nightfall support?

For pre-built Nightfall Detectors, Nightfall supports different languages for certain detection algorithms. For sensitive data types that are numeric/alphanumeric - such as card numbers, passport numbers, drivers licenses, etc. - Nightfall trains these detectors with context that corresponds to the language in that geographical area. For example, for our pre-built Brazilian CPF detector (a National Brazilian Tax Number) our detector is trained on context in English and in Portuguese (examples include phrases like “pessoas singulares registro número”).

For custom detectors (such as regular expressions), Nightfall supports any characters in the UTF-8 character set. For all intents and purposes this should support characters in most languages. The full list is available here [http://www.unicode.org/charts/index.html.](http://www.unicode.org/charts/index.html)



For example, let's take the following Hindi text: मेरा नाम पैट्रिक है।

This translates in English to: "My name is Patrick."



If we build a custom detector as a regular expression such as: "पैट्रिक" (which says match on the name “Patrick”), we will be able to detect this in Hindi text.



However, Nightfall has not yet built detection algorithms that attempt to understand this text (beyond what’s stated above), meaning it cannot match through any lexical context or interpretation of the text. In other words, Nightfall has no semantic or lexical understanding on what the underlying characters actually mean unless they are in English or trained per the above.

Because Nightfall has no interpretation of these Hindi characters, the pre-built Person Name detector will not flag on "पैट्रिक" (Patrick).
