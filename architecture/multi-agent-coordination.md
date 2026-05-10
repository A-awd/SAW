# Multi-Agent Coordination Layer

## Purpose

Make Claude, Codex, Gemini, and MCP-backed tools cooperate through durable artifacts.

## Roles

| Agent | Primary Job | Output |
|---|---|---|
| Claude | Architecture and planning | ADRs, specs, issue plans |
| Codex | Execution and verification | branches, PRs, tests, migrations |
| Gemini | Research and critique | review notes, comparisons, risk critique |
| MCP | Tool bridge | structured system actions |

## Handoff Contract

Every handoff should include:

- repo,
- goal,
- constraints,
- files/systems involved,
- verification expected,
- known risks,
- durable links.

## Conflict Resolution

1. Source code and migrations win.
2. Accepted ADRs win.
3. Latest merged PR wins.
4. Repo health notes guide priorities.
5. Chat memory loses if it conflicts with durable GitHub state.
