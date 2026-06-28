# 同类项目对比与 Z-PRD 取舍

> 调研时间：2026-06-28。Stars 会变化，下表用于说明设计取舍，不作为排名承诺。

## 热门参考项目

| 项目 | 当时 Stars | 主要特点 | Z-PRD 借鉴点 |
| --- | ---: | --- | --- |
| [product-on-purpose/pm-skills](https://github.com/product-on-purpose/pm-skills) | 425 | 68 个 PM skills、子 agents、workflow、模板、样例输出、CI 合约 | 借鉴 skill registry、子 agent 分层和样例质量标准 |
| [aakashg/pm-claude-code-setup](https://github.com/aakashg/pm-claude-code-setup) | 139 | 短 `CLAUDE.md`、6 个 PM skills、4 个模板，强调 60 秒可用 | 借鉴轻量入口、短上下文和可复制安装方式 |
| [Digidai/product-manager-skills](https://github.com/Digidai/product-manager-skills) | 117 | PM operator 定位，强调 PRD critique、SaaS 指标诊断和示例输出 | 借鉴 README 定位、示例驱动和“不是模板包”的表达 |
| [vishalmdi/ai-native-pm-os](https://github.com/vishalmdi/ai-native-pm-os) | 91 | PM 操作系统课程，强调上下文工程、agents 和长期工作基础设施 | 借鉴长期上下文和 PM OS 思路，但不做课程化 |
| [yanivy9h/ai-shipr](https://github.com/yanivy9h/ai-shipr) | 25 | 文件夹式产品记忆系统，强调 strategy、hypotheses、initiatives、proof | 借鉴可持续项目上下文，但不默认引入复杂状态目录 |

## Z-PRD 的选择

`Z-PRD` 不追求大而全。它专注一条高频链路：

```text
一句话想法 -> PRD -> 产品设计 -> UI 原型计划 -> 研发交接
```

## 为什么不拆成很多 Skill

多 skill 库适合完整 PM 操作系统，但对 Codex 日常使用有三个代价：

- 触发成本：多个相近描述容易同时匹配或误匹配。
- 上下文成本：每个 skill 都会带来额外说明和模板。
- 决策成本：用户要先知道该选哪个入口。

因此 `Z-PRD` 采用单入口：用户只记住 `$z-prd`，主 skill 决定当前该做需求、设计、原型还是交接。

## 多 Agent 怎么保留

多 agent 不作为默认入口，而作为复杂任务的可选执行策略：

- 需求复杂时拆“需求分析视角”。
- 状态/权限/对象复杂时拆“产品设计视角”。
- 需要可运行界面时拆“UI 原型视角”。
- 要交给开发时拆“研发交接视角”。

这样可以保留专家分工，同时避免所有任务都启动多个 agent。

## Token 优化策略

- 主 `SKILL.md` 只放触发、流程和关键规则。
- 长模板放 `references/product-flow-template.md`。
- 多 agent 规则放 `references/multi-agent-routing.md`。
- 节省上下文方法放 `references/token-budget-guide.md`。
- README 面向人读，不让每次 skill 触发都加载整篇说明。

## 适合继续扩展的方向

- 增加 `examples/`：展示一句话需求到产品文档的完整样例。
- 增加 `docs/context-workspace.md`：说明长期项目如何维护产品上下文。
- 增加轻量检查清单：PRD ready、prototype ready、handoff ready。
- 增加 Marketplace metadata：让安装入口更友好。
