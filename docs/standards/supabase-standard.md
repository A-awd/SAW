# Supabase Standard

Supabase is the production data layer. GitHub is the coordination and migration memory layer.

## Required Practices

- Store schema changes in `supabase/migrations/`.
- Use additive migrations unless a destructive migration is explicitly approved.
- Enable RLS on exposed tables.
- Keep security-definer functions out of exposed schemas unless reviewed.
- Never commit `service_role` keys, database passwords, JWT secrets, webhook secrets, or SQL dumps with private data.
- Use `.env.example` for names only, not values.

## Migration Review Checklist

Every migration PR must answer:

- What tables, views, functions, triggers, policies, or indexes change?
- Is the migration additive?
- What is the rollback path?
- Does it affect existing production data?
- Does it expose data through REST, Realtime, Storage, or Edge Functions?
- Are RLS policies present and aligned with access model?

## Data Access Pattern

- Browser: anon/publishable key only, RLS-enforced.
- Server: service role only in trusted server environments.
- n8n: scoped credentials with least privilege where possible.
- AI agents: no direct production writes unless explicitly routed through reviewed scripts or MCP tools.
