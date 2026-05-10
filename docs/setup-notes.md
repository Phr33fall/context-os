# Setup Notes

This is a reference setup, not a one-click installer.

Adapt it to your tools and risk model.

## Minimum Viable ContextOS

You need four things:

1. A source of truth for live project state
2. A markdown vault for durable handovers
3. Git for code history
4. A rule that restricted files are not automatically ingested

Everything else can improve over time.

## Suggested Folders

```text
vault/
  index.md
  log.md
  sessions/
    YYYY/
      MM/
  indexes/
  templates/
```

## Session Handover Rule

At the end of meaningful work, write one durable handover.

Do not write a transcript.

Write the operational truth:

- summary
- decisions
- files changed
- commits
- verification
- open risks
- next action

## Skill Pattern

Create a small instruction file for the assistant responsible for knowledge hygiene.

Its job:

- maintain handovers
- maintain indexes
- audit stale links
- preserve safety boundaries
- keep tool roles separate

## Practical Advice

Start small.

Do not automate every write on day one.

First prove that the handover format is useful. Then automate the boring parts.

