# Omni SuperDev

Omni SuperDev 是一套面向全流程软件与产品开发的自包含 skill suite。

它基于 `Superpowers` 的工程纪律模型改造而来，但发布形态不是“主 skill + 一堆额外依赖”的方式，而是直接打包成一套可安装、可分发的完整技能集合，用户不需要再单独安装常见 companion skills。

## 定位

你可以把这套 skill 理解成：

- `omni-superdev` 负责总流程路由
- `omni-tdd`、`omni-debug`、`omni-verify`、`omni-file-planning` 提供套件自带的轻量纪律层
- 已打包的专项 skills 负责补足 UI/UX、本地 Web 测试、MCP、PR/CI、代码评审、持久化规划等能力

这让 Omni SuperDev 很适合作为软件与产品工作的默认入口，尤其适用于可能横跨后端、前端、UI、测试、PR/CI、MCP 的混合型任务。

## 已内置 Skills

核心 Omni skills：

- `omni-superdev`
- `omni-tdd`
- `omni-debug`
- `omni-verify`
- `omni-file-planning`

已打包的专项 skills：

- `planning-with-files`
- `ui-ux-pro-max`
- `webapp-testing`
- `mcp-builder`
- `gh-fix-ci`
- `gh-address-comments`
- `brooks-review`
- `_shared`（`brooks-review` 依赖的支持文件）

## 典型路由方式

- 小任务：查看、修改、验证、总结
- 标准开发：澄清产品目标，梳理技术方案，对行为变更走 TDD，再实现、收敛、验证
- 复杂任务或跨会话任务：先做持久化规划，再按阶段推进
- 调试或测试失败：先做根因导向的调试，再决定修复方案
- UI/UX：路由到 `ui-ux-pro-max`
- 本地 Web QA：路由到 `webapp-testing`
- MCP 工作流：路由到 `mcp-builder`
- PR / CI 工作流：路由到 `gh-fix-ci`、`gh-address-comments` 或 `brooks-review`

## 安装方式

详见 [docs/install.md](./docs/install.md)。

简而言之，把当前仓库中的 [`skills/`](./skills) 目录内容整体复制到 Codex 可发现的 skills 目录中，并保留原有目录结构。

常见安装位置：

- `~/.agents/skills/`
- 你当前环境支持的项目级或个人级 skills 目录

## “不需要额外安装” 是什么意思

现在用户不需要再单独安装这些常见专项 skill：

- `planning-with-files`
- `ui-ux-pro-max`
- `webapp-testing`
- `mcp-builder`
- `gh-fix-ci`
- `gh-address-comments`
- `brooks-review`

当然，某些路由在真正执行时仍然依赖正常的本地运行环境，例如：

- Python：用于脚本型 skill
- `gh`：用于 GitHub PR / CI 流程
- Playwright 或本地开发服务器：用于浏览器测试与本地 Web QA

这些属于运行时前提，不属于额外的 skill 安装依赖。

## 许可证

当前仓库已经包含第三方打包 skill 的许可证文件。

- 第三方来源与归属说明：[docs/third-party.md](./docs/third-party.md)
- 仓库顶层许可证：[LICENSE](./LICENSE)
- 许可补充说明：[LICENSE-NOTICE.md](./LICENSE-NOTICE.md)
