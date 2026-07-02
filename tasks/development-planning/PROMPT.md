# PROMPT.md

## 任务目标

使用 `development-planning` 技能，规划任务质量仪表盘项目的开发与测试任务。

## 必读上下文

2. `docs/LLD.md`
3. `inputs/project-brief.md`

## 交付物

> 所有交付物路径均**相对仓库/worktree 根目录**（执行者的工作目录），例如 `outputs/PRD.md` 指根目录下的 `outputs/PRD.md`，不要写到 `tasks/` 子目录下。

- `plans/development-plan.md`

## 验收标准

- 包含开发任务、测试任务、依赖、验收命令、并行策略和停止条件。
- 不实现代码。

## Handoff

最终回复包含计划路径、执行顺序和测试策略。

## spec-executor 2.3 Agent Task Lifecycle 约束

- 本任务包通过 `spec.yaml` 的 `execution.agent` 声明 Agent 角色、上下文、工具和权限边界。
- `ENV` 仅用于 tmux session 环境变量注入，不作为普通上下文文件读取、总结或输出。
- 默认输出、报告和交付说明不得包含 `ENV` 变量值。
- `spec.yaml` 中存在 review items 时，必须在同一 JOB 内逐条完成修复、验证和交付记录。
- 运行过程必须保持 log-first detection 边界；screen capture 只作为显式查看或失败证据。
