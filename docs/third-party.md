# 第三方打包 Skills 说明

当前仓库打包了若干第三方 skill 内容，目的是让用户只安装这一套仓库，就能直接获得常用 companion skills，而不需要分别单独安装。

每个第三方 skill 仍然在自己的目录中保留了原始许可证文本。

## 已打包组件

| 打包路径 | 上游来源 | 许可证 |
| --- | --- | --- |
| `skills/planning-with-files` | 基于 [OthmanAdi/planning-with-files](https://github.com/OthmanAdi/planning-with-files) 的 Codex 兼容打包版本 | MIT |
| `skills/ui-ux-pro-max` | [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | MIT |
| `skills/brooks-review` | [hyhmrright/brooks-lint](https://github.com/hyhmrright/brooks-lint) | MIT |
| `skills/_shared` | [hyhmrright/brooks-lint](https://github.com/hyhmrright/brooks-lint) | MIT |
| `skills/webapp-testing` | Codex / OpenAI 打包 skill 发行内容 | Apache-2.0 |
| `skills/mcp-builder` | Codex / OpenAI 打包 skill 发行内容 | Apache-2.0 |
| `skills/gh-fix-ci` | Codex / OpenAI 打包 skill 发行内容 | Apache-2.0 |
| `skills/gh-address-comments` | Codex / OpenAI 打包 skill 发行内容 | Apache-2.0 |

## 补充说明

- `Omni SuperDev` 本身是当前仓库中的路由与包装层。
- 仓库顶层 [LICENSE](../LICENSE) 适用于 Omni SuperDev 自身的包装内容以及仓库级文档与打包整理内容。
- 第三方 skill 仍然分别受其各自目录中附带的许可证文件约束。
- 在再次分发或二次打包前，请同时阅读 [../LICENSE-NOTICE.md](../LICENSE-NOTICE.md)。
