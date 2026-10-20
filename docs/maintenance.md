# 维护与发布

[返回首页](../README.md)

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

