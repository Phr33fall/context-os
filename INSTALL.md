# Install And Adapt ContextOS

ContextOS is a skill pattern, not a packaged app.

Use it as an instruction layer for the AI tools you already use.

## Option 1 - Generic LLM / ChatGPT / Claude Chat

Copy [`skills/context-os.md`](skills/context-os.md) into your project instructions or custom instructions.

Then tell the assistant:

```text
Use ContextOS for this project. Before acting, respect the source-of-truth map, create handovers after meaningful work, and flag source conflicts instead of guessing.
```

## Option 2 - Claude Code

Create a skill folder:

```bash
mkdir -p ~/.claude/skills/context-os
cp skills/context-os.md ~/.claude/skills/context-os/SKILL.md
```

Then start a session and say:

```text
Use the context-os skill for this session.
```

For stronger automation, add a `/handover` command that writes a session handover to your knowledge vault.

## Option 3 - Codex

Create a skill folder:

```bash
mkdir -p ~/.codex/skills/context-os
cp skills/context-os.md ~/.codex/skills/context-os/SKILL.md
```

Then use it when auditing repos, writing handoffs, or checking whether implementation matches project state.

## Option 4 - Obsidian Vault

Create a simple structure:

```text
vault/
  index.md
  log.md
  sessions/
    YYYY/
      MM/
  templates/
```

Use [`templates/session-handover.md`](templates/session-handover.md) as your handover template.

## Option 5 - Notion + Obsidian

Use Notion for live project state.

Use Obsidian for durable knowledge and handovers.

Do not let either system pretend to be the other.

A simple rule works:

```text
Notion says what is current.
Obsidian remembers what was learned.
Git proves what changed.
```

## Minimum Viable Setup

If you only do three things, do these:

1. Define your source-of-truth map.
2. Create one handover template.
3. End meaningful sessions with a handover.

That alone prevents a large amount of drift.
