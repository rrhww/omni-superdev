# 安装 Omni SuperDev

## 快速安装

只需要安装一个 skill 目录：

```text
skills/
  omni-superdev/
```

把当前仓库中的 [`skills/omni-superdev/`](../skills/omni-superdev) 放到 Codex 可发现的 skills 目录中，并保留目录内部结构。

常见目标位置：

- `~/.agents/skills/omni-superdev/`
- 你当前环境支持的项目级 skills 目录

## 重要说明

Omni SuperDev 的安装单位是完整的 `omni-superdev/` 目录。

完整流程能力已经内置在：

```text
skills/omni-superdev/references/bundled/
```

也就是说，用户只安装 `omni-superdev/` 这一个目录，就能获得：

- 完整保留的 `Superpowers` 全量流程内容
- 产品发现、技术计划、TDD、调试、验证、评审、分支收口
- 持久化规划、UI/UX、本地 Web QA、MCP、GitHub PR/CI、代码评审等 companion 能力

## 运行时前提

某些内置流程在真正执行时仍然依赖本地常规工具环境，例如：

- Python：用于脚本型流程
- `gh`：用于 GitHub PR / CI 流程
- Playwright 与本地开发服务器：用于浏览器测试和本地 Web QA

这些属于运行时前提，不属于额外 skill 安装依赖。
