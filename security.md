# Security Statement

## Intended Users

This repository contains code and files for a class project. The intended users are:

- **Me:** I write and maintain all code in this repo.
- **The instructor and TAs:** They review and grade the work.
- **Classmates and collaborators:** They may view or contribute code when the assignment calls for it.

The repo is not meant for production use or for the general public. It does not contain real user data.

## Risk Assessment

**Overall risk: low.**

If the code or data fell into the wrong hands, the realistic concerns are:

| Concern | Risk | Notes |
|---|---|---|
| Exposure of secrets (API keys, tokens, passwords) | Low, but the most serious possibility | No secrets should be committed. If one were exposed, it would need to be revoked and rotated immediately. |
| Exposure of personal data | Very low | The repo contains no personal or sensitive data, only sample or public data. |
| Academic integrity (copying or plagiarism) | Moderate | Others could copy the code for the same assignment. This is an academic concern, not a technical one. |
| Malicious modification of code | Low | Only the owner (and any invited collaborators) can push to the repo. Changes by anyone else would require a pull request. |
| Vulnerable dependencies | Low | Third-party packages could contain known vulnerabilities, but the project is not deployed or exposed to users. |

Because the repo has no sensitive data, no production deployment, and no real users, the potential harm from a breach is small.

## Steps Taken to Secure the Repo

- **No secrets in the repo:** credentials and keys are kept out of version control. A `.gitignore` excludes files such as `.env` and local configuration.
- **Pull request rules:** the `main` branch is protected so changes go through a pull request rather than direct pushes.
- **CODEOWNERS file:** a `CODEOWNERS` file assigns me as the required reviewer for all files.
- **Limited access:** only people who need access (the instructor and TAs, plus any assigned teammates) have been added as collaborators.
- **Secure accounts:** Two-factor authentication is enabled on my GitHub account.
- **Dependency alerts:** GitHub Dependabot alerts are enabled to flag vulnerable dependencies.
- **Secret scanning:** GitHub secret scanning is enabled to catch accidentally committed credentials.

## If Something Goes Wrong

If a secret is accidentally committed, I will revoke it right away, remove it from the repo history, and replace it with a new one. Removing the file in a later commit is not enough, because the old commit still contains it.
