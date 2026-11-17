# kajisho5/ffmpeg-skill

> 仓库：https://github.com/kajisho5/ffmpeg-skill · ⭐ 6,724（2026-11-17 API 实测） · Python · License: MIT

**一句话：** Local video editor for coding agents —— 把 42 个 FFmpeg 能力包装成机器可读契约 + MCP server，让 Claude Code / Cursor / Codex 能可靠地剪视频、加字幕、改构图、调响度、按平台导出，全程本地、无云、无 API Key。

## 核心能力
- **42 个 FFmpeg 工具**：剪切 / 拼接 / 转码 / 加水印 / 抽音轨 / 变速 等常用视频操作全覆盖
- **机器可读契约**：每个工具都有明确 schema（参数类型、取值范围、输出约定），agent 按契约调用而不是猜命令行
- **MCP server**：标准 MCP 协议接入，Claude Code / Cursor / Codex 直接当工具用
- **字幕与文案**：字幕烧录 / 提取 / 时间轴处理
- **重构图（reframe）**：横转竖、主体追踪裁切，短视频平台适配
- **响度标准化**：广播级 loudness normalization，避免导出后忽大忽小
- **平台导出预设**：TikTok / YouTube / Reels 等尺寸与码率预设
- **零云依赖**：本地 FFmpeg 执行，素材不出机器、不花 API 费用

## 关键数据（2026-11-17 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 6,724（今日 +367，今日增速第一） |
| 🍴 Forks | 601（fork 率 8.9%） |
| Open Issues | 33 |
| 协议 | MIT |
| 语言 | Python |
| 创建时间 | 2026-09-03 |
| 最后推送 | 2026-11-16 |
| 主页 | https://www.npmjs.com/package/ffmpeg-skill |
| Topics | agent-skills, ai-agents, audio-processing, captions, claude-code, codex, coding-agent, cursor |

## 适用场景
- 让 coding agent 承担"视频批处理"这类枯燥但必须精确的活（批量裁切、统一响度、按平台导出）
- 自媒体工作流：一条素材 → 多平台尺寸/字幕/封面帧批量产出
- 无网络 / 保密素材环境（不放心上传云端剪辑工具）
- 想把视频能力塞进自己的 agent 流水线（MCP 直接接）

## 为什么值得关注
- **它的价值不在 FFmpeg，在"契约"二字。** 让 LLM 拼 ffmpeg 命令行是典型的不可靠操作——参数拼错就是静默产出废片。这个项目把能力收敛成有 schema 的动作，agent 做事变得可校验、可重试。**这是 agent 工具链里最被低估的一层工程。**
- **今日 +367 全场增速第一，且两个月前才创建**：说明这个需求一直存在（谁没被 ffmpeg 参数折磨过），只是没人正经做成 agent 可用的接口。
- **local-first 的组合拳**：无云 + 无 API Key，对"素材敏感"和"不想按次付费"这两类人都是直接解。
- ⚠️ 关注理由：依赖本机 FFmpeg 版本（不同版本 filter 行为有差异，建议锁版本）；重构图/主体追踪类需要额外的分析模型时能力边界会收窄；6.7K 星里相当一部分是"收藏待用"，实际生产案例还在积累。
