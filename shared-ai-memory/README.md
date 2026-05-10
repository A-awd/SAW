# Shared AI Memory

Shared AI memory is durable, explicit, and GitHub-native.

It is not chat history. It is the curated memory that any future AI model or human engineer can trust.

## Memory Types

- `index/`: maps where memory lives.
- `entities/`: durable records for businesses, systems, products, people roles, vendors, and tools.
- `projects/`: project summaries, ownership, current state, and canonical repos.
- `sessions/`: important session summaries that must survive model context loss.

## Rules

- Store facts, decisions, and links. Do not store secrets.
- Prefer stable identifiers: repo names, issue numbers, PR numbers, migration names, project IDs.
- Every memory entry must be useful to a future engineer who has no chat context.
- If memory becomes outdated, append a correction or update the record with a dated note.

## Memory Hierarchy

1. Source code, migrations, and workflows.
2. Issues and pull requests.
3. Architecture decisions and runbooks.
4. Repo health records.
5. Shared AI memory indexes.
6. Chat summaries.

The higher item wins when there is conflict.
