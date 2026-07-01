# PROMPT.md

## 任务目标

使用 `research-planning` 技能，规划任务质量仪表盘项目的研究任务。

## 必读上下文

1. `C:/Users/54256213/.codex/skills/research-planning/SKILL.md`
2. `docs/PRD.md`
3. `inputs/project-brief.md`

## 交付物

- `plans/research-plan.md`

## 验收标准

- 包含研究任务、依赖、验收、并行策略和停止条件。
- 不包含研究结论。

## Handoff

最终回复包含计划路径和任务批次。

## spec-executor 2.3 Agent Task Lifecycle 约束

- 本任务包通过 `spec.yaml` 的 `execution.agent` 声明 Agent 角色、上下文、工具和权限边界。
- `ENV` 仅用于 tmux session 环境变量注入，不作为普通上下文文件读取、总结或输出。
- 默认输出、报告和交付说明不得包含 `ENV` 变量值。
- `spec.yaml` 中存在 review items 时，必须在同一 JOB 内逐条完成修复、验证和交付记录。
- 运行过程必须保持 log-first detection 边界；screen capture 只作为显式查看或失败证据。
