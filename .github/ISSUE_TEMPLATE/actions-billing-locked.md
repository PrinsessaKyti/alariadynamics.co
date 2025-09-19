name: CI blocked by billing / account locked
about: Use this when GitHub Actions jobs are not starting because the account or organization is locked for billing reasons.
title: "CI blocked: account locked due to billing issue"
labels: ci, billing
assignees: ""

---

## Summary

CI jobs are not starting. The workflow run shows: "The job was not started because your account is locked due to a billing issue." See attached workflow run screenshot.

## Reproduction

1. Push code to `main` or open a PR.
2. Observe the GitHub Actions run show a red X and the annotation: "The job was not started because your account is locked due to a billing issue."

## Expected

Workflows should start and complete the build steps.

## Actual

GitHub blocks the job from starting and shows a billing/locked message.

## Notes / logs

- Repository: PrinsessaKyti/alariadynamics.co
- Workflow: Build Jekyll site (.github/workflows/jekyll.yml)
- Branch: main
- Screenshot: (attach the screenshot showing the "account is locked" annotation)

## Troubleshooting & suggested fixes

1. Check repository Billing settings: https://github.com/organizations/<your-org>/settings/billing or https://github.com/settings/billing for a user account.
2. Resolve any outstanding invoices or billing issues (update payment method, pay outstanding balance).
3. If this is an organization, ensure an owner has valid billing information and the Actions minutes policy is configured.
4. After resolving billing, re-run the failed workflow run or push a new commit.
5. If you can't resolve billing immediately, consider temporarily disabling the workflow or using the `docs/` publishing source for Pages (which does not require Actions), or use an alternative GitHub account/organization.
6. If you believe this is an error, contact GitHub Support with billing/account details: https://support.github.com/contact

## Additional context
Add any other context about billing emails or account messages you received.
