# Omni SuperDev

Omni SuperDev 是一个独立的全流程研发 skill。

它基于 `Superpowers` 的工程纪律模型改造而来，并把 `Superpowers` 全量内容与常用研发 companion 能力整合进 `skills/omni-superdev/` 这一个 skill 目录中。用户安装 Omni SuperDev 后，不需要再额外安装 `Superpowers` 或其它 companion skills 才能跑完整链路。

## 定位

Omni SuperDev 本身就是一套从产品意图到技术方案、实现、测试、评审、验证、收口的完整研发流程。

核心能力包括：

- 产品发现、需求澄清、方案设计
- 技术计划、任务拆分、持久化规划
- TDD 行为变更与 bugfix
- 根因导向调试
- UI/UX、本地 Web QA、MCP、GitHub PR/CI、代码评审
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
- `mcp-builder`
- `gh-fix-ci`
- `gh-address-comments`
- `brooks-review`
- `_shared`（`brooks-review` 依赖的支持文件）

## 使用方式

用户只需要触发 `omni-superdev`。当流程需要更细的纪律或专项能力时，Omni SuperDev 会读取自己目录下的内置参考资料并执行对应流程，而不是要求用户另装其它 skill。

典型链路：

- 新功能：产品发现 → 方案设计 → 技术计划 → TDD 实现 → 评审 → 验证
- Bug 修复：复现 → 根因调查 → 回归测试 → 最小修复 → 验证
- UI 工作：需求与交互确认 → UI/UX 指南 → 本地 Web QA → 验证
- PR/CI：检查失败原因 → 技术判断 → 修复 → 复验 → 回应评论

## 运行时前提

某些内置流程在真正执行时仍然需要常规本地工具，例如：

- Python：用于脚本型流程
- `gh`：用于 GitHub PR / CI 流程
- Playwright 与本地开发服务器：用于浏览器测试和本地 Web QA

这些是运行时工具，不是额外 skill 安装依赖。

## 许可证

当前仓库已经包含第三方打包内容的许可证说明。

- 第三方来源与归属说明：[docs/third-party.md](./docs/third-party.md)
- 仓库顶层许可证：[LICENSE](./LICENSE)
- 许可补充说明：[LICENSE-NOTICE.md](./LICENSE-NOTICE.md)
