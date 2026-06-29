# 安装 / 使用

这套工作台有三种用法，挑适合你的。

## 方式零：一行命令装进 Agent（最快，推荐用 Claude Code / Codex / Cursor 等）

```bash
npx skills add baozangtuan77/baozangtuan77-blogger-workstation
```

借助 [`skills` CLI](https://github.com/vercel-labs/skills)（支持 70+ 个 agent），它会自动把 skill 装进你 agent 的 skills 目录，不用你管路径。默认装到项目级，想全局可用加 `-g`，跳过确认加 `-y`。

**装完必做一步**：进 skill 目录 `cp config.example.yaml config.yaml`，填好《我的账号档案》——`npx skills add` 不会替你做这步。

> 想手动控制路径、或 agent 不在 `skills` CLI 支持列表里 → 看下面「方式二」。

## 方式一：直接粘进对话 AI（最简单，给博主）

不用装任何东西，豆包 / Claude / 任意对话 AI 都行：

1. 打开 `config.example.yaml`，照着填好你的《我的账号档案》（不会填看 `examples/` 里的母婴 / 家居示范），存到手机备忘录。
2. 想做某件事，去 `capabilities/` 找对应能力（不确定用哪个？看 `SKILL.md` 里的"能力路由"对症表）。
3. **把你的《账号档案》+ 那个能力的内容 + 你的素材，一起发给 AI。**
4. 用完把好东西用「素材沉淀」存进你自己的库。

## 方式二：装成 AI Agent 的 skill（Claude Code / WorkBuddy / Cursor 等）

> ⚠️ **关键：每个 agent 产品读 skills 的目录不一样，没有统一位置。** 装错目录 = agent 根本找不到这个 skill。所以别照搬别人的路径，按下面三步走。

**第 1 步 · 先 clone 到一个固定位置**（别直接 clone 进某个 agent 的目录，方便给多个 agent 共用）：
```bash
git clone https://github.com/baozangtuan77/baozangtuan77-blogger-workstation ~/skills/baozangtuan77-blogger-workstation
```

**第 2 步 · 放进你那个 agent 的 skills 目录**。常见位置如下（**以你 agent 自己的文档为准**，不确定就在它的设置/文档里搜"skills""自定义技能"）：

| Agent | skills 目录 |
|---|---|
| Claude Code | `~/.claude/skills/`（部分配置也认 `~/.agents/skills/`）|
| WorkBuddy | `~/.workbuddy/skills/` |
| 其他（Cursor / Cline…）| 查该产品文档里的 skills 目录 |

把第 1 步的文件夹**复制或软链**进去。软链最省事（clone 一份，多个 agent 共用，一处更新处处生效）：
```bash
# 例：装进 WorkBuddy
ln -s ~/skills/baozangtuan77-blogger-workstation ~/.workbuddy/skills/baozangtuan77-blogger-workstation
```

**第 3 步 · 重启 agent**（skills 在会话启动时加载，装完必须**重启或开个新会话**才会被识别）。

装好后直接说"帮我想选题""这条脚本帮我改活人感""帮我拆下我账号的商业定位"，它读 `SKILL.md` 自动路由到对应能力。第一次先填好 `config.example.yaml` 的《账号档案》。需要抓笔记/账号数据时可接 TikHub API（⚠️ 收费、需自己 key），不接就手动贴。

## 想要更强的？

这套是轻量开源版（方法 + 脚手架）。想要**带你真实后台数据**的深度诊断、全量方法论、个性化 → 七七的 **博主AI加速器**；卡在**商业方向**上 → 七七 **1v1**。
