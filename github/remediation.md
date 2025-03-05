---
description: >-
  Sensitive data like credentials pose a large risk when found in code repos.
  Read our guide to remediating these DLP risks in GitHub.
---

# Remediation on Nightfall for Github

GitHub is a code versioning tool, which means that it preserves a full history of searchable code changes. Sensitive data can proliferate in these code changes and is not always easily discoverable.

Credentials & secrets that are hard-coded in GitHub repositories pose risk if repos are leaked or accessed via social engineering attacks, as they can provide access to infrastructure, databases, and third-party APIs. Likewise, sensitive data like customer PII can end up in code repos. This can raise significant security, compliance, and brand risk.

Nightfall automatically detects sensitive data in GitHub repos in real-time across any code push event to GitHub. With Nightfall’s context-rich detection results, you’ll be able to prioritize remediation efforts based on the type and location of sensitive data. However, git is a complicated protocol and because git is designed to be a full historical trail of commits, remediation is non-trivial. As a result, we’ve outlined best practices to remediate violations below.

### 1. Rotate Your Credentials

In their [data security guide](https://docs.github.com/en/github/authenticating-to-github/removing-sensitive-data-from-a-repository), GitHub states the following: “Once you have pushed a commit to GitHub, you should consider any data it contains to be compromised. If you committed a password, change it! If you committed a key, generate a new one.” Secrets such as API keys and cryptographic keys should be considered high priority risks.

If you have pushed credentials & secrets to a repo, your first step should be to immediately revoke the compromised credentials and generate new ones.

After doing so, please remember to update your application code or config/environment variables accordingly to ensure things continue to work with your new credentials. If your credentials are used by other developers or deployed in your infrastructure, make sure they all get a new version of it.

Most common services that issue API keys such as Twilio, Stripe, Twitter, etc. typically all have mechanisms to revoke a key and generate a new one. This can be found in the admin panel of their API consoles. If you have questions about how to rotate a specific service’s token, please reach out to Nightfall Support at [support@nightfall.ai](mailto:support@nightfall.ai) and we would be happy to look into it.

### 2. Remove Historical References

### 2.A. Review repo access permissions

Simply because a GitHub repo is private doesn’t mean that sensitive data can or should be stored there safely. On GitHub, developers associate their personal GitHub accounts with their corporate organizations. This means that it can be easy for the lines to blur. You can [view who can access](https://docs.github.com/en/organizations/managing-access-to-your-organizations-repositories/viewing-people-with-access-to-your-repository) your repos on GitHub.

Similarly, an organization’s repos can have collaborators from outside the organization. [Check on this access](https://docs.github.com/en/organizations/managing-access-to-your-organizations-repositories/removing-an-outside-collaborator-from-an-organization-repository) by navigating to your GitHub organization and clicking the People tab. From here, click Outside Collaborators to review who can access your organization’s repos. Consider removing or modifying access.

You can [customize access](https://docs.github.com/en/organizations/managing-access-to-your-organizations-repositories/repository-permission-levels-for-an-organization) to each repository in your organization with granular permission levels, giving people access to the features and tasks they need. Likewise, you can [set base permissions](https://docs.github.com/en/organizations/managing-access-to-your-organizations-repositories/setting-base-permissions-for-an-organization) for the repositories that your organization owns.

GitHub repos should only be made public when strictly necessary. If a repo is intended to be open-sourced, it should undergo a thorough code review to confirm no sensitive information or trade secrets are revealed. If a repo is public that shouldn’t be, you can make it private.

Navigate to your GitHub repository and click Settings. In the “Danger Zone” section, click “Make private” if the repository is public. If the repo is no longer necessary, click “Delete this repository” to permanently remove it.

### 2.B. Rewrite git history

If the sensitive data can be successfully rotated per above, it may not be necessary to rewrite git history. However, it may be helpful to go the extra mile to keep your repositories clean and avoid future fire drills if the credentials are discovered at a later point and it is unclear if the secret has been correctly rotated or not.

If the sensitive data cannot be rotated, for example PII, then rewriting git history is necessary.

There are two recommended methods for rewriting git history, the BFG Repo-Cleaner tool, which we describe below, and git filter-branch to which we’ve linked steps.

#### 2.B.i. Using the BFG

#### ![](https://lh3.googleusercontent.com/DqF9NSxxZaOSSD6HOPWpn4GrW00m3Oya31GeVNvKEBIXv2z86n5niUIrs3Y31eP3Tme73FMZzoYgpOC5ZJsF_Yq3YYG7Qg70SCqmbTnnzJ5LX-P11bU-vE-t7RdWkFoGVlQxsAPX) <a href="#block-1b3b69fd-dde4-4cbb-b048-373b04fd4c33" id="block-1b3b69fd-dde4-4cbb-b048-373b04fd4c33"></a>

The [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/) is a tool that’s built and maintained by the open source community. It provides a faster, simpler alternative to git filter-branch for removing unwanted data. For example, to remove your file with sensitive data and leave your latest commit untouched, run:

`$ bfg --delete-files YOUR-FILE-WITH-SENSITIVE-DATA`

To replace all text listed in passwords.txt wherever it can be found in your repository’s history, run:

`$ bfg --replace-text passwords.txt`

After the sensitive data is removed, you must force push your changes to GitHub.

`$ git push --force`

See the [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/)‘s documentation for full usage and download instructions.

An alternative method to BFG Repo-Cleaner would be via `git filter-branch`. This process is more involved and the steps are outlined by GitHub [here](https://docs.github.com/en/github/authenticating-to-github/removing-sensitive-data-from-a-repository#using-filter-branch) or in git documentation [here](https://docs.github.com/en/github/authenticating-to-github/removing-sensitive-data-from-a-repository#using-filter-branch).

There are additional ways to modify git history, which you can review in git documentation for advanced & specific use cases: [Git Tools – Rewriting History](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History).

### 3. Review Access

Various third-party services provide access logs describing when secrets & credentials are used or called. Where possible, review these access logs to determine if any exposed secrets or credentials had been leveraged. If so, you may need to undergo a deeper investigation around a potential security incident.

For example, Zendesk provides the following Activity portal for their API. If you identified that a Zendesk API key was leaked, you could subsequently check this portal to determine if there is any anomalous usage activity beyond what you would normally expect.

![](https://lh4.googleusercontent.com/SiIhLdls9AN137bCo5tCiql-dEyCQoC_SmctaEVo9L5RjTHt_rWCxjDrucScoKnCnH3wJFRBY9IopE2P9pMUgORVCuFjUQT0TMONBGFoelUzhcaPvwKvOgmVuY16JE-OWx1aI34f)

### 4. Establish Your Workflow & Process

If you are collaborating on code with others in your organization or have limited permissions, it may not be feasible to remediate the compromised secrets on your own or complete the steps outlined above. In this case, it’s beneficial to set up a process by which you can log compromised secrets and notify the responsible party who will be able to act on them.

### Triage Workflow

Project management and bug tracking tools are good options for managing the process of remediating compromised credentials & secrets. For example, Jira and Linear. Consider creating tickets that include the following information so the Assignee has sufficient context:

* Repository – _e.g. nightfalldlp/sample_
* Commit reference – _e.g. d3cce9f_
* File path – _e.g. sample.py_
* Branch – _e.g. main_
* Link to the specific line of code on GitHub – _e.g._ [_https://github.com/nightfalldlp/sample/blob/master/sample.py#L2_](https://github.com/nightfalldlp/sample/blob/master/sample.py#L2*)

### Notifying Collaborators

When deciding who to notify and what to say in your message, it’s important to first consider the following:

* **Is the repo still actively used or maintained?** If not, it may be best to advise the repo owner to archive or delete the repo.
* **Who committed the compromised credentials?** The author who committed to secrets into the codebase may have the ability to follow the remediation steps above.
* **Who owns or manages the repo?** Perhaps the original author of the commit that introduced the compromised credentials is no longer in your organization or has changed roles/responsibilities. In this case, it may be best to reach out to the repo’s owners or admins. You can see who has access to the repo by navigating to _Settings_ then _Manage Access_.

### 5. Preventing Credential Exposure Going Forward

Now that you know what types of sensitive data tend to get exposed on GitHub and have begun to remediate these violations, you can be proactive about mitigating these risks moving forward via the following recommendations.

### Use a visual program like [GitHub Desktop](https://desktop.github.com/) or [gitk](https://git-scm.com/docs/gitk) to commit changes.

Visual programs generally make it easier to see exactly which files will be added, deleted, and modified with each commit.

### Use git commands in accordance with best practices.

* Avoid the catch-all commands `git add .` and `git commit -a` on the command line — use `git add filename` and `git rm filename` to individually stage files, instead.
* Use `git add --interactive` to individually review and stage changes within each file.
* Use `git diff --cached` to review the changes that you have staged for commit. This is the exact diff that `git commit` will produce as long as you don’t use the `-a` flag.

### Ignore files with sensitive information.

Name sensitive files in `.gitignore` and `.npmignore` to avoid checking them into git. Learn more about [gitignore](https://git-scm.com/docs/gitignore).

### Store credentials safely.

* Use local environment or configuration variables so the application retrieves these variables dynamically instead of hard-coding them into files
* Centralize credentials with a secrets management service “secrets as a service” solution
  * Examples include [AWS Secrets Manager](https://aws.amazon.com/secrets-manager/), [Hashicorp Vault](https://www.vaultproject.io/) or [Square Keywhiz](https://square.github.io/keywhiz/).
  * This prevents secret sprawl and allows for audit logging, however there is a cost to implementing and maintaining these solutions.

### Leverage safety controls provided by the third-party services issuing API keys.

* Services like Stripe, Twilio, SendGrid, Zendesk, etc. whose API keys you may be using may have different security controls you can take advantage of:

### Use temporary credentials with expiration dates if the service allows it.

* Enable IP allowlisting if the service allows it.
* Restrict permissions associated with the key.
  * Certain services like SendGrid and Stripe have granular permissions management across API keys, similar to IAM roles on AWS:

![](https://lh5.googleusercontent.com/7RJjr7ePHn2pN7Ps3zbd8OXxhRKbqPpW-zT7wgct_Yo_aXfYZ5VlUeqxcN09eAht4NgoFEnh3_JCIQohVeMBbCteDJuA40zwmvIVYMQPCZSf6U_pp1CRTymB4G8V2QXVOKWfxgez)

### Treat secrets equally. Protect dev/test secrets in addition to production secrets.

It’s easy to confuse dev/test secrets with production ones, and they can end up in the wrong environment – treat all credentials as if they are sensitive and high-risk to avoid this.

### Avoid sharing credentials & secrets.

Tools like Slack and email make communication seamless, but that also means they can open up pathways for easily transmitting credentials & secrets and sprawling this information to more data silos.

Nightfall has native integrations to identify sensitive data in other applications such as Slack and Confluence, where sensitive data is commonly proliferated by developers.

### Code security training.

As software development proliferates across every industry and use case, code security is more important than ever. Consider a formal training program or service to ensure developers understand the risk and best practices.

### Scan GitHub repositories at different parts of the SDLC.

[Nightfall](https://www.nightfall.ai/) provides multiple ways to scan for sensitive data in code repositories – in near real-time upon code commit to GitHub, historically across all code changes, upon Pull Request, and via a git-hook on the developer endpoint device. Reach out to our Support team to learn more about these options and determine what fits best in your SDLC.

## Need Help?

Reach out to Nightfall Support at [support@nightfall.ai](mailto:support@nightfall.ai).&#x20;
