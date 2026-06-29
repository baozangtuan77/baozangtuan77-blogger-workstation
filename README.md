# 博主AI工作台 · blogger-ai-workstation

[![install](https://img.shields.io/badge/install-npx_skills_add-black?logo=npm&logoColor=white)](https://github.com/baozangtuan77/baozangtuan77-blogger-workstation) [![agents](https://img.shields.io/badge/agents-Claude_Code_·_Codex_·_Cursor_·_70%2B-6E56CF)](https://github.com/vercel-labs/skills) [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

> 一套给小红书内容创作者（尤其母婴 / 家居博主）的 AI 内容工作台：选题、写稿、拆片、复盘、商单、定位诊断——**13 个能力**，每个都内置"懂品牌投放 + 带过几百个博主"的操盘手判断力。
>
> 作者：**宝藏团七七**（GitHub [@baozangtuan77](https://github.com/baozangtuan77)）

## 它解决什么

普通 AI 给你"正确的废话"，因为它不懂"什么内容能涨粉、什么内容品牌愿意付费"。这套工作台把这套判断力写进了 prompt——它**问对问题、给可直接用的话、守住"不编 / 不糊弄"的底线**，而不是泛泛而谈。

## 谁用 · 怎么用

- **你是博主（最常见）**：填一次《我的账号档案》（见 `config.example.yaml`），用某个能力时，把档案 + 你的素材一起发给 AI（豆包 / Claude / 任意对话 AI）。
- **你用 Claude Code / Codex / Cursor 等 Agent**：一行命令装好（见下），直接说你要干嘛，它读 `SKILL.md` 自动路由到对应能力。

## 安装（一行，支持 70+ 个 Agent）

```bash
npx skills add baozangtuan77/baozangtuan77-blogger-workstation
```

借助 [`skills` CLI](https://github.com/vercel-labs/skills)（Claude Code / Codex / Cursor / Cline / Gemini / Copilot / Windsurf 等都支持），它会自动装进你 Agent 的 skills 目录。默认装到项目级，想全局可用加 `-g`。

> 装完记得 **填配置**：进 skill 目录 `cp config.example.yaml config.yaml`，照着填好《我的账号档案》（不会填看 `examples/` 里的母婴 / 家居示范）。
>
> 不想用 CLI？手动安装（clone + 软链）和"直接粘进对话 AI"两种方式见 [`INSTALL.md`](./INSTALL.md)。

## 13 个能力

| 模块 | 能力 |
|---|---|
| 选题 | 爆款选题分析 · 批量生成选题 · 竞品账号拆解 |
| 写稿编导 | 短视频脚本编导 · 活人感改稿 · 封面标题优化 · 商单脚本 · 直播转短视频 |
| 拆解诊断 | 爆款视频拆解 · 内容数据复盘 |
| 商业定位诊断 | 商业定位诊断 |
| 运营沉淀 | 素材沉淀 · 日程规划 |

> 默认示范用母婴 / 家居赛道，**任意赛道都能用**——换掉《账号档案》里的赛道就行。

## 它做得到 / 做不到（诚实）

- ✅ 给你方法、脚手架、可直接用的产出——解决日常内容创作 60-80%。
- ❌ 它没有你的真实后台数据，也不替你拍板商业方向：
  - 想要带**你真实数据**的深度版 + 全量方法论 + 个性化诊断 → 七七的 **博主AI加速器**。
  - 卡在**方向**（要不要转赛道 / 怎么变现）这种 AI 给不了的判断 → 七七 **1v1 卡点突破**。

## 关于七七

4 年小红书内容营销操盘手，一边花着千万级预算帮品牌选博主投放，一边带出 300+ 博主。这套工作台是她把"双视角操盘手判断力"开源出来的轻量版。

- 小红书 **@宝藏团七七** · 公众号「**是自在的七七啊**」(AI × 创业实战) /「**七七宝藏团**」(博主孵化) · GitHub [@baozangtuan77](https://github.com/baozangtuan77)

## License

MIT © baozangtuan77（宝藏团七七）。自由使用 / 修改 / 分发，保留署名即可。
