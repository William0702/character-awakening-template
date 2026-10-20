# 角色觉醒与法相模板

给一张初始角色图，先确定觉醒方向与详细设定，确认后生成15秒四段式变身与法相提示词。

**使用流程：角色图 → 有方向直接深化／无方向五选一 → 审核觉醒设定与爆发运镜 → 确认后输出完整提示词。**

## 从这里开始

| 你想做什么 | 对应入口 |
|---|---|
| 安装技能、开始使用、同步最新版本 | [安装与使用指南](docs/installation.md) |
| 看实际生成视频与配套提示词 | [效果预览](examples/README.md) |
| 看真实对话如何选方向、确认和修改 | [对话参考](examples/conversations/README.md) |
| 自己跑一轮测试并记录问题 | [可复制测试模板](examples/conversations/test-template.md) |
| 看版本变化 | [更新记录](CHANGELOG.md) |
| 修改技能、发布新版本 | [维护指南](docs/maintenance.md) |
| 理解每个文件的用途 | [目录说明](docs/repository-map.md) |

## 生成直出预览

| 渊潮魇王 | 缝身蛛后 |
|---|---|
| [![渊潮魇王](examples/abyss-tide/poster.jpg)](https://github.com/William0702/character-awakening-template/releases/download/v1.2.1/abyss-tide.mp4) | [![缝身蛛后](examples/stitched-spider/poster.jpg)](https://github.com/William0702/character-awakening-template/releases/download/v1.2.1/stitched-spider.mp4) |
| [完整提示词](examples/abyss-tide/prompt.md) | [完整提示词](examples/stitched-spider/prompt.md) |

点击封面打开原始视频。视频保存在 Release，安装技能时不会下载视频。示例缺少完整模型配置和初始角色图，不作为效果保证。

## 快速安装与调用

Windows PowerShell，需要已安装 Git；目标目录应不存在，自定义 CODEX_HOME 的用户需调整路径：

```powershell
git clone https://github.com/William0702/character-awakening-template.git "$env:USERPROFILE\.codex\skills\character-awakening-template"
```

安装后在新聊天中附上角色图，输入：

```text
使用 $character-awakening-template，这是我的初始角色，我没有具体方向。
```

已有想法时，把“没有具体方向”替换为自己的方向。未选中时可继续换新；详细设定经你确认后，才填写完整母版。技能不自动调用付费生成服务。

更新已安装版本：

```powershell
git -C "$env:USERPROFILE\.codex\skills\character-awakening-template" pull --ff-only
```

这是手动同步；遇到本地修改或冲突时先处理差异。更多说明见[安装与使用指南](docs/installation.md)。

## 文件分区

| 分区 | 用途 | 谁需要看 |
|---|---|---|
| `docs/` | 安装、维护与目录导航 | 使用者、维护者 |
| `examples/` | 视频封面、示例提示词与历史测试对话 | 看效果、做测试的人 |
| `SKILL.md` + `references/` | 执行流程、确认关口、爆发机制与运镜要求 | Codex、修改规则的人 |
| `assets/` | 原始母版与中括号替换模板 | Codex、修改母版的人 |
| `agents/` | Codex 中的技能显示信息 | 维护者 |

## 使用边界

提示词中的时长、120帧、360度等是创作要求，不保证模型准确执行。历史测试包含失败与修正，结构自检也不等于生成效果验证。

当前未授予额外开源许可证；公开可访问不等于任意再分发或商业授权。
