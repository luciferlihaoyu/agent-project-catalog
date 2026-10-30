# CursorTouch/Windows-MCP

| 项 | 值（2026-10-30 GitHub API 实测） |
|---|---|
| 仓库 | https://github.com/CursorTouch/Windows-MCP |
| ⭐ | 10,737（forks 1,165，fork 率 10.9%） |
| 语言 / 协议 | Python / MIT |
| Open Issues | 30（对 1.07 万星 = 0.28%，很健康） |
| 创建 / 最近推送 | 2025-05-13 / 2026-10-29（活跃，最新提交 #492 注册表键路径字面量传递修复） |
| Topics | ai, desktop, mcp, tools, windows, windows-automation |
| 官网 | https://windowsmcp.io |
| 用户规模 | Claude Desktop 扩展用户 **2M+**；新增 VM 支持 |
| 收录来源 | L 2026-10-29 飞书转发抖音 @迈迈学AI 视频（「让不同大模型都能接管 Windows」） |

## 一句话
让任意能调 MCP 的大模型（Claude / GPT / 本地模型都行）直接接管 Windows 桌面的 MCP server——AI 变成电脑操作员，靠模拟人对 GUI 的操作实现全权控制，不依赖厂商 API 集成。

## 核心能力
- 鼠标点击 / 移动、键盘输入与按键
- 截屏（全桌面或单窗口）
- 应用窗口管理与交互
- 文件系统导航
- 桌面应用工作流自动化、QA 测试
- Windows 7-11，本地 stdio transport 运行

## ⚠️ 安全须知（收录重点）
- **系统级执行能力**：能向 PowerShell 传注册表键路径（最新提交正是在修这块的传参安全）——本质是给 AI 一双完整的手
- **提示注入 = 拿到你的手**：AI 全权操作桌面时，任何被注入的指令都可能转化为真实系统操作
- **务必跑在 VM 里**：项目已提供 VM 支持，生产机不要直接喂鼠标键盘；与 2026-10-29「安全检查 TOP 10 Skill」榜单的 Agent 配置/攻击面思路互为印证

## 为什么值得关注
- 2M+ 用户的计算机使用（computer use）路线参考实现，MIT 宽松协议
- 不挑模型——只要求客户端支持 MCP，配 OpenClaw / Claude Desktop / Cursor 等都能跑
- 桌面自动化测试、重复操作批处理是正经生产场景
