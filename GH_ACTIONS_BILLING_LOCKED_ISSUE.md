Title: CI blocked: account locked due to billing issue

Description:

Our GitHub Actions workflow run for "Build Jekyll site" failed to start with the annotation: "The job was not started because your account is locked due to a billing issue." A screenshot of the failure is available.

What happened:

- The workflow run shows a red X and the message that the account is locked due to billing.
- No job logs are available because the job was not started.

Steps to reproduce:

1. Push changes to `main` or open a PR.
2. Observe the workflow run fail to start with the billing/locked annotation.

What I tried:

- Verified the workflow file is valid and works locally.
- Confirmed repository is configured to use `docs/` for Pages (project site).

Suggested actions:

1. Check account/organization billing settings and resolve outstanding invoices or update payment method.
2. Re-run the workflow after billing is resolved.
3. If you cannot resolve billing quickly, as a temporary workaround you can set GitHub Pages source to the `docs/` folder (already used here), which publishes site without Actions, or host the static site elsewhere.

Please advise if you want me to open an official support ticket or prepare a PR that disables the workflow temporarily until billing is resolved.
