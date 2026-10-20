# 仓库目录说明

[返回首页](../README.md)

## 普通使用者

1. 按[安装与使用指南](installation.md)安装技能，在 Codex 中附图调用。
2. 通过[效果预览](../examples/README.md)查看成片和对应原提示词。
3. 如需了解多轮制作过程，读[对话参考索引](../examples/conversations/README.md)。

## 文件用途

| 文件或目录 | 内容 |
|---|---|
| [README.md](../README.md) | 仓库首页与快速入口 |
| [VERSION](../VERSION) / [CHANGELOG.md](../CHANGELOG.md) | 当前包版本与版本变化 |
| [docs/installation.md](installation.md) | 安装、调用、更新和固定版本 |
| [docs/maintenance.md](maintenance.md) | 修改、校验、提交与发布步骤 |
| [examples/README.md](../examples/README.md) | 两条生成直出预览索引 |
| [examples/media.json](../examples/media.json) | 视频下载地址、大小及 SHA-256 |
| examples/abyss-tide/ | 渊潮魇王封面与完整提示词 |
| examples/stitched-spider/ | 缝身蛛后封面与完整提示词 |
| [examples/conversations/README.md](../examples/conversations/README.md) | 对话、测试模板、观察记录入口 |
| [SKILL.md](../SKILL.md) | Codex 加载的技能入口 |
| [references/workflow.md](../references/workflow.md) | 有方向／无方向两条制作路径 |
| [references/setting-contract.md](../references/setting-contract.md) | 觉醒设定与替换字段要求 |
| [references/impact-contract.md](../references/impact-contract.md) | 母版爆发机制对照 |
| [references/mechanism-camera-contract.md](../references/mechanism-camera-contract.md) | 六类机制、运镜与衔接要求 |
| [assets/master-original.txt](../assets/master-original.txt) | 原始母版 |
| [assets/master-template.md](../assets/master-template.md) | 中括号替换模板 |
| [agents/openai.yaml](../agents/openai.yaml) | 技能显示信息 |

## 保存规则

通用执行规则在 SKILL.md 和 references；母版在 assets；公开案例和历史证据在 examples；面向人的使用文档在 docs。具体角色的制作状态保存在使用者自己的工程目录。

视频原件放在 GitHub Release，仓库只收录封面、提示词和校验信息。运行资源与现有案例路径保留，旧链接和安装命令继续有效。
