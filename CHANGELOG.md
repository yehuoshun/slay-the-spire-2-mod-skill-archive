# Changelog

## [2026-10-04]

### Added
- `references/multiplayer/multiplayer-netactions.md` — 网络行动（GameAction/INetAction 骨架、GameActionType 语义、PlayPhase 门控、IsPlayerReadyToEndTurn、执行失败 rethrow、模型状态防护）
- `references/harmony/harmony-transpiler.md` — Transpiler 泛型 operand 结构判定 + 自定义 comparer 相等返 0 保确定性

### Changed
- `references/resource/resource-lifecycle.md` — 补自定义图标预加载（Patch `PreloadManager.GetRunAssetPaths`）
- `references/settings/settings-core.md` — 补延迟注册需等 `LocManager.Instance` 就绪
- `references/multiplayer/multiplayer.md`/`multiplayer-core.md`/`harmony.md`/`index.md` — 导航与索引同步
- 主仓库同步：48d90fe（学 YuWanCard 2026-10-04 增量）
- README 参考资料表补 2 行（harmony-transpiler / multiplayer-netactions）

## [2026-10-02]

### Changed
- **同步策略定案**：archive 只同步 `references/` 文件夹，references 以外（SKILL.md/LEARN.md/LEARNED.md/README.md）一律不跟主仓库（本地副本冻结）

### Added
- **v4 归档（第四代）**：补齐 9-10 月断档的版本留档 — 23 个模块统一推进到 v4（当前版快照；reward 与 v1 无差异保持不动），multiplayer 首次入档
- 影响模块：baselib, card, energy, harmony, multiplayer, pile, resource, rest-site, serialization, settings, setup（新生成）+ act, badge, character, enchantment, event, modifier, monster, orb, pet, potion, power, relic（v3 后演进定格）
- 主仓库同步：89ed2ed（全量 md 体检修复 4 处）

### Changed
- README 参考资料表全面更新：settings 改纯原生表述（ConfigFile + NSubmenu UI）、新增 multiplayer 行、setup 补全至 17 个文件、serialization 补自动注册框架

## [2026-09-19]

### Added
- `references/card/card-variables.md` — 新增 card-variables（卡牌自定义动态变量）
- 主仓库结构同步：各模块根目录放置当前版本文件

### Changed
- 重构 archive 目录结构：旧版本从 `module-v1.md` 改为 `v1/module.md` 目录式管理
- 影响模块：act, baselib, card, character, enchantment, event, harmony, modifier, monster, orb, pet, potion, power, relic, serialization, setup

### Removed
- 移除临时快照目录 `snapshot-2026-09-19/`

## [2026-08-28]

### Added
- 初始化归档：旧版参考文档（v1/v2/v3）迁移至此仓库
- 预置 `patterns/`、`settings/` 目录占位