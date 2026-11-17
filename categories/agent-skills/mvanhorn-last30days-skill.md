# mvanhorn/last30days-skill

> 仓库：https://github.com/mvanhorn/last30days-skill · ⭐ 68,125（2026-11-17 API 实测） · Python · License: MIT

**一句话：** AI agent skill that researches any topic across Reddit, X, YouTube, HN, Polymarket, and the web - then synthesizes a grounded summary —— 跨六个信息源做"近 30 天"主题调研，并输出带出处的综述，专治 LLM 训练数据过时。

## 核心能力
- **六源并行检索**：Reddit / X / YouTube / Hacker News / Polymarket / 通用 web
- **"近 30 天"时窗**：把调研锁定在最近一个月，专门补模型知识截止日期之后的盲区
- **带出处的综述**：不是自由发挥，而是把抓到的原文摘要 + 链接作为 grounding 再综合
- **预测市场信号**：接入 Polymarket 是它区别于普通 deep-research 的地方——能拿到"市场当前怎么定价这件事"
- **Agent Skill 形态**：MIT、topics 含 claude-code / clawhub / ai-skill，可直接装进 Claude Code 等 agent
- **跨平台源**：还列了 bluesky，多云内容源覆盖

## 关键数据（2026-11-17 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 68,125（今日 +135） |
| 🍴 Forks | 6,037（fork 率 8.9%） |
| Open Issues | 31 |
| 协议 | MIT |
| 语言 | Python |
| 创建时间 | 2026-01-23 |
| 最后推送 | 2026-11-16 |
| Topics | ai-prompts, ai-skill, bluesky, claude, claude-code, clawhub, deep-research, hackernews |

## 适用场景
- 写周报 / 行业简报前，快速捞"这 30 天大家到底在聊什么"
- 技术选型：想看 HN + Reddit 真实吐槽而不是官方文档措辞
- 投资 / 市场研究：把预测市场赔率当情绪指标一起看
- 自媒体选题：找最近一个月已经被验证过热度的题材

## 为什么值得关注
- **它命中了 LLM 最真实的痛点**：知识截止。所有"帮我调研"的 prompt 都隐含一个时窗问题，而大多数方案靠模型自己想象最近发生了什么。这个 skill 把"最近 30 天"做成硬约束 + 真实抓取。
- **68K 星 / 31 open issues 的比例非常健康**，一年内做成这种体量且 issue 这么少，说明契约稳定、用户预期管理得好。
- **多源 + 出处的组合比单源 deep-research 可靠**：单看 X 会偏情绪，单看 HN 会偏工程，加 Polymarket 补了"钱怎么投"这一维——三视角交叉后综述的可靠性明显不同。
- ⚠️ 关注理由：依赖各平台的抓取可用性（X 的 API 政策变化风险最高），源失效会静默降级；综述仍可能被某些高热度低质量内容带偏，关键结论建议手动点回原文。
