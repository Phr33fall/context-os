# ContextOS Architecture

ContextOS separates tools by responsibility.

The architecture is built around one rule: current state, durable knowledge, source code, and sensitive evidence are different things. They should not live in the same place or be treated as interchangeable.

## Role Map

| Component | Responsibility | Not Responsible For |
|---|---|---|
| Orchestrator | Direction, live state, decisions, handoff quality | Direct code edits without verification |
| Implementation agent | File changes, tests, local execution, commits | Reconstructing business state from memory |
| Auditor | Independent review, drift detection, repo checks | Acting as the canonical project manager |
| Operational hub | Current status, project hubs, specs, dev logs | Long-form personal knowledge |
| Knowledge vault | Durable notes, session handovers, reusable patterns | Declaring live project state |
| Git | Code history, diffs, branches, commits | Explaining why the business decision changed |
| Encrypted vault | Restricted material | Automatic ingestion, indexing, graphing, or memory |

## Read Sequence

When current project state matters, tools should read in this order:

1. Current operational source of truth
2. Relevant project hub or spec
3. Development log or commit history
4. Knowledge vault notes as supporting context

The reverse order creates drift.

Old notes are useful. They are not automatically current.

## Handoff Flow

```text
Orchestrator defines the task
        |
        v
Implementation agent changes files and verifies locally
        |
        v
Auditor checks claims against source, repo, and rules
        |
        v
Session handover records what changed, why, and what comes next
        |
        v
Next session resumes from evidence
```

## Why Handoffs Matter

AI sessions fail quietly when work is completed but not carried forward.

A good handover records:

- what happened
- what changed
- what was decided
- what was verified
- what remains risky
- the single next action

That is enough for another tool or another day to restart without guessing.

## Design Principle

Do not aim for one giant memory.

Aim for clear custody.

Each layer should know what it owns and what it must fetch from somewhere else.

