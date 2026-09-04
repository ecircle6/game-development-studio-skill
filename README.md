# Game Development Studio Skill（游戏开发工作室技能包）

一个可复用的**游戏开发方法论技能包**：把"多角色游戏开发团队"的组织方式、七阶段标准流程、质量门制度与交付物标准，抽象为一份 AI 可执行的通用规则。**不绑定任何具体题材、引擎或项目内容**——同一套规则可用于手游、独立游戏、网页小游戏等任意游戏项目。

## 这是什么

本技能包源自一套经过实际项目验证的"游戏开发工作室"专家团队工作法，其核心是两条：

1. **编排与建造分离**：主理人（Orchestrator）只负责诊断阶段、路由任务、把守质量门、汇编产出；专业工作（策划/程序/美术/音频/测试/发布）由六大角色分工完成，专业判断以角色结论为准。
2. **流程与标准先于灵感**：七阶段 SOP + 阶段间质量门（PASS/CONCERNS/FAIL）+ 标准化交付物结构，让"产出可直接落地、跨角色产出可互相校验"。

## 目录结构

```
game-development-studio-skill/
├── README.md                          ← 本说明文档
└── game-development-studio/           ← 技能包本体（标准 Skill 结构）
    ├── SKILL.md                       ← 主技能文件（触发条件、铁律、流程概览、使用方法）
    ├── references/
    │   ├── roles.md                   ← 六角色定义 + 派发 prompt 七要素模板
    │   ├── workflow.md                ← 七阶段 SOP（目标/输入/输出/切换条件）
    │   ├── quality-gates.md           ← 质量门制度与评审输出模板
    │   └── deliverable-standards.md   ← 交付物标准结构 + 设计哲学
    └── examples/
        └── usage-examples.md          ← 三个典型场景走查 + 反模式清单
```

## 六大角色

| 角色 ID | 职责域 |
|---|---|
| `design-strategist` | 创意方向、游戏策划、系统/关卡/经济设计、叙事、UX |
| `engineering-lead` | 技术方向、架构与 ADR、玩法实现、性能、DevOps |
| `art-director` | 美术方向、美术圣经、资产规格、技术美术、可访问性 |
| `audio-director` | 音乐基调、音效设计、混音、音频实现策略 |
| `quality-lead` | 测试策略、烟雾测试、回归、Bug 分级、Playtest |
| `release-ops-lead` | 发布管理、构建/版本、本地化、Live Ops、回滚 |

主理人（编排者）不属于派发角色，其职责见 `SKILL.md` 协作铁律。

## 安装

**方式 A · WorkBuddy 用户级技能（推荐）**

将 `game-development-studio/` 整个目录复制到：

```
~/.workbuddy/skills/game-development-studio/
```

重启 WorkBuddy 后，在对话中提到"做游戏 / 立项 / GDD / 美术圣经 / 发布清单"等即可触发。

**方式 B · 项目级技能（团队共享）**

复制到项目内的 `.workbuddy/skills/game-development-studio/`。

## 快速上手

- **完整立项**：直接说"我想做一款×××游戏，用工作室流程帮我从头推进"。
- **单点问题**：说"帮我设计一个×××系统 / 帮我做测试策略"，会按关键词路由到单一角色，不走全流程。
- **半路接手**：说"接手一个已有代码的游戏项目"，会先做阶段诊断再补文档。

更多场景见 `game-development-studio/examples/usage-examples.md`。

## 自定义指南

| 想改什么 | 改哪里 |
|---|---|
| 角色、职责边界 | `references/roles.md` |
| 阶段顺序、并行策略 | `references/workflow.md` |
| 质量门松紧、评审模板 | `references/quality-gates.md` |
| 文档结构标准、设计哲学 | `references/deliverable-standards.md` |
| 触发时机与描述 | `game-development-studio/SKILL.md` 的 YAML frontmatter |

## 安全说明

本技能包为**纯 Markdown 方法论**：不含可执行脚本、无网络调用、无外部依赖，不收集任何数据。所有协作行为（写文件、提交代码、发布）均要求先获得用户确认。

## License

MIT
