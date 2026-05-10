# ADR-0001: GitHub as AI Operating System

## Status

Accepted

## Context

The ecosystem uses Claude, Codex, Gemini, MCP, Supabase, n8n, Shopify, multiple businesses, multiple devices, and multiple AI workflows.

Chat memory is fragmented and temporary. Repositories and GitHub issues/PRs are durable, reviewable, and linkable.

## Decision

GitHub is the permanent business operating system, long-term AI memory, and coordination layer.

AI models coordinate through:

- repositories,
- issues,
- pull requests,
- architecture docs,
- runbooks,
- migrations,
- versioned prompts.

## Consequences

- Every project needs AI coordination files.
- Important decisions become ADRs or GitHub issues.
- Supabase remains the production data layer.
- n8n remains the deterministic automation layer.
- Chat summaries are useful but not authoritative.
