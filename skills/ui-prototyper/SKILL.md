---
name: ui-prototyper
description: UI prototyping expert for turning approved PRDs, product specs, feature ideas, wireframes, screenshots, or page lists into usable interactive prototypes in HTML, React, Vue, or the current project framework. Use when the user explicitly asks for UI 原型, 交互原型, 高保真原型, 页面设计, 前端 demo, 可运行原型, wireframe, mockup, dashboard, app screen, or wants a prototype-only artifact.
---

# UI Prototyper

## Overview

Create reviewable, usable UI prototypes that make product decisions visible. Prefer building the actual usable first screen instead of a marketing page.

## Workflow

1. Read the PRD or product spec. If absent, infer a concise screen list from the user's idea and state assumptions.
2. Choose the smallest implementation that produces a real interactive prototype: existing app framework first, then standalone HTML when no project exists.
3. Design the primary workflow first, including navigation, list/detail/edit surfaces, empty states, errors, and realistic sample data.
4. Match the product domain. Operational tools should be dense, calm, and efficient; consumer products can be more expressive.
5. Implement responsive layouts with stable dimensions for fixed-format UI such as toolbars, boards, tables, cards, and counters.
6. Verify the prototype visually in a browser when possible, including desktop and mobile widths.
7. Report the file path or local URL and the main interaction coverage.

## Prototype Rules

- Build the application experience, not a landing page, unless the user explicitly asks for marketing.
- Use existing design systems, components, dependencies, and icons when present.
- Include feature-complete controls that users would expect: tabs, filters, menus, toggles, inputs, sliders, dialogs, tables, and tooltips as appropriate.
- Avoid visible instructional text about how the UI works unless the product naturally needs it.
- Do not nest cards inside cards. Use cards for repeated items, modals, or framed tools only.
- Avoid one-note color palettes and oversized hero typography inside compact app surfaces.
- Ensure text does not overlap or overflow on mobile and desktop.

## Output Shape

Use `references/prototype-brief-template.md` when planning or summarizing a prototype.

For implementation tasks, deliver:

- Implemented files
- Running instructions or local URL
- Covered screens and interactions
- Known gaps or assumptions

