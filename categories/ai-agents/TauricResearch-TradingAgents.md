# TauricResearch/TradingAgents

> 仓库：https://github.com/TauricResearch/TradingAgents · ⭐ 114,605（2026-10-26 API 实测） · Python · License: Apache-2.0

**一句话：** TradingAgents: Multi-Agents LLM Financial Trading Framework —— Tauric Research 开源的多智能体 LLM 金融交易框架，把「基本面 / 技术面 / 情绪 / 新闻」分析师、研究员、交易员、风控拆成独立 Agent，用辩论式协作汇聚出买卖决策。

## 核心能力
- **多 Agent 角色分工**：基本面分析师、技术分析师、情绪分析师、新闻分析师 + 研究员 + 交易员 + 风控官，各司其职
- **辩论机制（debate）**：分析师之间就分歧结论进行多轮辩论，由研究总监（Research Manager）汇聚共识——多智能体协作在决策密集型场景的标准范式
- **回测防未来函数**：v0.5.2 起，回测**只读取每个分析日期当时已发布的数据**，杜绝「事后诸葛亮」
- **决策即时结算**：v0.6.0 起，历史上已下出的决策在分析师工作期间先完成结算，回测与实盘口径一致
- **多模型分层调度**：v0.6.0 起支持**按模型层级配置不同 provider**——管理者与分析师可以跑在不同的模型上（如强推理模型跑决策、便宜模型跑批量分析）
- **可用自有订阅**：v0.7.0 起支持直接跑在自己的 ChatGPT Plus / Pro 计划上，不必自备 API Key
- **工程化输出**：CLI 无交互运行（`--ticker` / `--date` 等 flag）、报告保存为单页 HTML、每次运行的 settings 记录进报告、GitHub Release 附 wheel
- **并行分析师**：v0.5.2 起支持并行分析以提速；可选 Jev 社交舆情筛选

## 关键数据（2026-10-26 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 114,605（今日 +381） |
| 🍴 Forks | 22,130（fork 率 19.3%） |
| Open Issues | 151 |
| 协议 | Apache-2.0 |
| 语言 | Python |
| 创建时间 | 2024-12-28 |
| 最后推送 | 2026-10-16 |
| 主页 | https://arxiv.org/abs/2412.20138（论文） |
| Topics | agent, finance, llm, multiagent, trading |

## 适用场景
- 量化/金融 Agent 框架的研究与教学（多角色辩论架构的经典参考实现）
- 复现和对比「LLM + 交易决策」类论文的 baseline
- 个人/团队的行情分析辅助工作流（配合自有数据源与回测管线）

## 为什么值得关注
- **它是「学术背书 + 工程实现」齐全的标杆**：有 arXiv 论文（2412.20138）作为方法论出处，有 11 万星和 2.2 万 fork（19.3% 的 fork 率说明大量人在拿它做二次开发），有持续到 v0.7.0 的版本节奏。学术项目与工程项目的结合体在 Agent 领域不多见。
- **回测严谨性是它真正的技术护城河**：LLM 金融框架最常见的两个自欺是「未来函数」和「单模型瓶颈」，它一个用「按分析日切片数据」堵死，一个用「按模型层级配 provider」解开。**关注细节的成熟度，比关注 Agent 数量更能判断项目水平。**
- **多智能体「辩论」范式的通用参考**：分析师辩论 → 总监汇聚 → 交易员决策 → 风控把关，这条链路已经被多个论文和框架抄，TradingAgents 是被抄得最多的那批之一。
- ⚠️ 关注理由：最后推送 2026-10-16，**近十天未更新**但热度未退（今日仍 +381）；151 open issues 相对 11 万星属健康水平；Apache-2.0 可商用，但**金融建议类项目自带合规与免责声明义务**，务必按研究/教育用途定位，不要接实盘或对外提供投顾建议。

## 参考资料
1. [GitHub 仓库](https://github.com/TauricResearch/TradingAgents)
2. [论文：TradingAgents: Multi-Agents LLM Financial Trading Framework (arXiv:2412.20138)](https://arxiv.org/pdf/2412.20138)
3. [CHANGELOG.md](https://github.com/TauricResearch/TradingAgents/blob/main/CHANGELOG.md)
