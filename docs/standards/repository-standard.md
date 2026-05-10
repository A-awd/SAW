# Shared Repository Standard

This standard applies across A-awd repositories.

## Required Files

- `README.md`: human onboarding and product summary.
- `AGENTS.md`: AI execution rules and repo-specific constraints.
- `docs/ai/OPERATING_MODEL.md`: how Claude, Codex, Gemini, MCP, Supabase, n8n, and external tools coordinate for this repo.
- `docs/ai/REPO_HEALTH.md`: maturity, risks, missing standards, and next hardening steps.
- `.github/pull_request_template.md`: deterministic change checklist.
- `.github/ISSUE_TEMPLATE/ai-task.yml`: structured task intake.
- `.env.example`: safe placeholder-only environment reference for apps.

## Folder Standard

Use these folders when relevant:

```text
app/ or src/                 # application source
components/                  # reusable UI components
lib/                         # shared app logic and integrations
supabase/migrations/         # additive SQL migrations only
docs/architecture/           # architecture decisions and system maps
docs/ai/                     # AI coordination and repo health
docs/runbooks/               # operational playbooks
scripts/                     # deterministic local/CI scripts
.github/workflows/           # GitHub Actions
logs/                        # local runtime logs, gitignored
backups/                     # local backups, gitignored
```

Shopify theme repos keep Shopify's native folders (`assets`, `blocks`, `config`, `layout`, `locales`, `sections`, `snippets`, `templates`) and add only the standards folders that do not conflict with Shopify.

## Migration Discipline

- Prefer additive migrations.
- Never edit applied production migrations.
- Every migration must include purpose, rollback notes, and data-risk notes in the PR.
- Supabase projects must use RLS deliberately.
- Do not expose `service_role` keys to frontend code.

## Environment Strategy

- `.env` files are local only.
- `.env.example` contains placeholders only.
- Public frontend variables must be explicitly safe for browser exposure.
- Service keys, Shopify private tokens, payment secrets, webhook signing secrets, and customer data never enter GitHub.

## AI Coordination

GitHub is the durable memory layer. Agents should leave the durable state in one of:

- issue comments for task decisions,
- PR descriptions for implementation details,
- `docs/architecture/` for durable system decisions,
- `docs/ai/REPO_HEALTH.md` for repo maturity and next actions.

Chat memory is useful but not authoritative.
