# Slay the Spire 2 Mod 开发 Skill（archive）

> 杀戮尖塔 2 纯原生 Mod 开发，零第三方依赖。

> ⚠️ 本仓库是主仓库 [yehuoshun/slay-the-spire-2-mod-skill](https://github.com/yehuoshun/slay-the-spire-2-mod-skill) 的**备份镜像**：`references/` 与 `SKILL.md` 由同步流程自动更新，README 为人工维护的定制存档说明（不随主仓库同步）。首次使用请以主仓库为准。

---

## 目录

| 文件 | 说明 |
|------|------|
| [SKILL.md](SKILL.md) | AI 工作流 + 硬规则（与主仓库同步） |
| [LEARN.md](LEARN.md) | 学习流程 + 备份同步流程（本仓库副本，不随主仓库更新） |
| [LEARNED.md](LEARNED.md) | 已学仓库登记，防重复学习（本仓库副本，不随主仓库更新） |
| [references/](references/) | 知识文档（与主仓库同步），见下方模块索引 |

## references 模块索引

> 📌 每个模块的 `xx.md` 为**导航页**（概述 + 常见问题 + 章节导航表），正文按章节拆分在 `xx-*.md`。读模块先开导航页，再按需读子文件。`setup/` 无独立导航页，入口见环境与工程小节。

### 环境与工程

| 模块 | 入口 |
|------|------|
| setup（环境/骨架/构建/CI/loader） | [environment-setup.md](references/setup/environment-setup.md)（全文件平级，见该目录） |

### 内容模块（导航页入口）

| 模块 | 导航页 |
|------|--------|
| relic 遗物 | [relic.md](references/relic/relic.md) |
| card 卡牌 | [card.md](references/card/card.md) |
| potion 药水 | [potion.md](references/potion/potion.md) |
| enchantment 附魔 | [enchantment.md](references/enchantment/enchantment.md) |
| event 事件 | [event.md](references/event/event.md) |
| power 能力 | [power.md](references/power/power.md) |
| character 角色 | [character.md](references/character/character.md) |
| monster 敌怪 & 遭遇 | [monster.md](references/monster/monster.md) |
| modifier 修改器 | [modifier.md](references/modifier/modifier.md) |
| orb 球体 | [orb.md](references/orb/orb.md) |
| act 章节 | [act.md](references/act/act.md) |
| pet 宠物 | [pet.md](references/pet/pet.md) |
| resource 自定义资源 | [resource.md](references/resource/resource.md) |
| badge 徽章 | [badge.md](references/badge/badge.md) |
| rest-site 休息点 | [rest-site.md](references/rest-site/rest-site.md) |
| pile 牌堆 | [pile.md](references/pile/pile.md) |
| reward 奖励 | [reward.md](references/reward/reward.md) |
| energy 能量 | [energy.md](references/energy/energy.md) |

### 横切能力

| 模块 | 导航页 |
|------|--------|
| harmony 补丁 | [harmony.md](references/harmony/harmony.md) |
| serialization 序列化与注册 | [serialization.md](references/serialization/serialization.md) |
| settings 设置界面 | [settings.md](references/settings/settings.md)（+ [modconfig.md](references/settings/modconfig.md)） |
| baselib 纯原生设计模式 | [design-patterns.md](references/baselib/design-patterns.md) |
| multiplayer 多人模式 | [multiplayer.md](references/multiplayer/multiplayer.md) |
| overlay 游戏内覆写 | [overlay.md](references/overlay/overlay.md) |
| ui 手牌/战斗 UI | [ui.md](references/ui/ui.md) |
| run Run 生命周期 | [run.md](references/run/run.md) |

---

## 设计原则

1. **硬规则驱动**：所有行为由硬规则约束，不靠"建议"
2. **知识注入**：代码模板和 API 参考在 references 中持续积累
3. **真编译验证闭环**：文档（唯一创作源）→ [sts2-mod-examples](https://github.com/yehuoshun/sts2-mod-examples) 可编译示例 → CI 真编译（dotnet build + API 白名单 + 本地化校验）→ 报错回流修文档；本仓库为**文档型**（无 C# 代码），编译验证走示例仓库 CI，agent 负责静态检查 + push
4. **零第三方依赖**：只靠 `0Harmony.dll` + `sts2.dll`

## 版本归档

> `references/<模块>/v1/`-`v4/` 是旧版本留档（只读，**不要动**）；当前版直接放在 `references/<模块>/` 根目录。大改前先留档（当前版复制为 `v<N+1>`）再同步新内容。

---

## 鸣谢

### 活跃仓库

- [Alchyr/BaseLib-StS2](https://github.com/Alchyr/BaseLib-StS2) — 官方模组标准库（Custom*Model 基类、[Pool]、Builder、工具）
- [Alchyr/ModTemplate-StS2](https://github.com/Alchyr/ModTemplate-StS2) — 官方模组脚手架模板（工程化思想：骨架自动化、路径检测、目录规范）
- [YuWan886/Sts2-YuWanCard](https://github.com/YuWan886/Sts2-YuWanCard) — 实战大型 mod（真实 API 用法样本：多人、自定义稀有度、多版本 loader、生命条预测）
- [lf201014/STS2_MarisaMod](https://github.com/lf201014/STS2_MarisaMod) — 实战角色 mod（增幅卡系统、动画状态机、角色资源覆写、AsyncLocal 异步 Patch）
- [s1f102500012/sts2mod](https://github.com/s1f102500012/sts2mod) — 多聚合 mod 合集（15 项全学：overlay/角色/附魔/符文/Run 生命周期/UI/补丁框架 等）
- [s1f102500012/HextechRunes](https://github.com/s1f102500012/HextechRunes) — 海克斯符文独立仓库（9 万行级巨型 mod 工程模式）

### 项目仓库

- [yehuoshun/slay-the-spire-2-mod-skill](https://github.com/yehuoshun/slay-the-spire-2-mod-skill) — 主仓库（唯一创作源）
- [yehuoshun/sts2-mod-examples](https://github.com/yehuoshun/sts2-mod-examples) — 可编译示例仓库（CI 验证闭环）

### 不活跃仓库

- [烟汐忆梦_YM](https://space.bilibili.com/481430814) — 9 篇入门教程（见 LEARNED.md 清单）