# ContextOS Bootstrap

Use this for the first setup session.

The goal is not to build a perfect system. The goal is to stop every new AI session starting from guesswork.

## Day-One Prompt

Copy this into your AI assistant:

```text
I want to set up ContextOS for my AI workflow.

Your job is to help me bootstrap it from zero.

Do not assume my tools are connected.
Do not assume memory is current.
Do not assume one tool can see what another tool knows.
Ask only the questions needed to build a simple working map.

Find out:

1. What tool owns live project state.
2. Where durable notes and handovers should live.
3. Where code or file changes are tracked.
4. Which AI assistants, agents, or coding tools I use.
5. Which connectors, MCPs, plugins, or local tools are available.
6. What files, folders, systems, or data types must never be ingested automatically.
7. What should happen at the end of a meaningful session.
8. What date/time convention should be used.
9. What a clean restart should look like.

Output:

- source-of-truth map
- handover location
- restricted-material boundaries
- session-end checklist
- first test workflow
- next setup action

Rules:

- Keep the setup small.
- Prefer one clear next step over a large plan.
- Flag conflicts instead of guessing.
- Do not ingest private material unless I explicitly approve that exact task.
- Do not write to live project systems until I approve the proposed update.
```

## Minimum Source-Of-Truth Map

Your first map can be simple:

```md
| Layer | Owner | What It Is Trusted For | What It Must Not Do |
|---|---|---|---|
| Live project state | <tool> | Current status, decisions, active risks | Long-term memory |
| Durable knowledge | <tool/folder> | Notes, handovers, reusable lessons | Live status unless updated |
| Code/file history | <tool> | Diffs, commits, rollback | Business context |
| Memory retrieval | <tool> | Helpful context | Canonical truth |
| Restricted storage | <location> | Sensitive material | Automatic ingestion |
```

## First Test Workflow

Run one small session:

1. Read the source-of-truth map.
2. Do one low-risk task.
3. Verify the result.
4. Create a handover.
5. Start a fresh chat.
6. Ask the fresh assistant to continue from the handover.

If the fresh assistant can continue without guessing, ContextOS is working.

## What To Avoid On Day One

- complex automation
- broad file ingestion
- trying to connect every tool at once
- moving private material into memory stores
- building a perfect taxonomy before doing useful work
- letting the assistant write to live systems without approval

Start small. Prove the handover loop. Improve from there.

## Common Failure Modes

- Empty search is not proof of absence.
- Memory retrieval is not current state.
- A clean commit does not explain business context.
- A handover without a next action is incomplete.
- If two sources disagree, stop and flag the conflict.
- If the assistant races ahead without confirmation, stop it. Momentum is not permission.
- Do not let the assistant write to live systems until the proposed update is approved.

## Simple Maintenance Rhythm

Weekly:

- review the latest handovers
- check whether the source-of-truth map still matches reality
- archive or close stale sessions
- capture one lesson learned

Monthly:

- review tool roles
- remove unused automation
- check restricted-material boundaries
- test whether a fresh assistant can restart from the latest handover
