# cloudflare/security-audit-skill

> 仓库：https://github.com/cloudflare/security-audit-skill · ⭐ 42,151（2026-10-24 API 实测） · JavaScript · License: MIT

**一句话：** A coding-agent skill for multi-phase security audits with independently verified, machine-readable findings. —— Cloudflare 官方开源的「多阶段安全审计」编码 Agent 技能：把侦察 → 覆盖驱动猎取 → 候选验证 → 结构化输出 → 独立记录复核 → 中立报告编排成一条流水线。

## 核心能力
- **六阶段审计流水线**：Reconnaissance → Coverage-led hunting → Candidate validation → Structured output → Independent record verification → Target-neutral reporting
- **覆盖台账（coverage-ledger.json）**：每个 hunter 只负责台账里分配到自己的一块，覆盖率可追溯；`validate-coverage-ledger.cjs` 零依赖校验器全程把关
- **反证优先的验证**：每个候选漏洞都交给**全新的 verifier 去尝试推翻它**，而不是去证明它成立
- **三态结论**：`confirmed`（完整源码溯源 + 有界观测结果）/ `needs_validation`（精确的未决事实、不给严重性）/ `rejected`（已被证伪）—— 用 `report-schema.json` 强制 schema 校验
- **独立记录复核**：最终源码论断由**新 agent** 独立验证；material replacement 还要再过一道独立 verifier
- **可叠加增量运行**：多次审计同一仓库是可加的，会复用历史台账定向补缺口、复验变更源码，不会把过期或未决的工作误算为已覆盖
- **19 类攻击面 hunting 文档**：内存安全 / 二进制 / 内核、AI 与 LLM（提示注入、agent/tool、输出处理）、Web 协议与认证、客户端侧、供应链与发布、云与部署（IaC、容器、serverless、ingress）、协议 RPC 与消息、资源耗尽与可用性、数据隔离与生命周期、桌面移动与本地 IPC
- **零依赖校验器 + 测试**：`validate-findings.cjs` / `validate-coverage-ledger.cjs` 及其 `.test.cjs` 测试与 producer 兼容 fixture

## 关键数据（2026-10-24 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 42,151（今日 +2,716，**全场最高**） |
| 🍴 Forks | 2,633 |
| Open Issues | 83 |
| 仓库体积 | 143 KB（**极轻，纯 prompt + 校验器**） |
| 创建时间 | 2026-06-18 |
| 最后推送 | 2026-09-14T19:29:02Z |
| 主页 | 无 |
| 协议 | MIT |

## 适用场景
- 对自有代码库做 Agent 辅助的安全审计（CI 里跑）
- 搭建内部「漏洞发现 harness」的起点
- 评估自身 Agent 系统的安全边界与提示注入风险
- 研究「如何让 Agent 的结论可审计、可复核」

## 为什么值得关注
- **它解决的是 Agent 领域最要命的一个问题：结论不可信**。目前 99% 的 AI 安全审计输出是「一堆疑似漏洞的散文」，没法进工单、没法复验、没法追责。这套 skill 的设计全部围绕**可验证性**：覆盖台账、JSON schema 三态结论、**反证优先**的 verifier、由新 agent 做的独立复核。**把「AI 说有漏洞」变成「有源码溯源、有观测边界、有独立证伪记录」**，这是从玩具走向工程的分界线。
- **「反证优先」是整套设计里最聪明的一点**。让模型去证明自己发现的漏洞，几乎必然导致确认偏误（越挖越觉得有）。改成「派一个全新的 agent 去推翻它」，把搜索目标从「找到漏洞」翻转成「排除漏洞」——**这本质上是把形式化验证的思路（证明 ¬P）搬进了 prompt 工程**。
- **143 KB 全部内容是 prompt + 校验器 + schema，没有一行依赖**。这意味着它可以被塞进任何 Agent 环境而不引入供应链风险，也**极易 fork 改造**（MIT 协议）——2,633 fork 印证了这一点。
- **Cloudflare 官方背书 + 明确溯源**：README 直接写明这是 Cloudflare 漏洞发现 harness 的种子项目，harness 后来长成了多阶段 fleet 级系统，**这个 skill 是它演化出来的单仓库起点**。业界愿意把内部 harness 的雏形开源，本身就是最强的质量信号。
- ⚠️ 关注理由：最后推送 2026-09-14，**近六周未更新**（但今日仍 +2,716 星，说明热度未退）；另外**这个 skill 天然是双刃的**——它同时也是一份「如何系统性地审计一个目标」的方法论文档，用于防守侧自查与自身 Agent 能力评估是安全的。

## 参考资料
1. [GitHub 仓库](https://github.com/cloudflare/security-audit-skill)
2. [Cloudflare 博客：Build your own vulnerability harness](https://blog.cloudflare.com/build-your-own-vulnerability-harness)
3. [配套：mukul975/Anthropic-Cybersecurity-Skills](../agent-skills/anthropic-cybersecurity-skills.md)
4. [配套：SnailSploit/Claude-Red](../agent-skills/SnailSploit-Claude-Red.md)
5. [配套：vxcontrol/pentagi](../security-ai/pentagi.md)
