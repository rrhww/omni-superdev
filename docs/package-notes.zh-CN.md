# Omni SuperDev 打包说明

这个仓库现在按“独立 skill”方式打包。

## 定位

`Omni SuperDev` 是一个基于 `Superpowers` 思路改造出来的全流程研发自动化 skill。

它的发布形态是一个独立目录：

```text
skills/omni-superdev/
```

`Superpowers` 全量内容、常用 companion 能力与扩展研发自动化模块已经整合进这个目录的 `references/bundled/` 下。用户安装 `omni-superdev/` 后，不需要再单独安装 `Superpowers`、`planning-with-files`、`ui-ux-pro-max`、`webapp-testing`、`mcp-builder`、`gh-fix-ci`、`gh-address-comments`、`brooks-review`、`brooks-health`、`brooks-test`、`playwright`、`playwright-interactive`、`screenshot`、`migrate-to-codex`、`security-best-practices`、`security-threat-model`、`security-ownership-map` 或 `jupyter-notebook`。

## 包内内容

主入口：

- `skills/omni-superdev/SKILL.md`
- `skills/omni-superdev/agents/openai.yaml`
- `skills/omni-superdev/references/automation-matrix.md`
- `skills/omni-superdev/references/workflow-map.md`
- `skills/omni-superdev/references/conflict-policy.md`

内置全量 `Superpowers` 内容：

- `skills/omni-superdev/references/bundled/brainstorming/`
- `skills/omni-superdev/references/bundled/dispatching-parallel-agents/`
- `skills/omni-superdev/references/bundled/executing-plans/`
- `skills/omni-superdev/references/bundled/finishing-a-development-branch/`
- `skills/omni-superdev/references/bundled/receiving-code-review/`
- `skills/omni-superdev/references/bundled/requesting-code-review/`
- `skills/omni-superdev/references/bundled/subagent-driven-development/`
- `skills/omni-superdev/references/bundled/systematic-debugging/`
- `skills/omni-superdev/references/bundled/test-driven-development/`
- `skills/omni-superdev/references/bundled/using-git-worktrees/`
- `skills/omni-superdev/references/bundled/using-superpowers/`
- `skills/omni-superdev/references/bundled/verification-before-completion/`
- `skills/omni-superdev/references/bundled/writing-plans/`
- `skills/omni-superdev/references/bundled/writing-skills/`

内置 companion 能力：

- `skills/omni-superdev/references/bundled/planning-with-files/`
- `skills/omni-superdev/references/bundled/ui-ux-pro-max/`
- `skills/omni-superdev/references/bundled/webapp-testing/`
- `skills/omni-superdev/references/bundled/playwright/`
- `skills/omni-superdev/references/bundled/playwright-interactive/`
- `skills/omni-superdev/references/bundled/screenshot/`
- `skills/omni-superdev/references/bundled/mcp-builder/`
- `skills/omni-superdev/references/bundled/migrate-to-codex/`
- `skills/omni-superdev/references/bundled/gh-fix-ci/`
- `skills/omni-superdev/references/bundled/gh-address-comments/`
- `skills/omni-superdev/references/bundled/brooks-review/`
- `skills/omni-superdev/references/bundled/brooks-health/`
- `skills/omni-superdev/references/bundled/brooks-test/`
- `skills/omni-superdev/references/bundled/security-best-practices/`
- `skills/omni-superdev/references/bundled/security-threat-model/`
- `skills/omni-superdev/references/bundled/security-ownership-map/`
- `skills/omni-superdev/references/bundled/jupyter-notebook/`
- `skills/omni-superdev/references/bundled/_shared/`

Omni 原生自动化能力：

- 代码库侦察与风险面识别
- 实现后简化
- 发布说明/变更日志整理
- 不能公开分发的本地辅助 skill 对应能力边界说明

## 适用场景

这个 skill 适合做以下入口：

- 新功能开发
- Bug 修复
- 端到端交付
- 产品需求到技术方案到实现到测试的完整链路
- 前后端混合任务
- UI、MCP、PR、CI、代码评审、安全、质量、浏览器自动化、迁移、Notebook 等统一研发流程
- 发布准备、变更日志、分支收口
- skill 编写与维护

## 安装方式

将仓库中的 `skills/omni-superdev/` 整体放到目标环境的 skills 目录中，并保留内部结构。

不要只复制 `SKILL.md`，否则内置参考资料、脚本、模板和许可证文件不会完整可用。

## 许可说明

- 第三方打包来源与许可证：见 [third-party.md](./third-party.md)
- 仓库根许可证状态：见 [../LICENSE-NOTICE.md](../LICENSE-NOTICE.md)
