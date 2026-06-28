---
name: product-workflow
description: End-to-end product workflow orchestrator for automatically turning a one-sentence product idea, vague requirement, business request, app concept, feature ask, or "帮我做一个..." prompt into requirements analysis, product design, reviewable product documentation, UI prototype planning, and optionally a runnable prototype. Use when the user gives a short product idea and wants Codex to "自动跑完", "从需求到原型", "做产品方案", "做一个系统/应用/小程序/网站", "一句话需求", or does not explicitly name requirements analyst, product designer, or UI prototyper.
---

# Product Workflow

## Overview

Run the product team flow from a short idea to concrete artifacts with review checkpoints. Prefer Chinese outputs unless the user asks for another language.

## Default Behavior

When the user gives a one-sentence idea, do not ask them to choose an expert. Start the product flow, but pause at review gates:

1. Requirements analysis: clarify problem, users, scope, user stories, acceptance criteria, risks, and open questions.
2. Product documentation review: produce a compact PRD and product design brief for the user to review. Stop here and ask for confirmation before moving to UI prototype planning.
3. Product design: after approval, refine product structure, information architecture, page map, workflows, states, MVP, and roadmap.
4. UI prototype planning: define screens, interactions, sample data, visual direction, and responsive checks.
5. Prototype implementation: only build runnable UI after the user confirms the product document or explicitly says to skip review and proceed directly.

If a blocking business detail is missing, ask one concise question. If the missing detail is non-blocking, make a reasonable assumption and continue.

## Review Gates

Use human review by default. Do not continue from product documentation to UI prototype or implementation until the user says something like "确认", "继续", "没问题", "按这个做", "进入原型", or gives edits to incorporate.

Skip the review gate only when the user explicitly says "无需审核", "直接跑完", "全自动", "不要停", or equivalent.

At the review gate, show a concise product document with:

- Product understanding
- Target users and scenarios
- P0/P1/P2 requirements
- MVP boundary
- Page map
- Core workflow
- Main assumptions and open questions
- What will be designed or built next after approval

## Output Modes

Use compact-review mode by default for vague early ideas:

- One-paragraph product understanding
- PRD summary
- Product design summary
- UI prototype plan
- Assumptions and open questions
- Review request: ask the user to confirm or revise before continuing

Use full mode when the user asks for detailed documents, PRD, complete product plan, or stakeholder-ready output. Use `references/end-to-end-template.md`.

Use implementation mode when building a prototype. Follow existing project conventions first; otherwise create a standalone prototype that can be opened or served locally.

## Coordination Rules

- If the user explicitly invokes another skill or plugin, honor the explicit invocation first.
- If the request is a vague product idea, one-sentence requirement, or from-zero product build request, prefer this workflow as the orchestrator.
- If multiple skills seem relevant, use this workflow to decide stage order, then apply the specialist skill standards inside each stage.

- Apply the same standards as `$requirements-analyst`, `$product-designer`, and `$ui-prototyper` without requiring the user to name them.
- Keep decisions flowing forward, but pause at review gates.
- Label assumptions clearly.
- Preserve traceability from requirement to page to interaction.
- For internal tools, dashboards, CRM, ERP, admin systems, and SaaS, design dense, calm, work-focused interfaces.
- For consumer products, content products, games, or brand experiences, allow more expressive interaction and visual style.

## Handoff

End review-gate responses with a direct confirmation request:

- "你先看这版产品文档，确认后我再进入 UI 原型。"
- "如果要改，直接告诉我要调整的点；如果没问题，回复继续。"

When the user asks to continue, continue from the current artifact instead of restarting.

