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

## Platform Output Contracts

### 墨刀 / Modao 原型输出

Use when the user wants an interactive product prototype or asks for 墨刀交付.

Produce:

- 项目结构：页面分组、导航层级、主流程入口。
- 页面清单：页面名、用途、核心组件、默认状态。
- 交互说明：点击、跳转、弹窗、表单校验、异常返回。
- 状态矩阵：空、加载、错误、无权限、部分数据、成功。
- 文案清单：标题、按钮、表单提示、错误提示、空状态文案。
- 样例数据：每个页面 3-8 条真实感数据。
- 上传清单：建议在墨刀中创建的页面、连线和备注。

If upload is requested, ask the user to log in to Modao and confirm the target project before uploading.

### 蓝湖 / Lanhu 设计交付输出

Use when the user wants design-to-development handoff, annotation, assets, or 蓝湖交付.

Before output, ask briefly whether the team has its own standard style:

```text
你们是否已有设计规范、组件库、颜色/字体/间距标准或蓝湖标注口径？有的话请提供；没有我按通用 SaaS/后台产品规范输出。
```

Produce:

- 页面交付清单：页面、状态、端型、优先级。
- 标注口径：间距、字号、颜色、圆角、阴影、栅格、断点。
- 组件清单：按钮、表单、表格、卡片、导航、弹窗、提示。
- 资产清单：图标、图片、空状态插图、Logo、导出倍率。
- 研发验收：视觉还原点、交互验收、响应式检查。
- 蓝湖备注：每页给设计/研发看的关键说明。

### Figma / MasterGo / Pixso 设计文件输出

Use when the user wants a design-file-ready brief.

Produce:

- Frame plan: desktop/mobile/tablet frames and naming rules.
- Component map: local components and variants.
- Design tokens: color, type, spacing, radius, elevation.
- Prototype links: interaction paths and transition notes.
- Dev-mode notes: states, constraints, responsive behavior, acceptance checks.

Ask for existing design system, brand style, or component library before finalizing visual specs.

### 可运行 HTML/React 原型输出

Use when the user wants a reviewable screen or vibe-coding-ready output.

Produce:

- screen inventory
- sample data model
- implemented interactions
- state coverage
- responsive targets
- visual verification checklist

Only build code after the user confirms they want a runnable prototype.

### 研发交接包输出

Use when design output is unnecessary and the next consumer is engineering.

Produce:

- data objects and fields
- actions/APIs
- permissions
- acceptance criteria
- edge cases
- analytics events
- visual or interaction checks

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

If the user chooses an option, immediately produce the matching platform contract above.

## Avoid

- Automatically producing high-fidelity design when the user only approved PRD.
- Uploading files to third-party tools without explicit approval.
- Treating design output as mandatory.
- Sending a full PRD to every specialist when only page specs are needed.
