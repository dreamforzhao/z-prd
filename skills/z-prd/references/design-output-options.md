# Design Output Options

Use this reference after the product document is approved and the user is deciding whether to continue into design or handoff output.

## Core Rule

Design output is optional. Always ask whether to continue. If the user says no, stop at the approved product artifact and summarize the current deliverable.

## Output Ladder

| Level | Use when | Deliverables |
| --- | --- | --- |
| Stop here | PRD/product plan is enough | approved scope, open questions, next suggested action |
| Low-fidelity | structure and flow are not yet confirmed | screen inventory, user flow, wireframe notes, state list |
| Design brief | a designer will continue in a tool | page-by-page requirements, content, sample data, components, tokens |
| Platform handoff | team uses Modao, Lanhu, Figma, MasterGo, Pixso, or similar | upload checklist, page annotations, interaction notes, design-token table |
| Runnable prototype | PM/engineering needs reviewable UI | standalone HTML or app-native prototype, responsive and visual checks |
| Engineering handoff | design is approved or prototype is enough | component map, data/actions, acceptance checks, visual verification |

## Platform Notes

| Platform | Good for | Z-PRD should produce |
| --- | --- | --- |
| 墨刀 / Modao | product prototypes, interaction demos, product-team collaboration | page list, flow map, interaction rules, copy, state table, optional upload checklist |
| 蓝湖 / Lanhu | design handoff, annotation, assets, developer collaboration | design annotation checklist, assets list, spacing/color/type notes, acceptance checks |
| Figma | UI design, prototyping, design systems, design-to-code workflows | frame plan, component map, token table, prototype links, dev handoff notes |
| MasterGo | domestic design collaboration, prototype/design/dev mode | page specs, component/state map, responsive rules, dev-mode handoff notes |
| HTML/React prototype | quick review, vibe coding, implementation preview | runnable screens, sample data, states, responsive checks |

## Upload Guidance / 上传前确认

Do not assume platform access. If the user wants upload:

1. Ask the user to log in to the chosen platform.
2. Confirm the target workspace/project.
3. Confirm exactly what will be uploaded.
4. Use browser automation only after the user clearly approves the upload.

中文规则：如果用户要求上传到墨刀、蓝湖、Figma、MasterGo、Pixso 或其他第三方平台，必须先确认“目标空间/项目、上传内容、是否立即提交”。用户没有明确授权时，只输出可导入材料，不自动上传。

If upload is not available, provide an import-ready package:

- page inventory
- screen-by-screen spec
- interaction table
- state matrix
- copy deck
- sample data
- asset checklist
- design-token table
- developer acceptance checks

## Design Handoff Template

```markdown
## 是否继续设计输出

当前产品文档已可作为阶段成果。是否继续输出设计落地材料？

可选：
1. 不继续，停在当前 PRD/产品设计。
2. 输出低保真线框和页面流程。
3. 输出给墨刀/蓝湖/Figma/MasterGo 的设计交付包。
4. 输出可运行 HTML/React 原型。
5. 输出研发交接包。
```

## Avoid

- Automatically producing high-fidelity design when the user only approved PRD.
- Uploading files to third-party tools without explicit approval.
- Treating design output as mandatory.
- Sending a full PRD to every specialist when only page specs are needed.
