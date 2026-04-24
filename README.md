# xifeng-style-writer

一个用于 Claude Code 的 Skill，完整复现"西风 / 记忆承载"的思想系统、判断顺序和写作风格。

## 它是什么

这不是一个简单的"文风模仿器"。

它的目标是让 AI 以西风本人的状态出场——不只是句子像，而是思想方式、判断顺序、说话口吻、文字节奏四层一致。

## 支持四种模式

| 模式 | 用途 |
|------|------|
| `thinking-mode` | 用西风的方式拆问题、下判断、看趋势、做选择 |
| `diagnosis-mode` | 诊断一件事的真实结构、误判来源、风险位置 |
| `writing-mode` | 用西风式认知骨架写文章 |
| `hybrid-mode` | 在西风骨架上混入专业承接，适合既传播又转化的内容 |

## 核心原则

- 先拆表层叙事，再找底层结构，再看位置和利益，再判断旧答案是否失效，最后才讨论个人应对
- 不是先表态，而是先拆局
- 不是先追求最优，而是先避免出局
- 不提供廉价安慰，不制造无用焦虑

## 项目结构

```
xifeng-style-writer/
├── SKILL.md                          # Skill 主定义文件
├── README.md                         # 本文件
└── references/                       # 参考文档
    ├── author-persona.md             # 作者人格卡——角色、视角、基调、判断习惯
    ├── worldview.md                  # 世界观——结构剧而非道德剧，稳定是例外
    ├── judgment-sequence.md          # 判断顺序——八步判断法、三层翻译法
    ├── life-strategy.md              # 人生策略——先保命再升级，迷恋能力而非稳定
    ├── writing-sop.md                # 写作 SOP——起稿、结构、改稿、风格诊断
    ├── style-map.md                  # 风格地图——标题、骨架、句法、论证引擎
    ├── taboo-list.md                 # 禁忌清单——常见误区和结构性/语言性/认知性禁忌
    ├── prompt-templates.md           # 提示词模板——17 种即用型调用模板
    └── training-guide.md             # 训练指南——如何内化这套思想系统
```

## 使用方式

在 Claude Code 中调用 `西风` 或 `记忆承载` 相关指令即可激活此 Skill。具体调用方式参见 `SKILL.md`。

## 参考文档说明

- 需要校准世界观和风险观 → 读 `worldview.md`
- 需要按西风方式拆问题 → 读 `judgment-sequence.md`
- 话题涉及人生选择和生存策略 → 读 `life-strategy.md`
- 需要把判断落成文章 → 读 `writing-sop.md`
- 需要加强标题感和节奏感 → 读 `style-map.md`
- 需要校准说话姿态和人格基调 → 读 `author-persona.md`
- 完成后做反向排错 → 读 `taboo-list.md`
- 用户要即用型模板 → 读 `prompt-templates.md`
- 用户想内化这套思想 → 读 `training-guide.md`
