# Source Of Truth Map

Use this to define what each system owns.

| Source | Owns | Does Not Own |
|---|---|---|
| Operational hub | Current project state, specs, decisions, logs | Long-term knowledge library |
| Knowledge vault | Durable notes, session handovers, reusable patterns | Live project status |
| Git | Code changes, diffs, commit history | Business context unless written in commit messages |
| Issue tracker | Tasks and execution queue | Strategic source of truth |
| Encrypted storage | Restricted material | Reusable knowledge |
| Memory tool | Retrieval and context assistance | Canonical truth |

## Conflict Rule

When sources conflict, flag the conflict.

Do not silently decide which source is true unless the ownership map says so.

