---
description: Zoom Password Findings
---

# Why does the Password Detector Report False Positive Zoom Password Findings?

Previously, Nightfall Password detector used to report Zoom passwords as sensitive data findings. However, the Nightfall Password detector now recognizes passwords found in personal Zoom links. Customers sharing these links in docs and messages will no longer be alerted for these non-sensitive findings.

The detector can now identify patterns such as:

* Zoom meeting invites containing embedded PWD parameters and separate alpha-numeric passcodes.
* Zoom recording URLs with associated passcodes.

Examples:

1.  Multi-line meeting invite with embedded Zoom password and passcode

    [https://company](https://company).[**zoom.us**](http://zoom.us)/j?**pwd=VBhZM3h5SEhQTXEzQzEyYUREWkJHQT09**

    Meeting ID: 991 1959 8432

    **Passcode: 475749**
2.  Recording URL with passcode

    [https://company](https://company).[**zoom.us/rec**](http://zoom.us/rec)/share/zuBQvxkbLce3PRl6eYSBXN0Uj47mE9grL\_6G4J1qeFcaWCqB94hdgC5hb4B3R3SF.VxapNL9oXfGuiokO

    **Passcode: BH%$!.06**
