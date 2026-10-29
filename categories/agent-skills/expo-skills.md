# expo/skills

> 仓库：https://github.com/expo/skills · ⭐ 3,576（2026-10-29 API 实测） · Shell · License: MIT · 文档 https://docs.expo.dev/skills/

**一句话：** Expo 官方出品的 AI agent skill 集合 —— 给 agent 用的 Expo 构建 / 部署 / 升级 / 调试指南，覆盖 Expo SDK、React Native、EAS、Expo Router、原生模块全流程，**免费与付费边界直接写进 skill 描述**。

## 关键数据（2026-10-29 API 实测）

| 项 | 值 |
|---|---|
| ⭐ Stars | 3,576（今日 +90） |
| 🍴 Forks | 228（fork 率 6.4%） |
| 语言 / 协议 | Shell / MIT |
| Open Issues | 100（对 3.6 千星 = 2.8%） |
| 创建 / 最后推送 | 2025-11-30 / 2026-10-28 |
| Topics | 无 |
| 收录 | GitHub Trending 每日精选 2026-10-29（+90/日） |

## 核心能力

- **入口路由器 `expo-overview`**：Router 与共享 setup 规则，任何 Expo/EAS 任务先加载它再路由到具体 skill。
- **Framework 组（免费开源 SDK）**：`expo-project-structure` / `expo-router` / `expo-animation` / `expo-native-ui` / `expo-design-system` / `expo-ui`（SwiftUI + Jetpack Compose）/ `expo-data-fetching` / `expo-dom` / `expo-web-to-native` / `expo-module` / `expo-brownfield` / `expo-dev-client` / `expo-examples` / `expo-app-clip` / `expo-upgrade`。
- **Services 组（付费 EAS）**：`eas-app-stores` / `eas-hosting` / `eas-workflows` / `eas-observe` / `eas-update`。
- **免费/付费边界内嵌元数据**：每个 skill 描述带同一套标签，每个服务类 skill 开头即写 costs / plan-limits。
- **多宿主分发 + 分流更新**：
  - Claude Code / Codex → 官方插件市场（`claude plugin install expo@claude-plugins-official` / `codex plugin add expo@openai-curated`），市场自动更新；
  - Cursor / OpenCode / Copilot / Windsurf / Gemini / Cline / AMP / Factory Droid / Antigravity / Kiro CLI → skills CLI（`npx skills@latest add expo/skills --skill '*'`），更新用 `npx skills@latest update`。
- **明确自定位**：Expo 文档、Expo CLI、EAS CLI 仍是 source of truth，skill 只负责帮 agent「正确应用」它们。

## 为什么值得关注

- **第一个「平台方官方下场」发布的 agent skill 集合**：此前 skill 生态主力是社区整理（`aws/agent-toolkit-for-aws`、`cloudflare/security-audit-skill`、`NVIDIA/SkillSpector`），今天出现了官方账号 + 官方徽章 + 官方插件市场分发的形态 —— **平台方开始把「教 agent 怎么用我」当正式产品线做**。
- **把定价写进检索层**：当 agent 替你决策时，「这个功能要不要花钱」必须能被检索到，**这在本库已收录 skill 中是第一个做到的**。
- **尊重各家官方市场**：不强行统一到一个安装命令，而是按 agent 的官方渠道分流安装与更新 —— 这正是 agent 生态「不合并、只并存」现实的正确姿势。
- **敢写「我不是 source of truth」**：定位放在「正确应用」而非「取代文档」，比夸大其词的 skill 仓库成熟得多。

## ⚠️ 局限

- **更新即腐烂**：skill 描述的是 Expo SDK 的 API 与约束，**SDK 一升级 skill 即可能过时**，且没有版本钉住（不像 npm 有 semver），agent 读到哪一版取决于安装时刻。
- **主语言是 Shell**：skill 本身是脚本/Markdown 混合体，逻辑正确性靠什么保证尚未可知。
- **无 topics、无官网、issues 100**，GitHub 侧可检索性偏弱。
- **与官方文档的内容重叠度未知**：若 skill 只是把文档切碎重排，价值就只剩「省 token、少走弯路」——仍然值 3.5 千星，但**上限也止于此**。

## 参考

1. [GitHub 仓库](https://github.com/expo/skills)
2. [官方文档 docs.expo.dev/skills](https://docs.expo.dev/skills/)
3. [skills.sh 收录页](https://skills.sh/expo/skills)
