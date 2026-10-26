# JetBrains/thinkrail

> 仓库：https://github.com/JetBrains/thinkrail · ⭐ 1,734（2026-10-26 API 实测） · TypeScript · License: Apache-2.0

**一句话：** Vibe code with pi in a lightweight, real IDE that customises itself around the way you work —— JetBrains 孵化项目：给第三方 `pi` 编码 Agent 套一层真 IDE（Monaco 编辑器 + 终端 + 文件树），用 git worktree 隔离并行工作区，用 living specs 让项目意图跨会话存活。

## 核心能力
- **隔离工作区（Isolated workspaces）**：打开任意 git 仓库作为 project，用 `git worktree` 切出多个工作区，各有独立分支与工作目录，**Agent 可并行干活而不碰你的 checkout**；好的分支合并，其余删掉。完成/休眠的工作区自动「settle」到项目专属 shelf，PR 合并或关闭、或一周无操作后自动收起，再工作时会回来
- **真 IDE 而非聊天框**：可切分的 Monaco 编辑器标签页、带实时 git 变更标记的文件树 / Changed 视图、终端、文档，全部作用域限定在当前工作区；可在文件与 diff 上留锚定 review 评论并作为结构化上下文发进对话，也能直接用已安装的 IDE 打开该 worktree
- **会思考的流式对话**：每个工作区可并发多个 `pi` 会话，各自带自己的模型和实时 token / 成本读数；可中途引导（steer）正在跑的回合、排队后续任务、委派给 subagent，共用一份 agent 会持续更新、你也能编辑的共享 plan，每完成一步即可单独提交与评审
- **living specs 即持久记忆**：代码旁挂一棵连通的 `SPEC.md` 关系图，Agent 通过专用 `spec_*` 工具读取、检索、维护，**意图因此跨会话存活**；只读的 Specs 工具在工作台里把图渲染成树
- **Skills 与工作流**：可直接就地读取你在别的编码 Agent 里已经维护的 Agent Skills，另有内置工作流引导项目初始化、设计头脑风暴、走完发 PR 流程（用你自己的 `gh` 推分支并开/更新 PR）
- **Agent 专属工具**：网页调研、行内图表、方案对比、文件预览；Agent 提出 UI 改动时直接给 before/after 效果图，你可以像看 diff 一样在图上评论。Settings → Extensions 列出 Agent 能用的扩展并可逐个关闭
- **MCP servers**：读取 `pi` 的 `mcp.json`；**Agent 调非只读工具前会先在对话里问你**，仓库自带的 server 保持关闭待批准，可对信任项目永久放行，支持 OAuth 登录
- **你的 provider、你的凭据**：用 JetBrains AI 登录或走 `pi` 自己的任意 provider 认证，**ThinkRail 不设自有账号**
- **桌面应用或浏览器**：原生桌面应用，或 `thinkrail` CLI 在浏览器里打开同一个应用，二者共用同一 engine host，状态存 `~/.thinkrail`
- **多语言**：Settings → Language 跟随系统或手动选择，内置英文与简体中文，支持自定义翻译

## 关键数据（2026-10-26 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 1,734（今日 +51） |
| 🍴 Forks | 102（fork 率 5.9%） |
| Open Issues | 201 |
| 协议 | Apache-2.0 |
| 语言 | TypeScript |
| 创建时间 | 2026-07-08 |
| 最后推送 | 2026-10-26 |
| 主页 | https://thinkrail.ai/ |
| Topics | agent, agent-skills, agentic-ai, agentic-workflow, ai-coding, ai-tools, pi-agent, pi-agent-extension |

## 适用场景
- 需要「一个真实 IDE + 一个能真正干活的编码 Agent」的团队
- 并行多任务：每个任务切一个 worktree，Agent 并行改代码互不干扰
- 长期项目的意图沉淀：living specs 让需求/设计决策不随会话消失
- 不想被单一厂商绑定：底层 Agent 是开源 `pi`，provider 走自己的账号

## 为什么值得关注
- **它把「Agent 宿主层」正式摆上了台面。** JetBrains 没有自研 Agent 引擎，而是选择给第三方的 `pi` 做宿主——等于公开承认「模型和 Agent 引擎是别人的，编辑器才是自己的地盘」。**IDE 从「写代码的地方」退化成「Agent 的宿主与仲裁层」**，这个转身是 2026 年 IDE 行业最关键的战略动作。
- **三个设计点值得直接抄**：
  1. **worktree 即工作区** —— 把「Agent 并发」从概念变成 Git 原生操作，天然隔离、无需容器、复用你现有的 CI；
  2. **living specs 即记忆** —— 不是聊天记录，是可演进的规格关系图，agent 有专门的 `spec_*` 工具去读写维护；
  3. **PR 是终态** —— 顶栏直接显示分支与 `origin` 的差距、CI 检查结果、review 决策，一键 publish / push / 开 PR（PR 描述可由 plan、commit、PR 模板或 Agent 草稿生成），失败检查可直接甩回给 Agent 修。
- **权限默认值给得很克制**：MCP 非只读工具调用前必问、仓库自带 server 默认关闭待批、OAuth 走设置面板——在「Agent 默认拿到什么」这件事上，它比多数同类激进做法更保守。
- ⚠️ 关注理由：**201 个 open issues 对 1,734 星，比例极高**——这既是早期项目的真实反馈通道，也说明稳定性仍在爬坡；README 明说「接下来要加完整扩展支持，让 ThinkRail 能自己造出需要的工具」，扩展能力仍在 roadmap 阶段；JetBrains Incubator 徽章意味着可能长期在孵化期，建议先在非核心项目上试水。

## 参考资料
1. [GitHub 仓库](https://github.com/JetBrains/thinkrail)
2. [官网 thinkrail.ai](https://thinkrail.ai/)
3. [官方博客 thinkrail.ai/blog](https://thinkrail.ai/blog/)
4. [底层 pi Agent](https://www.npmjs.com/package/@earendil-works/pi-coding-agent)
