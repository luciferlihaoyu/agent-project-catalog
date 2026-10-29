# macro-inc/macro

> 仓库：https://github.com/macro-inc/macro · ⭐ 5,418（2026-10-29 API 实测） · Rust · License: AGPL-3.0 · 官网 https://macro.com

**一句话：** 团队工作软件的「重做尝试」—— 把 email + messages + docs + tasks + agents + calls + CRM 统一进一个界面，所有对象用 @link 双向图谱互连、共享团队级记忆，Rust + SolidJS 写的团队「操作系统」。

## 关键数据（2026-10-29 API 实测）

| 项 | 值 |
|---|---|
| ⭐ Stars | 5,418（今日 +117） |
| 🍴 Forks | 518（fork 率 9.6%） |
| 语言 / 协议 | Rust / AGPL-3.0 |
| Open Issues | 340（对 5.4 千星 = 6.3%，偏高） |
| 创建 / 最后推送 | 2025-11-08 / 2026-10-29 |
| Topics | agent, ai, ai-agents, all-in-one, crm, crm-system, email, linear |
| 收录 | GitHub Trending 每日精选 2026-10-29（+117/日） |

## 核心能力

- **Blocks 拼装式架构**：Email / Messages / Tasks / Docs / Canvas / Agents / Calls / File storage / Pull requests / CRM —— 每个 block 有专用界面但共用同一后端。
- **双向图谱**：文档↔任务、频道消息↔邮件、CRM 记录↔讨论，跨引用原生存成 bidirectional graph，所有对象 @link 互通、全局可搜。
- **团队级共享记忆 + Agents**：Agents block 提供 unified team-level memory，可代人行动。
- **邮件优先的 CRM**：多 Google 账号统一收件箱、键盘优先（`j`/`k`/`e` 导航）、按联系人/公司聚合邮件、附件 PDF 解析后统一索引供 agent 直接检索。
- **CRDT 实时协作文档**（markdown-native）、Canvas 2D 白板嵌 @link、GitHub PR 与任务互链。

## 为什么值得关注

- **立论击中了一个被默认忽略的真痛点**：作者原话是用了 Slack / Linear / Notion / HubSpot / Superhuman 一堆好产品，但「公司不是可计算的，是被 MCP 和 Zapier 缝起来的」—— **缝合层本身就是复杂度税**。
- **技术选型反直觉地硬核**：Rust 后端 + SolidJS 前端，不是 Electron 也不是 Next.js；15 人团队 dogfood 两年，目标明写「for speed and reliability」。
- **把「应用间集成」问题变成「单库内建图」问题** —— 若真做到统一，Zapier/MCP 缝合层可以真正消失。这是图数据库式工作空间第一次出现在 Trending 上。
- **与本库已收录的 `twentyhq/twenty`（开源 CRM）、`coollabsio/coolify`（自托管 PaaS）** 同属「团队工作平台 / 后端底座」赛道；与 `stablyai/orca`、`nightly-labs/openbot` 的差异在于 —— **那两者是「多个 agent 的宿主」，macro 是「整个公司工作面的宿主」**。

## ⚠️ 局限

- **AGPL-3.0**：团队工作软件选 AGPL，商业化路径比 MIT 窄得多。
- **340 个 open issues 对 5.4 千星（6.3%）偏高**，对一个宣称「两年 dogfood 的成熟产品」说明边界情况不少。
- **全家桶的复杂度悖论**：10 个 block 每块都要做 Email/Messages/Tasks/Docs/CRM 全套，任何一块都不如专门的 Slack/Notion/HubSpot 成熟 —— **「不切换工具」的收益是否盖得住「每样都差一截」的代价**，是这个模式的核心问号。
- 官网已有 demo 预约与招聘页，说明是产品导向而非玩具 —— **它可能直接变成商业产品而不是社区项目**。

## 参考

1. [GitHub 仓库](https://github.com/macro-inc/macro)
2. [官网 macro.com](https://macro.com)
3. [官方文档 docs.macro.com](https://docs.macro.com)
