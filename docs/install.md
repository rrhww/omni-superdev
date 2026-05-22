# 安装 Omni SuperDev

## 快速安装

把当前仓库 `skills/` 目录中的内容整体复制到 Codex 可发现的 skills 目录中。

目标结构应类似如下：

```text
skills/
  omni-superdev/
  omni-tdd/
  omni-debug/
  omni-verify/
  omni-file-planning/
  planning-with-files/
  ui-ux-pro-max/
  webapp-testing/
  mcp-builder/
  gh-fix-ci/
  gh-address-comments/
  brooks-review/
  _shared/
```

其中 `_shared/` 是 `brooks-review` 的依赖目录，必须与其他 skill 目录放在同一层级。

## 常见安装位置

根据你的使用环境，常见位置包括：

- `~/.agents/skills/`
- 你当前环境支持的项目级 skills 目录

## 重要说明

不要只复制 `omni-superdev/` 一个目录。

请复制当前仓库 `skills/` 目录下的全部内容，并保留原有目录结构。否则像 `brooks-review`、`planning-with-files` 这类已打包的专项能力会变成不完整状态。

## 当前已包含的内容

这套仓库已经自带：

- Omni 总路由与轻量纪律 skills
- 持久化规划能力
- UI/UX 指导能力
- 本地 Web 测试能力
- MCP 工作流指导能力
- GitHub PR / CI 辅助能力
- 代码评审能力

也就是说，用户不需要再额外安装这些常见 companion skills。

## 运行时前提

某些已打包 skill 在真正执行时，仍然依赖本地常规工具环境，例如：

- Python：用于脚本型 skill
- `gh`：用于 GitHub PR / CI 流程
- Playwright 与本地开发服务器：用于浏览器测试和本地 Web QA

这些属于运行时前提，不属于额外的 skill 安装依赖。
