# AI Operating Model

## Repository Role

Describe what this repo owns, what it does not own, and which business or product it supports.

## AI Roles

- Claude: architecture and planning.
- Codex: implementation and verification.
- Gemini: research and review.

## Durable Memory

Durable memory lives in:

- GitHub issues,
- pull requests,
- `docs/architecture/`,
- `docs/ai/REPO_HEALTH.md`,
- migrations and runbooks.

## Data and Secrets

- Secrets live outside GitHub.
- `.env.example` documents names only.
- Production data belongs in Supabase or approved production systems.

## Standard Workflow

1. Convert request into a GitHub issue or PR task.
2. Claude clarifies architecture when needed.
3. Codex implements on a branch.
4. Tests and migration checks run.
5. PR records the durable decision and verification.
6. Merge only after risk is understood.
