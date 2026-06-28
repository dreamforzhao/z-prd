# Token Budget Guide

Use this when a task is long, repeated, or likely to involve multiple agents.

## Main Principle

Keep `$z-prd` as the only always-loaded product workflow. Put long examples, templates, and comparisons in references so they are loaded only when useful.

## Response Modes

| Mode | Use when | Shape |
| --- | --- | --- |
| Compact review | vague idea, early discussion | 1-2 pages, assumptions labeled |
| Full PRD | formal doc requested | use `product-flow-template.md` |
| Prototype brief | PRD already approved | screen list, states, interactions, sample data |
| Handoff brief | ready for development | objects, actions, permissions, checks |

## Practical Rules

- Ask only blocking questions. State non-blocking assumptions and continue.
- Prefer tables for requirements, stories, risks, and page maps.
- Do not paste full templates unless requested.
- Summarize prior decisions before continuing a long thread.
- Use separate files for stable artifacts when work spans sessions.
- For multi-agent work, send each agent only the slice it needs.

## Context Reset Handoff

When a thread becomes long, produce a short handoff:

```text
Product:
Current decision:
Approved scope:
Open questions:
Next action:
Files/artifacts:
```

This is cheaper than replaying the whole conversation.
