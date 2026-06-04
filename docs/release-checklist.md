# 发布检查清单

在把 Omni SuperDev 发布到 GitHub 之前，可以按这份清单做最后确认。

## 必查项

- [ ] 确认根目录 [LICENSE](../LICENSE) 符合你希望公开发布 Omni SuperDev 包装层内容的方式
- [ ] 确认每个内置第三方目录中的许可证文件仍然保留
- [ ] 确认 [third-party.md](./third-party.md) 中的上游来源与归属说明仍然准确
- [ ] 确认安装说明里强调的是安装完整 `skills/omni-superdev/` 目录
- [ ] 确认 `skills/omni-superdev/references/bundled/_shared/` 与 Brooks 系列目录保持同级
- [ ] 确认 `skills/omni-superdev/references/automation-matrix.md` 与 `workflow-map.md` 的阶段说明一致
- [ ] 确认 README 与 docs 中没有残留本地路径、私有项目说明或无关上下文

## 建议检查

- [ ] 打开 [README.md](../README.md) 看一遍首页说明是否清晰
- [ ] 打开 [install.md](./install.md) 确认安装结构与当前仓库一致
- [ ] 抽查 `skills/omni-superdev/SKILL.md` 是否仍然表达为独立全流程 skill
- [ ] 对内置的 `ui-ux-pro-max`、`planning-with-files`、`jupyter-notebook`、`security-ownership-map` 做一次代表性脚本冒烟验证
- [ ] 检查新增内置模块没有残留必须安装外部同名 skill 的路径说明

## 首个 Release 可直接使用的说明方向

- 一个可直接安装的 Omni SuperDev 独立 skill
- 基于 `Superpowers` 工作流模型改造
- 已内置研发自动化矩阵与常用专项能力，用户不需要再额外安装 companion skills
- 已附带第三方来源说明与各内置内容对应许可证文件
