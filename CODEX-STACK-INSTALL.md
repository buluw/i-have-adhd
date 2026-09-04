# 给其他 Codex 的安装指令

将下面整段作为一个任务发送给目标 Codex：

```text
请直接操作当前电脑，为当前用户安装下面这套 Codex 组合，不要只给方案。

目标组件：
1. i-have-adhd-codex：从 buluw/i-have-adhd 的 codex-personal 分支安装。
2. stop-that-shit：安装完整 Codex 插件，固定版本 0.2.0。
3. ponytail-review：只安装独立 Skill，固定版本 v4.9.0。
4. ponytail-audit：只安装独立 Skill，固定版本 v4.9.0。

边界：
- 不安装 simplify-codebase。
- 不安装完整 Ponytail 插件或 Ponytail 主 Skill。
- 不 fork、不合并这些项目，不创建新的超级插件。
- 已有正确安装就复用；只有版本或来源不正确时才更新。
- 权限不足时请求必要授权，不要改用浏览器或 GUI 绕路。

执行：
1. 检查 codex plugin list 和 codex plugin marketplace list。
2. 安装个人 ADHD 插件：
   codex plugin marketplace add buluw/i-have-adhd --ref codex-personal
   codex plugin add i-have-adhd-codex@i-have-adhd-codex
3. 安装 Stop That Shit：
   codex plugin marketplace add lennney/stop-that-shit --ref 0.2.0
   codex plugin add stop-that-shit@stop-that-shit
4. 使用内置 skill-installer，从 DietrichGebert/ponytail 的 v4.9.0 安装：
   - skills/ponytail-review
   - skills/ponytail-audit
5. 做一次最小验证：
   - 两个插件处于 installed, enabled。
   - ADHD marketplace 指向 buluw/i-have-adhd.git 的 codex-personal 分支。
   - stop-that-shit 版本是 0.2.0，并包含 UserPromptSubmit 和 PreToolUse Hook。
   - ponytail-review 与 ponytail-audit 的 SKILL.md 能加载，名称正确。

完成后立即停止。告诉用户重新启动 Codex；在新任务中运行 /hooks，检查并信任 stop-that-shit 的 UserPromptSubmit 和 PreToolUse Hook。
```

来源固定为：

- [i-have-adhd-codex / codex-personal](https://github.com/buluw/i-have-adhd/tree/codex-personal)
- [stop-that-shit / 0.2.0](https://github.com/lennney/stop-that-shit/tree/0.2.0)
- [ponytail / v4.9.0](https://github.com/DietrichGebert/ponytail/tree/v4.9.0)
