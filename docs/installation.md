# 安装、使用与更新

[返回首页](../README.md)

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

