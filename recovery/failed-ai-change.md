# Recovery: Failed AI Change

## Symptoms

- AI change breaks build, tests, UX, data, or deployment.
- PR scope is too broad.
- Agent touched unrelated files.

## Steps

1. Stop further changes on the same branch.
2. Identify exact files changed.
3. Run deterministic tests/checks.
4. Revert only the bad change, not unrelated user work.
5. Preserve evidence in PR comments.
6. Split future work into smaller tasks.

## Rule

Do not hide failed AI work. Capture the failure mode so future agents improve.
