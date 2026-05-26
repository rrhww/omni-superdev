# 第三方内置内容说明

当前仓库把第三方 skill 内容整合进 `skills/omni-superdev/references/bundled/`，目的是让用户只安装 `omni-superdev/` 这一个独立 skill，就能直接获得完整研发流程。

每个第三方来源目录仍然保留了原始许可证文本。

## 已内置组件

| 内置路径 | 上游来源 | 许可证 |
| --- | --- | --- |
| `skills/omni-superdev/references/bundled/planning-with-files` | 基于 [OthmanAdi/planning-with-files](https://github.com/OthmanAdi/planning-with-files) 的 Codex 兼容打包版本 | MIT |
| `skills/omni-superdev/references/bundled/ui-ux-pro-max` | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | MIT |
| `skills/omni-superdev/references/bundled/brooks-review` | [hyhmrright/brooks-lint](https://github.com/hyhmrright/brooks-lint) | MIT |
| `skills/omni-superdev/references/bundled/_shared` | [hyhmrright/brooks-lint](https://github.com/hyhmrright/brooks-lint) | MIT |
| `skills/omni-superdev/references/bundled/webapp-testing` | Codex / OpenAI 打包 skill 发行内容 | Apache-2.0 |
| `skills/omni-superdev/references/bundled/mcp-builder` | Codex / OpenAI 打包 skill 发行内容 | Apache-2.0 |
| `skills/omni-superdev/references/bundled/gh-fix-ci` | Codex / OpenAI 打包 skill 发行内容 | Apache-2.0 |
| `skills/omni-superdev/references/bundled/gh-address-comments` | Codex / OpenAI 打包 skill 发行内容 | Apache-2.0 |
| `skills/omni-superdev/references/bundled/brainstorming` 等完整打包的 Superpowers 内容 | 本地安装的 [Superpowers](https://github.com/obra/superpowers) | MIT |

## 完整内置的 Superpowers 目录

以下目录来自本地安装的 [Superpowers](https://github.com/obra/superpowers)，并作为完整内容随 `omni-superdev/` 分发：

- `skills/omni-superdev/references/bundled/brainstorming`
- `skills/omni-superdev/references/bundled/dispatching-parallel-agents`
- `skills/omni-superdev/references/bundled/executing-plans`
- `skills/omni-superdev/references/bundled/finishing-a-development-branch`
- `skills/omni-superdev/references/bundled/receiving-code-review`
- `skills/omni-superdev/references/bundled/requesting-code-review`
- `skills/omni-superdev/references/bundled/subagent-driven-development`
- `skills/omni-superdev/references/bundled/systematic-debugging`
- `skills/omni-superdev/references/bundled/test-driven-development`
- `skills/omni-superdev/references/bundled/using-git-worktrees`
- `skills/omni-superdev/references/bundled/using-superpowers`
- `skills/omni-superdev/references/bundled/verification-before-completion`
- `skills/omni-superdev/references/bundled/writing-plans`
- `skills/omni-superdev/references/bundled/writing-skills`

## 补充说明

- `Omni SuperDev` 自身是当前仓库中的独立 skill。
- 仓库顶层 [LICENSE](../LICENSE) 适用于 Omni SuperDev 自身的包装内容以及仓库级文档与打包整理内容。
- 第三方内容仍然分别受其各自目录中附带的许可证文件约束。
- 在再次分发或二次打包前，请同时阅读 [../LICENSE-NOTICE.md](../LICENSE-NOTICE.md)。
