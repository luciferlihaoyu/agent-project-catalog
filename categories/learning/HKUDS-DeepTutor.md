# HKUDS/DeepTutor

| 项 | 值（2026-10-28 GitHub API 实测） |
|---|---|
| 仓库 | https://github.com/HKUDS/DeepTutor |
| ⭐ | 45,895（forks 5,757，fork 率 12.5%） |
| 语言 / 协议 | Python / Apache-2.0 |
| Open Issues | 218（对 4.59 万星 = 0.48%，很健康） |
| 最近推送 | 2026-10-27（创建 2025-12-28 · 立项约 10 个月） |
| Topics | ai-agents, ai-tutor, clawbot, cli-tool, deepresearch, interactive-learning, learning, multi-agent-systems |
| 官网 / 论文 | https://deeptutor.info/ · arXiv:2604.26962 |
| 收录 | GitHub Trending 每日精选 2026-10-28（+1,598/日） |

## 一句话
「终身个性化辅导」的 agent 原生学习工作台——把答疑、出题、研究、可视化、掌握度练习全部接在同一套能力运行时和同一份会话上下文上，Web 端给人用，CLI 端给别的 agent 用。

## 核心能力
- **One runtime for every mode**：Chat / Ask Questions / Quiz / Research / Visualize / Solve / Course Study / Mastery Path / Immersive Reading / Audio Overview 共享同一能力运行时与会话上下文，各自保留专用循环
- **CLI 双入口（Agent-Native）**：`deeptutor chat` 交互式 REPL；`deeptutor run <capability> "<msg>" --format json` 输出 **NDJSON 逐行事件流**（`content` / `tool_call` / `tool_result` / `done`），每行带 `session_id`，**headless 安全**（`ask_user` 无 TTY 时自动空回复而不挂起）
- **可被别的 agent 驱动**：仓库自带根 `SKILL.md` 作为交接文档，`deeptutor run` 可直接包成 LangChain / AutoGen 循环里的一个工具
- **多引擎知识库**：LlamaIndex / PageIndex / GraphRAG / LightRAG（含远程 Server）/ 自托管 WeKnora / MarginNote 4 / 腾讯 IMA / Kiwix ZIM / Obsidian vault，带可插拔文档解析
- **可检视的记忆**：L1 轨迹 → L2 表层摘要 → L3 综合，**Memory Graph 把 L2 事实连回 L1 证据**，个性化不是黑箱
- **Subagents 与 Partners**：可接 Claude Code / Codex / Grok CLI / Antigravity / Kimi / opencode / MiMo / Hermes / OpenClaw / DeepSeek 等 agent harness，或以同一「大脑」跑常驻 IM 伙伴
- **Task Board**：学习任务看板（待办 / 进行中 / 完成），卡片留在当前工作区、跟随外观与语言设置
- **沉浸式视频学习**：YouTube / Bilibili 链接原生播放 + 转写搜索 + 时间戳锚定的辅导
- **14 种语言 README**（含简中 / 繁中 / 日 / 西 / 法 / 俄 / 印地 / 葡 / 泰 / 波），社区在 Discord / 飞书 / 微信

## 为什么值得关注
- **4.59 万星 + 45,895 stars 仍在 +1,598/日**，立项仅 10 个月——这是教育类 AI 项目里罕见的体量与增速。
- **「给 agent 用」这件事做得比大多数教育项目彻底**：NDJSON 流式协议、`--format json`、headless 自动降级、仓库自带 `SKILL.md` 交接文档、专门写了 Agent Setup 指南。**它不是「把学习功能塞进 agent」，而是「把 agent 当成一等公民做接口设计」**——这与本库已收录的 `HKUDS/CLI-Anything`（让所有软件变 agent-native）是同一所实验室的同一条路线。
- **记忆可检视（L1/L2/L3 + Memory Graph）**是教育 AI 里少见的设计：个性化辅导最大的争议就是「凭什么这么说」，它把证据链摊开给人看。
- **Apache-2.0 + 4 阶段发版节奏**（v1.5.15 → v1.6.15 半个月迭代 6 次）+ 218 个 issue，成熟度远高于同类教育 Agent 仓库。
- 与本库已收录的 `xiaoyang111222/cn-math-taxonomy`（课标级数学知识图谱）、`Renhuai123/ziwei-doushu`（命盘引擎）构成「教育 AI 底座」的三件套：一个有知识图谱、一个有知识工作台。

## ⚠️ 局限
- **功能面极大 = 学习曲线陡**：单次发版覆盖 LightRAG / WeKnora / MarginNote / Kiwix / Paged Preview / 原生 speech，README 里全是特性清单，**上手路径比 star 数暗示的复杂**。
- **4.59 万星配 218 个 open issues 仍然偏多**（0.48%），对一个宣称「多用户协作（learner / guardian 账号）」的成熟项目，说明边界情况很多。
- **依赖极重**：Next.js 16 + Python 3.11+ + 多个 RAG 引擎 + 多个 provider，**自托管全量部署的坑不少**（有 Docker 一键试玩：`ghcr.io/hkuds/deeptutor:latest`，端口 3782）。
- **模型 provider 依赖**：核心能力（quiz / research / memory）全靠外部模型，**API key 成本与可用性是长期变量**。
- 教育场景的**准确性与版权**风险由使用者自行承担，README 未做明显免责。

## 参考
1. [GitHub 仓库](https://github.com/HKUDS/DeepTutor)
2. [官网 / 文档](https://deeptutor.info/)
3. [论文 · arXiv:2604.26962](http://arxiv.org/abs/2604.26962)
4. [Agent Handoff 文档](https://deeptutor.info/docs/cli/agent-handoff/)
5. 同族项目：HKUDS/CLI-Anything（本库 ai-agents 分类已收录）
