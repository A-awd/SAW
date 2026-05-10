# ADR-0002: Multi-Agent Role Contract

## Status

Accepted

## Context

Different AI models are useful for different work. Without clear roles, outputs become duplicated, conflicting, or temporary.

## Decision

Use this role contract:

- Claude: architect, strategist, decision framer.
- Codex: execution engineer, implementation, tests, migrations, repository operations.
- Gemini: researcher, critic, comparison engine, second-pass reviewer.
- MCP: connector/tool bridge.
- Supabase: production data system.
- n8n: deterministic automation runtime.

## Consequences

- Planning and implementation are separated.
- Durable work lands in GitHub.
- Every agent must preserve existing repo context and avoid destructive changes.
