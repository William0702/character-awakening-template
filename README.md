# 角色觉醒与法相模板

从初始角色图制作15秒四段变身与法相提示词。

- 有方向：直接深化觉醒设定与字段替换表。
- 无方向：五个不同方向＋“都不满意”，持续迭代。
- 用户确认详细设定与机制运镜卡片后，输出完整母版提示词。
- 前置设计角色变身、生长重构、瞬间压场、摄影机速度、光照与法相规模。
- 不自动调用图片、视频或付费生成服务。

## 生成直出预览

点击封面观看或下载原始MP4；视频存放在Release，拉取技能不下载视频。

| 渊潮魇王 | 缝身蛛后 |
|---|---|
| [![渊潮魇王](examples/abyss-tide/poster.jpg)](https://github.com/William0702/character-awakening-template/releases/download/v1.2.1/abyss-tide.mp4) | [![缝身蛛后](examples/stitched-spider/poster.jpg)](https://github.com/William0702/character-awakening-template/releases/download/v1.2.1/stitched-spider.mp4) |
| [配套提示词](examples/abyss-tide/prompt.md) | [配套提示词](examples/stitched-spider/prompt.md) |

[查看示例说明](examples/README.md)。示例不保证每次生成相同效果，初始参考图及完整模型设置尚未收录。

## 对话参考与测试

[查看19轮脱敏实测对话](examples/conversations/conversation-reference.md) · [复制多轮测试模板](examples/conversations/test-template.md) · [查看观察与已知问题](examples/conversations/observations.md)

覆盖方向换新、恐怖转向、设定确认、角色重启、场景联动修改和母版收紧。保留真实失败与中断，不作为全部通过的测试报告；原图附件和私人路径未公开。

## 安装

需要 Git。以下以 Windows PowerShell 为例；自定义 CODEX_HOME 的用户将目录改为自己的 skills 目录。

```powershell
git clone https://github.com/William0702/character-awakening-template.git "$env:USERPROFILE\.codex\skills\character-awakening-template"
```

如果目标目录已存在，请先自行备份并移走旧目录，勿强制覆盖。安装后在新聊天中使用：

```text
使用 $character-awakening-template，这是我的初始角色，我没有具体方向。
```

也可提供明确方向，直接进入详细设定。技能可自动匹配相关任务。

## 获取更新

```powershell
git -C "$env:USERPROFILE\.codex\skills\character-awakening-template" pull --ff-only
```

main 是最新已发布内容。这是手动同步，不会在后台自动更新。使用快进拉取，不覆盖本地修改；遇到冲突先备份并处理差异，勿用强制重置。
更新后建议在新聊天中使用，已经加载旧内容的聊天可能需要重新读取技能。

查看本地版本及更新内容：
```powershell
Get-Content "$env:USERPROFILE\.codex\skills\character-awakening-template\VERSION"
git -C "$env:USERPROFILE\.codex\skills\character-awakening-template" log -5 --oneline
```

## 使用固定版本

在技能目录中运行：
```text
git fetch --tags
git switch --detach v1.2.0
```

恢复追踪最新：
```text
git switch main
git pull --ff-only
```

## 维护与发布

维护源是本仓库，不依赖独立视频项目。编辑 SKILL.md 或对应 references；不将具体角色生产状态写进通用规则。

1. 修改内容，检查母版保留和工作流确认关口。
2. 更新 VERSION 与 CHANGELOG.md。
3. 执行技能结构校验（可用 Codex skill-creator 的 quick_validate.py），并人工审阅实际交付行为。
4. 提交并推送 main，用户下次 pull 获取更新。
5. 重要版本创建对应 Git 标签及 Release。

```text
git status --short
git add <明确需要发布的文件>
git commit -m "Describe the change"
git push origin main
git tag vX.Y.Z
git push origin vX.Y.Z
```

版本策略：修复与说明用补丁号，兼容的功能增强用次版本，工作流或母版不兼容变化用主版本。不要将示例标签原样运行。

## 目录

- SKILL.md：技能入口。
- assets/master-original.txt：原始母版。
- assets/master-template.md：中括号替换模板。
- references/workflow.md：两条完整制作路径。
- references/setting-contract.md：详细觉醒设定。
- references/impact-contract.md：爆发机制对照。
- references/mechanism-camera-contract.md：六类机制及运镜前置设计。
- agents/openai.yaml：显示信息。

## 边界

提示词时间是节奏预算，“120帧”“360度”等描述不保证模型执行。结构校验不等于生成效果验证。
公开仓库包含技能文本、提示词及预览封面，Release另含用户授权的示例视频；使用者应自行确保输入素材和输出用途适当。当前未授予额外开源许可证，公开可访问不等于授予任意再分发或商业授权。
