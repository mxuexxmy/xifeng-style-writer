# xifeng-style-writer

一个自包含的 Agent Skill：完整复现「西风 / 记忆承载」的思想系统、判断顺序和写作风格。

## 安装（推荐）

兼容 [Skills CLI](https://skills.sh/) 支持的各类 Agent（Claude Code、Cursor、Codex、OpenCode、Copilot 等 70+），不局限于某一家。

```bash
# 全局安装：自动装到本机已检测到的 Agent
npx skills add mxuexxmy/xifeng-style-writer -g -y

# 装到本机所有支持的 Agent
npx skills add mxuexxmy/xifeng-style-writer -g --agent '*' -y
```

常用变体：

```bash
# 先看仓库里有哪些 skill
npx skills add mxuexxmy/xifeng-style-writer --list

# 指定若干 Agent（可多选）
npx skills add mxuexxmy/xifeng-style-writer -g -a claude-code -a cursor -a codex -y

# 只装到当前项目（不写 -g）
npx skills add mxuexxmy/xifeng-style-writer -y
```

安装后，在对应 Agent 的对话里提到 `西风`、`记忆承载`，或说「用西风的方式分析 / 写一篇」，即可触发。

本 skill **自包含**：只需 `SKILL.md` 与 `references/`，不依赖任何人的 Obsidian、原文库或其他本地资料目录。

## 它是什么

这不是一个简单的「文风模仿器」。

目标是让 AI 以西风本人的状态出场——不只是句子像，而是思想方式、判断顺序、说话口吻、文字节奏四层一致。

## 支持四种模式

| 模式 | 用途 |
|------|------|
| `thinking-mode` | 用西风的方式拆问题、下判断、看趋势、做选择 |
| `diagnosis-mode` | 诊断一件事的真实结构、误判来源、风险位置 |
| `writing-mode` | 用西风式认知骨架写文章 |
| `hybrid-mode` | 西风骨架 + 传播入口与专业承接，适合既传播又转化；旧称「Link x 西风」按此模式处理 |

## 核心原则

- 先拆表层叙事，再找底层结构，再看位置和利益，再判断旧答案是否失效，最后才讨论个人应对
- 落到个人时，先问「我有什么、我要什么、我愿意放弃什么」
- 不是先表态，而是先拆局
- 不是先追求最优，而是先避免出局
- 不提供廉价安慰，不制造无用焦虑

## 输出约定

写作类模式默认在对话里输出完整稿（标题、正文、备用标题），不自动落盘；只有你明确指定保存路径时，才会写成 Markdown 文件。

## 项目结构

```
xifeng-style-writer/
├── SKILL.md                          # Skill 主定义文件
├── README.md                         # 本文件
└── references/                       # 参考文档
    ├── author-persona.md             # 作者人格卡——角色、视角、基调、判断习惯
    ├── worldview.md                  # 世界观——结构剧而非道德剧，稳定是例外
    ├── judgment-sequence.md          # 判断顺序——八步判断法、三层翻译法、个人决策三问
    ├── life-strategy.md              # 人生策略——先保命再升级，迷恋能力而非稳定
    ├── writing-sop.md                # 写作 SOP——起稿、结构、改稿、输出
    ├── hybrid-mode.md                # 折中模式——传播入口 + 专业承接（自包含）
    ├── style-map.md                  # 风格地图——标题、骨架、句法、论证引擎
    ├── examples.md                   # 标注样稿——正例与偏味对照
    ├── taboo-list.md                 # 禁忌清单——常见误区和结构性/语言性/认知性禁忌
    ├── prompt-templates.md           # 提示词模板——17 种即用型调用模板
    └── training-guide.md             # 训练指南——如何内化这套思想系统
```

## 参考文档说明

- 需要校准世界观和风险观 → 读 `worldview.md`
- 需要按西风方式拆问题 → 读 `judgment-sequence.md`
- 话题涉及人生选择和生存策略 → 读 `life-strategy.md`
- 需要把判断落成文章 → 读 `writing-sop.md`
- 需要传播+专业承接（hybrid） → 读 `hybrid-mode.md`
- 需要加强标题感和节奏感 → 读 `style-map.md`
- 需要正例/偏味对照 → 读 `examples.md`
- 需要校准说话姿态和人格基调 → 读 `author-persona.md`
- 完成后做反向排错 → 读 `taboo-list.md`
- 用户要即用型模板 → 读 `prompt-templates.md`
- 用户想内化这套思想 → 读 `training-guide.md`

## 手动安装

若不用 Skills CLI，把本仓库复制到对应 Agent 的 skills 目录即可。目录名保持 `xifeng-style-writer`，常见位置例如：

| Agent | 全局目录（示例） |
|-------|------------------|
| Claude Code | `~/.claude/skills/xifeng-style-writer/` |
| Cursor | `~/.cursor/skills/xifeng-style-writer/` 或 `~/.agents/skills/xifeng-style-writer/` |
| Codex | `~/.codex/skills/xifeng-style-writer/` |
| OpenCode / 通用 | `~/.config/agents/skills/xifeng-style-writer/` 或项目内 `.agents/skills/xifeng-style-writer/` |

完整 Agent 列表与路径以 [skills.sh](https://skills.sh/) / Skills CLI 文档为准。
