# basketikun/infinite-canvas（无限画布）

| 项 | 值（2026-10-30 GitHub API 实测） |
|---|---|
| 仓库 | https://github.com/basketikun/infinite-canvas |
| ⭐ | 9,400（forks 2,206，**fork 率 23.5%**，远高于均值——创作者真的在拿它干活） |
| 语言 / 协议 | TypeScript / MIT |
| Open Issues | 21（对 9.4 千星 = 0.22%，非常健康） |
| 版本 / 技术栈 | v0.20.0 · Vite 7 + React Router 7 |
| 创建 / 最近推送 | 2026-05-18（立项约 5 个半月）/ 2026-10-25 |
| 官网 | https://canvas.best |
| 部署 | Docker（`docker compose up -d` → :3000）· Render 一键部署 |
| 收录 | GitHub Trending 日榜 #12（2026-10-29，公众号「老王不爱唠嗑」卡片）；L 2026-10-29 飞书转发 |

## 一句话
面向 AI 图片创作的开源无限画布工作台——把画布编排、AI 生图、参考图编辑、视频生成、对话助手、提示词库、素材沉淀放进同一个节点式界面，类似「创作向的 ComfyUI」但更偏可视化工作流而非管线拼接。

## 核心能力
- **无限画布**：多画布项目、节点拖拽缩放、连线、小地图、撤销重做、导入导出
- **AI 创作（浏览器直连）**：前台直连自配的 OpenAI 兼容接口，文生图 / 图生图 / 参考图编辑 / 文本问答 / 音频与视频生成
- **画布助手**：围绕选中节点和上游节点对话、生图，结果直接插回画布
- **本地 Canvas Agent**：本机 Agent 连接 Codex / Claude Code，让 agent 通过 **MCP** 操作当前画布；另有 Codex App 插件自动注册 MCP
- **插件系统**：URL 动态安装/启用/更新/卸载远程节点插件，带 TypeScript SDK 自行开发
- **自定义接口调用**：可自定义生图/视频接口调用方式，灵活适配 chatgpt2api、grok2api、flow2api、newapi 等中转渠道
- **提示词库**：内置 7 个开源提示词来源，支持自定义标准 JSON 来源，前端直连并缓存到 IndexedDB

## 隐私亮点
API Key、画布、素材、生成记录**默认全部存浏览器本地（IndexedDB）**，不经后端——对隐私敏感用户是核心卖点。

## 为什么值得关注
- **5 个半月 9.4k 星 + 23.5% fork 率**，中文社区（Linux.do）驱动，迭代快（450+ commits）
- **Agent-native 的画布**：MCP + Codex 插件这条路子和 OpenClaw 生态高度契合——agent 直接操作画布节点是罕见设计
- 兼容中转站生态，接入门槛极低；有自建服务或免费渠道即可白嫖起步

## ⚠️ 备注
- 单人项目（邮箱/QQ 定制联系），bus factor 低；远程插件按 URL 加载，装第三方插件前留意供应链风险
