# Safety Model

ContextOS treats safety as architecture, not an afterthought.

The system assumes that some material should never be automatically indexed, embedded, summarised, graphed, or handed to an AI tool.

## Default Rule

Restricted material is outside AI access by default.

Access requires explicit, task-specific approval from the user.

ContextOS is built around exclusion first: restricted material stays outside AI workflows unless a user explicitly approves a specific task.

## Restricted Material Examples

- personal data
- access secrets
- private records
- internal documents
- unpublished evidence
- private screenshots
- financial or personal documents
- anything governed by policy, contract, law, or explicit user restriction

## Boundary Pattern

```text
Reusable knowledge      -> knowledge vault
Live project state      -> operational hub
Code and diffs          -> Git
Sensitive source files  -> encrypted storage
```

The knowledge vault may contain a sanitised pointer to sensitive material, but not the sensitive material itself.

## Good Pointer

```md
# Insurance Policy Review

Status: pending review
Sensitive source documents: encrypted vault
AI access: denied unless explicitly approved for a specific task
Next action: review policy terms manually
```

## Bad Pointer

```md
# Restricted Finding

Identifier: private-system-name
Record: copied restricted source material
Owner: named individual
```

## Agent Rule

If a tool cannot see a source, it should say so.

It should not infer.

It should not claim absence from an empty search.

It should not treat a memory result as current truth.

