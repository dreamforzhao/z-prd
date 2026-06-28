# Multi-Agent Routing

Use this reference when the product task is large enough that separate expert views would reduce risk.

## Default

Stay single-agent for simple or medium tasks. One `$z-prd` pass is enough when the user wants a compact PRD, product plan, or prototype brief.

## Recommend Multi-Agent When

| Signal | Suggested view | Output |
| --- | --- | --- |
| User problem is unclear, market/user assumptions are weak | Requirements analyst | problem framing, P0/P1/P2, user stories, acceptance criteria |
| Product has many roles, objects, states, or permissions | Product designer | information architecture, page map, workflows, state model |
| UI needs reviewable interaction detail | UI prototyper | screen inventory, sample data, interaction plan, responsive checks |
| Work is about implementation readiness | Engineering handoff | data objects, actions/APIs, dependencies, test and visual checks |
| User asks for critique or risk review | Skeptic reviewer | assumptions, overscope, failure modes, missing evidence |

## Routing Contract

Each view should return:

- verdict: ready / needs revision / blocked
- key findings
- decisions made
- open questions
- next recommended action

Do not ask every view to repeat the full PRD. Each view should inspect only its own layer and produce a compact delta.

## Token-Saving Pattern

1. Main agent writes or reads the compact product brief.
2. Send each specialist only the relevant section.
3. Merge outputs into one decision memo.
4. Ask the user to confirm before UI prototype or coding.

## Avoid

- Spawning specialists for a small feature.
- Asking multiple agents to produce the same document.
- Sending the entire codebase or full PRD to every agent.
- Letting specialists make conflicting product decisions without a final main-agent synthesis.
