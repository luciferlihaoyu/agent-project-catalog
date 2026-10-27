# nightly-labs/openbot

| 项 | 值（2026-10-27 GitHub API 实测） |
|---|---|
| 仓库 | https://github.com/nightly-labs/openbot |
| ⭐ | 1,475（forks 185，fork 率 12.5%） |
| 语言 / 协议 | TypeScript / NOASSERTION（README 标注 PolyForm Noncommercial 1.0.0） |
| Open Issues | 202（对 1,475 星 = 13.7%，早期项目特征） |
| 最近推送 | 2026-10-26（创建 2026-08-12） |
| 官网 | https://openbot.run/ |
| 收录 | GitHub Trending 每日精选 2026-10-27（+176/日） |

## 一句话
本地优先的桌面「AI 队友工作台」——每个 Agent 一个独立工作区 + 独立会话，配 FIFO 任务队列、文件传输、内嵌浏览器和 Agent 间消息。

## 核心能力
- **多 Agent 后端统一**：Codex App Server 与 Claude Code 原生接入；Grok CLI、OpenCode、Gemini、Cursor CLI、Cline CLI 走 **ACP** 接入；支持自定义 OpenAI 兼容端点与自定义 ACP agent，自动探测本地模型服务器（Ollama、LM Studio）
- **持久化队友**：prompt 驱动的 Agent 创建与编辑（可编辑 instructions、头像、段落级 review），每个 Agent 绑定独立会话与本地工作区
- **FIFO 消息队列**：支持暂停 / 恢复 / 取消 / 崩溃安全持久化
- **Agent 间通信**：互相发消息、回复、表情、传图、文件传输；共享桌面频道聊天（单一任务负责人、显式委派、共享历史，支持 Stop / Resume / Reassign / Archive / Restore）
- **每 Agent 上下文监控**：长线程撑爆模型窗口前自动 compact
- **常驻内嵌浏览器**：Agent 可直接打开、检查并控制

## 为什么值得关注
- **ACP 正在成为「换模型 / 换 Agent」的通用插槽**——原生 + ACP 双轨接入的意义比它自己实现的任何功能都更具行业价值。
- **把上下文管理下沉到宿主层**，而不是指望每个 harness 各自实现。
- 12.5% fork 率对 1.4k 星的小盘项目偏高，说明有人在拿它做二次开发。

## ⚠️ 局限（README 自述）
- **安全姿态激进**：development preview 阶段，Agent 以 `danger-full-access` + `approvalPolicy: never` 运行——首次同意后不再逐次确认，可读改文件、执行命令、联网、控制浏览器。只跑可信 Agent 与任务，务必备份。
- **协议非 OSI 开源**：PolyForm Noncommercial 1.0.0 —— 非商业免费，**商用需授权**，GitHub API 识别为 NOASSERTION。
- 项目很新（2026-08 立项，昨天仍在推送），接口与数据格式仍可能变。

## 参考
1. [GitHub 仓库](https://github.com/nightly-labs/openbot)
2. [官网 openbot.run](https://openbot.run/)
3. [Codex App Server 文档](https://learn.chatgpt.com/docs/app-server)
