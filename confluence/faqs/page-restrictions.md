---
description: >-
  Note the current issue that we have with scanning for Confluence pages with
  Page Restrictions set
---

# Page Restrictions

We have been noticing some errors in our service when scanning certain pages/spaces in your Confluence instance. This issue is related to certain custom page permission restrictions for those specific Confluence pages. With base page restrictions set, our app is unable to view edits on these page.

When ‘Page restrictions’ are set on a page/space, our app is no longer able to see it, so when scanning is attempted on items from that page, our API requests fail. For a short term solution, you can add our app 'Nightfall DLP for Confluence' to have 'View' access on the page.\
\
**Note**: We are currently working on a longer term solution for this issue, and are in discussion with Atlassian directly



If you are not seeing these pages being scanned and want to check if this restriction is in place, this can be checked as seen below:

**Checking Workspace Permissions:**

<figure><img src="https://lh5.googleusercontent.com/P3waeU4vyGCYmd7_zXQj_WY7E5w_29m0WbPvzztNPIc02p7wk69j6kc5NVXuQCgowj1FPJFShYiu0kVpCcQldYjlpRNIbUxR6WJDFoX6RTB-bRrsM6N3wMfmQQODUyh-6b0rTq3MIlKLfnhz4B44ZLbkBYge3zYD9cO66Om-qn9nTBqZ_e611av6wQ" alt=""><figcaption><p>Checking and Updating Workspace Permissions</p></figcaption></figure>

**Checking Page Restrictions:**

<figure><img src="https://lh5.googleusercontent.com/bMoOmZDocQ0JRuM7JSj_anspnOnmwQCG3Ol0e1_WPlzqJxfk5SFxbAZpOy3GHPbJZG0ypLPuyVvdPs89njzjMZygwUiK1UQ4gmzeIKnNqJ3rrywKdfVbCRqz8Qv5Qj2C5BlAFVAORSoSDhji-yItj6j6k_roCUJH1oD6X1QtUePDZrdnowMBn43kxw" alt=""><figcaption><p>Checking and Updating Confluence Page Restrictions</p></figcaption></figure>

If you have any questions about these restrictions, or are unsure how to workaround, please file a support ticket with us, or you can reach out to support@nightfall.ai.
