# CLAUDE.md

## Assignment

使用 `research-planning` 技能规划研究任务。

## Context To Load

- `C:/Users/54256213/.codex/skills/research-planning/SKILL.md`
- `docs/PRD.md`
- `inputs/project-brief.md`

## Constraints

- 不执行研究。
- 不修改 task package。

## Acceptance Criteria

- `plans/research-plan.md` 包含任务、依赖、验收和并行批次。

## Verification Method

运行 spec.yaml 中的 verify 命令。

## Handoff

说明计划路径和调度建议。

## spec-executor 2.3 Agent Task Lifecycle 约束

- 本任务包通过 `spec.yaml` 的 `execution.agent` 声明 Agent 角色、上下文、工具和权限边界。
- `ENV` 仅用于 tmux session 环境变量注入，不作为普通上下文文件读取、总结或输出。
- 默认输出、报告和交付说明不得包含 `ENV` 变量值。
- `spec.yaml` 中存在 review items 时，必须在同一 JOB 内逐条完成修复、验证和交付记录。
- 运行过程必须保持 log-first detection 边界；screen capture 只作为显式查看或失败证据。
