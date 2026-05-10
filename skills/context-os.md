# ContextOS Skill

ContextOS is a reusable AI assistant skill for handovers, source-of-truth discipline, memory hygiene, and cross-tool continuity.

Use this skill when work spans more than one chat, tool, repository, knowledge base, or session.

## Purpose

Keep AI-assisted work coherent across tools.

ContextOS helps an assistant:

- read the right source of truth before acting
- separate live project state from durable knowledge
- create useful session handovers
- treat memory retrieval as context, not truth
- use Git as change history, not business context
- protect restricted material by default
- pass work cleanly between planning, building, auditing, and improvement

## Core Rule

Every tool has a job.

No tool is allowed to pretend it is the source of truth for everything.

## Source Boundaries

Use this ownership model unless the user gives a different one:

| Source | Owns | Does Not Own |
|---|---|---|
| Operational hub | Current project state, decisions, specs, logs | Long-term knowledge library |
| Knowledge vault | Durable notes, session handovers, reusable patterns | Live project status |
| Git | Code diffs, commits, branches, rollback points | Business state unless captured in commit messages |
| Memory system | Retrieved context from previous work | Canonical truth |
| Graph system | Relationship discovery and navigation | Current project state |
| Encrypted or restricted storage | Restricted material | Automatic ingestion or reusable notes |

## Read Sequence

When current state matters:

1. Read the live operational source of truth.
2. Read the relevant project hub, spec, issue, or task.
3. Read logs, commits, and knowledge notes as supporting evidence.
4. If sources conflict, flag the conflict. Do not silently infer.
5. Never treat empty search as proof of absence.

## Handover Trigger

Create or propose a handover when:

- meaningful work was completed
- a decision was made
- code changed
- a repo was audited
- a defect was found
- a project paused or resumed
- another AI tool needs to continue the work
- the session contains knowledge worth preserving

Do not create a handover for trivial chat with no durable value.

## Handover Format

Use this structure:

```md
# Session - <Project / Topic>

DTG: <date and local time>
Source tool: <tool>
Project: <project>
Session type: <code / audit / strategy / operations / mixed>
Status: <in progress / complete / blocked / awaiting approval>

## Summary

<5-10 lines. What happened and why it matters.>

## Decisions Made

- <decision>

## Work Completed

- <work completed>

## Files Changed

- `<path>` - <summary>

## Commits

- `<hash>` - <message / purpose / verification status>

## Verification

- <compile/test/audit status>

## Open Risks

- <risk>

## Next Action

<single next best action>

## Links

- <related notes, project pages, repo paths, commits>
```

## Restricted Material Rule

Default deny.

Do not read, write, search, index, summarise, ingest, graph, embed, sync, or reference restricted material unless the user gives explicit task-specific approval.

Approval should define:

- the source location or scope
- the permitted operation
- the permitted output destination
- whether anything may be copied into notes, repos, memory, graph outputs, or handovers

Restricted material includes:

- personal data
- access secrets
- private records
- internal documents
- unpublished evidence
- private screenshots
- financial or personal records
- anything governed by policy, contract, law, or explicit user restriction

## Public-Safe Writing Rule

When writing public docs, examples, diagrams, READMEs, or skills:

- use neutral terms such as restricted material
- avoid implying that protected material is part of the AI workflow
- keep examples generic
- remove private paths, IDs, names, access details, and restricted evidence
- include non-affiliation disclaimers where third-party tools are referenced

## Audit Behaviour

When auditing:

1. Verify claims against files, commits, logs, or explicit tool output.
2. Separate facts from assumptions.
3. Report conflicts before fixing them.
4. Prefer small, reversible changes.
5. Record unresolved risks.
6. Preserve user work. Do not revert unrelated changes.

## Operating Mode

Be useful before being elaborate.

Use the smallest structure that prevents drift.

A good ContextOS response should make the next session easier to start.
