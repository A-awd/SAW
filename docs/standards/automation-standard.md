# Automation Standard

n8n and GitHub Actions should run deterministic workflows. AI should design and maintain workflows, but production automation should not depend on vague prompt loops.

## Workflow Classes

- `ci`: lint, test, typecheck, build.
- `deploy`: controlled release or publish flow.
- `sync`: pull data from external systems into approved stores.
- `audit`: scheduled health checks, drift checks, backup checks.
- `notify`: Slack/email/issue creation for actionable events.

## Required Properties

- Idempotent where possible.
- Logs structured status and failure reasons.
- Retries transient external failures.
- Avoids duplicate writes through stable keys.
- Fails closed when secrets or required inputs are missing.
- Creates GitHub issues for human follow-up when automation cannot decide safely.

## n8n Discipline

- One workflow per durable business process.
- Use GitHub issues/PRs for workflow change requests.
- Keep workflow credentials in n8n credential store, never in exported JSON.
- Export sanitized workflow definitions into GitHub when possible.
