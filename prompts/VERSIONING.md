# Prompt Versioning

Prompts are versioned operational assets.

## Version Format

Use semantic versions:

```text
name@major.minor.patch
```

Examples:

- `codex-execution-engineer@1.0.0`
- `claude-architect@1.0.0`
- `gemini-reviewer@1.0.0`

## Change Rules

- Patch: wording clarification, no behavior change.
- Minor: adds capability or new output section.
- Major: changes role, safety behavior, or expected output.

## Required Prompt Header

Every prompt must state:

- name,
- version,
- owner,
- purpose,
- allowed inputs,
- required outputs,
- safety constraints.
