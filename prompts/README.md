# Prompt Management

Prompts are versioned operational assets.

## Folders

```text
prompts/
  claude/        # architecture and planning prompts
  codex/         # execution, repo maintenance, migration prompts
  gemini/        # research, critique, comparison prompts
  shared/        # model-neutral task contracts
```

## Rules

- Prompts must state inputs, expected outputs, and safety constraints.
- Prompts must not contain secrets.
- Repo-specific prompts should link back to the repo and issue/PR context.
- When a prompt changes behavior materially, update the changelog or related issue.
