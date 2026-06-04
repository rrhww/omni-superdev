# Omni SuperDev

Omni SuperDev 是一个独立的全流程研发自动化 skill。

它基于 `Superpowers` 的工程纪律模型改造而来，并把 `Superpowers` 全量内容、常用研发 companion 能力，以及扩展研发自动化模块整合进 `skills/omni-superdev/` 这一个 skill 目录中。用户安装 Omni SuperDev 后，不需要再额外安装 `Superpowers` 或其它 companion skills 才能跑完整链路。

## 定位

Omni SuperDev 本身就是一套从代码库侦察、产品意图、技术方案、实现、测试、安全、评审、发布说明、验证到收口的完整研发自动化流程。

核心能力包括：

- 产品发现、需求澄清、方案设计
- 技术计划、任务拆分、持久化规划
- TDD 行为变更与 bugfix
- 根因导向调试
- UI/UX、本地 Web QA、通用 Playwright、交互式浏览器/Electron 调试、系统截图
- MCP、GitHub PR/CI、代码评审、代码库健康评估、测试质量评估
- 安全最佳实践、威胁建模、安全所有权/Bus Factor 分析
- Codex 迁移、Notebook 实验/教程、发布说明/变更日志
- 完成前验证与分支收口
- skill 编写与维护方法

## 安装

只需要安装这一个目录：

```text
skills/
  omni-superdev/
```

仓库中真正用于分发的目录是 [`skills/omni-superdev`](./skills/omni-superdev)。

安装时把 `skills/omni-superdev/` 放到 Codex 可发现的 skills 目录中即可，例如：

- `~/.agents/skills/omni-superdev/`
- 你当前环境支持的项目级或个人级 skills 目录

## 内置内容

Omni SuperDev 的内置资料位于：

```text
skills/omni-superdev/references/bundled/
```

其中完整保留了 `Superpowers` 的 14 个 skill 内容：

- `brainstorming`
- `dispatching-parallel-agents`
- `executing-plans`
- `finishing-a-development-branch`
- `receiving-code-review`
- `requesting-code-review`
- `subagent-driven-development`
- `systematic-debugging`
- `test-driven-development`
- `using-git-worktrees`
- `using-superpowers`
- `verification-before-completion`
- `writing-plans`
- `writing-skills`

同时内置了这些 companion 能力：

- `planning-with-files`
- `ui-ux-pro-max`
- `webapp-testing`
- `playwright`
- `playwright-interactive`
- `screenshot`
- `mcp-builder`
- `migrate-to-codex`
- `gh-fix-ci`
- `gh-address-comments`
- `brooks-review`
- `brooks-health`
- `brooks-test`
- `security-best-practices`
- `security-threat-model`
- `security-ownership-map`
- `jupyter-notebook`
- `_shared`（`brooks-review` 依赖的支持文件）

此外，`skills/omni-superdev/references/automation-matrix.md` 提供 Omni 自己的研发自动化矩阵，用于代码库侦察、实现后简化、发布说明/变更日志、以及不能直接公开分发的辅助能力边界。

## 使用方式

用户只需要触发 `omni-superdev`。当流程需要更细的纪律或专项能力时，Omni SuperDev 会读取自己目录下的内置参考资料并执行对应流程，而不是要求用户另装其它 skill。

典型链路：

- 新功能：产品发现 → 方案设计 → 技术计划 → TDD 实现 → 评审 → 验证
- Bug 修复：复现 → 根因调查 → 回归测试 → 最小修复 → 验证
- UI 工作：需求与交互确认 → UI/UX 指南 → 浏览器/截图 QA → 验证
- 安全工作：敏感面识别 → 安全最佳实践 → 威胁建模或所有权分析 → 修复/报告
- 发布准备：验证 → 健康/测试质量/安全检查 → 变更日志 → 分支收口
- PR/CI：检查失败原因 → 技术判断 → 修复 → 复验 → 回应评论

## 运行时前提

某些内置流程在真正执行时仍然需要常规本地工具，例如：

- Python：用于脚本型流程
- `gh`：用于 GitHub PR / CI 流程
- Node/npm、Playwright 与本地开发服务器：用于浏览器自动化、本地 Web QA、交互式调试
- `networkx`：用于安全所有权图分析

这些是运行时工具，不是额外 skill 安装依赖。

## 许可证

当前仓库已经包含第三方打包内容的许可证说明。

- 第三方来源与归属说明：[docs/third-party.md](./docs/third-party.md)
- 仓库顶层许可证：[LICENSE](./LICENSE)
- 许可补充说明：[LICENSE-NOTICE.md](./LICENSE-NOTICE.md)
