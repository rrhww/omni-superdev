# Omni SuperDev 打包说明

这个目录现在已经整理成一个可单独分发的 `skill suite` 仓库，而不是单一 skill 包。

## 定位

`Omni SuperDev` 是一个基于 `Superpowers` 思路改造出来的全流程开发套件。

但它现在的发布形态不是“先装主 skill，再补装一堆依赖 skill”，而是把常用核心能力和专项能力一起随仓库分发，让用户一次安装即可使用完整链路。

可以这样理解：

- `omni-superdev` 负责总流程路由
- `omni-tdd`、`omni-debug`、`omni-verify`、`omni-file-planning` 负责套件自带的轻量纪律能力
- `planning-with-files`、`ui-ux-pro-max`、`webapp-testing`、`mcp-builder`、`gh-fix-ci`、`gh-address-comments`、`brooks-review` 已经作为专项能力随仓库一起打包

## 包内内容

核心 Omni skills：

- `skills/omni-superdev/`
- `skills/omni-tdd/`
- `skills/omni-debug/`
- `skills/omni-verify/`
- `skills/omni-file-planning/`

随仓库分发的专项 skills：

- `skills/planning-with-files/`
- `skills/ui-ux-pro-max/`
- `skills/webapp-testing/`
- `skills/mcp-builder/`
- `skills/gh-fix-ci/`
- `skills/gh-address-comments/`
- `skills/brooks-review/`
- `skills/_shared/`

其中 `skills/_shared/` 是 `brooks-review` 的依赖目录，不能漏掉。

## 适用场景

这个套件适合做以下入口：

- 新功能开发
- Bug 修复
- 端到端交付
- 产品需求到技术方案到实现到测试的完整链路
- 前后端混合任务
- UI、MCP、PR、CI、代码评审等统一调度场景

## 安装方式

将仓库中的 `skills/` 目录内容整体复制到目标环境的 skills 目录中，并保留原有目录结构。

常见位置：

- `~/.agents/skills/`
- 其他支持 skills 发现机制的本地目录

不要只复制 `omni-superdev/` 一个目录，否则被一起打包的专项能力不会完整可用。

## “不需要额外安装” 的含义

现在用户不需要再单独安装这些专项 skill：

- `planning-with-files`
- `ui-ux-pro-max`
- `webapp-testing`
- `mcp-builder`
- `gh-fix-ci`
- `gh-address-comments`
- `brooks-review`

但某些专项流程在真正执行时，仍然可能依赖本地运行环境，例如：

- Python
- `gh` GitHub CLI
- Playwright
- 本地开发服务器

这些属于运行时工具前提，不属于额外 skill 安装。

## 许可说明

- 第三方打包来源与许可证：见 [third-party.md](./third-party.md)
- 仓库根许可证状态：见 [../LICENSE-NOTICE.md](../LICENSE-NOTICE.md)

如果你准备公开发布这个仓库，仍然建议为你自己的 Omni SuperDev 包装层内容补一个顶层 `LICENSE` 文件。
