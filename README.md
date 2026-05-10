# A-awd AI Operating System Seed

This repository is the public, non-secret seed for the A-awd GitHub-first AI operating system.

GitHub is the permanent memory and coordination layer. Supabase is the production data layer. Claude acts as architect. Codex acts as execution engineer. Gemini can be used for research, critique, and second-pass review. MCP tools connect the models to durable systems.

Important: do not store secrets, private customer data, production credentials, financial records, or irreversible operational instructions in this public repository. Use this repo for standards, templates, workflows, and coordination patterns only.

## Core Repositories

| Repository | Current Role | Notes |
|---|---|---|
| `A-awd/yoright` | OTA platform | Production-style monorepo; needs highest operational discipline. |
| `A-awd/rocantis-store` | Shopify theme/store | Has strong Shopify `AGENTS.md`; now participates in shared AI standards. |
| `A-awd/oleel-shopify` | Shopify theme | Dawn-derived Shopify repo; standardization target. |
| `A-awd/jwleria` | Lovable React/Supabase app | Needs product identity and repo health docs. |
| `A-awd/jwleria-s-gembox` | Lovable React/Supabase app | Possible duplicate/variant of `jwleria`; review before merging. |
| `A-awd/calapres` | Lovable React/Supabase app | More complete test setup than some Lovable siblings. |
| `A-awd/SAW` | AI OS seed / coordination | Empty before this initialization. |

## Operating Principle

AI models coordinate through repositories, issues, pull requests, and durable docs, not chat memory.

Every project should have:

- `AGENTS.md` for model-specific execution rules.
- `docs/ai/OPERATING_MODEL.md` for repo-specific AI workflow.
- `docs/ai/REPO_HEALTH.md` for health, risks, and maturity.
- `.github/ISSUE_TEMPLATE/ai-task.yml` for deterministic AI tasks.
- `.github/pull_request_template.md` for test, migration, and safety checklists.
- `docs/architecture/` for product and technical decisions.
- `supabase/migrations/` when Supabase is used.
- `logs/` and `backups/` standards documented, but generated artifacts ignored.

## Role Contract

- Claude: architecture, product framing, long-term planning, technical decisions.
- Codex: implementation, tests, migrations, repo maintenance, operational hardening.
- Gemini: external research, second-opinion review, broad comparison, critique.
- Supabase: durable production data, migrations, RLS, operational data APIs.
- n8n: deterministic automation orchestration and scheduled workflows.
- Shopify: commerce runtime for Shopify businesses.

## Safety Contract

- Never commit secrets.
- Never overwrite raw production data.
- Never rewrite Git history unless explicitly approved.
- Prefer additive migrations.
- Preserve business context in GitHub docs and issues.
- Use deterministic scripts and workflows before AI loops.
- Treat public repos as public, even if business context feels harmless.
