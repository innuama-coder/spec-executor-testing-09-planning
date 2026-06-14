# spec-executor-testing-09-planning

规划型独立测试仓库。该仓库用于验证 spec-executor 是否能够驱动 agent 使用研究规划、设计规划和开发规划技能，产出可调度的任务计划。

## 目录

- `docs/PRD.md`
- `docs/HLD.md`
- `docs/LLD.md`
- `docs/DELIVERY.md`
- `inputs/project-brief.md`
- `tasks/research-planning/`
- `tasks/design-planning/`
- `tasks/development-planning/`

## 运行

```bash
spec-executor run --spec tasks/research-planning/spec.yaml --workspace ./workspace
spec-executor run --spec tasks/design-planning/spec.yaml --workspace ./workspace
spec-executor run --spec tasks/development-planning/spec.yaml --workspace ./workspace
```
