# NVIDIA/SkillSpector

| 项 | 值（2026-10-27 GitHub API 实测） |
|---|---|
| 仓库 | https://github.com/NVIDIA/SkillSpector |
| ⭐ | 22,187（forks 1,937，fork 率 8.7%） |
| 语言 / 协议 | Python / Apache-2.0 |
| Open Issues | 175 |
| 最近推送 | 2026-10-23（创建 2026-03-21） |
| 官网 | https://docs.nvidia.com/skills/scanning-agent-skills |
| 收录 | GitHub Trending 每日精选 2026-10-27（+214/日） |

## 一句话
在安装 Claude Code / Codex / MCP skill **之前**先扫一遍——71 个检测模式覆盖 17 个类别，抓提示注入、数据外泄、提权、供应链与记忆投毒。

## 核心能力
- **多格式输入**：git 仓库、URL、zip 文件、目录、单文件全部可扫（覆盖 skill 的全部真实分发形态）
- **71 个漏洞模式 / 17 个类别**：prompt injection、data exfiltration、privilege escalation、supply chain、excessive agency、output handling、system prompt leakage、memory poisoning、tool misuse、rogue agent、anti-refusal、trigger abuse 等
- **fail-closed 资源上限**：bundle / parser / 嵌套产物 / ledger / finding 均有硬性天花板，防止恶意 skill 用资源耗尽或分析器递归自我规避
- **Pi / OpenCode 扩展**：可在 agent 会话内部直接调用扫描，而非只能做 CI 门禁
- **进入发布管线**：SkillSpector 是 [NVIDIA Verified Skills](https://docs.nvidia.com/skills/) 的第一步——扫描 → 评估 → **签名** → 发布进 NVIDIA skills catalog

## 关键数据
- 官方研究：在 **31,132 个 skill** 的分析样本中，**26.1% 含漏洞，5.2% 疑似恶意**

## 为什么值得关注
- **skill 是带隐式信任安装的**：Claude Code / Codex / Gemini CLI 加载 skill 时不要求逐条确认，用户甚至不知道它改写了什么系统提示——这个攻击面比 npm 更裸露。
- **「签名」这一步是行业级的**：通过扫描的 skill 拿到大厂背书的签名，逻辑等同 npm provenance，只是对象换成了 skill。
- `excessive agency`（过度授权）与 `memory poisoning`（记忆投毒）两类是同类工具普遍漏掉的，而它们恰恰最贴近 skill 的真实攻击面。
- 1,937 fork / 8.7% fork 率在安全类项目里偏高，说明大量用户是接入自己 CI 流水线而非读源码。

## ⚠️ 局限
- 只解决「skill 本身恶意」，不解决「skill 描述的功能本身就是危险能力」——后者属授权问题，需配合运行时沙箱（如 NVIDIA/OpenShell）。
- Apache-2.0 可商用，适合作为 CI 门禁自建。

## 参考
1. [GitHub 仓库](https://github.com/NVIDIA/SkillSpector)
2. [官方文档 · 扫描 agent skills](https://docs.nvidia.com/skills/scanning-agent-skills)
3. [分析资源上限说明](https://github.com/NVIDIA/SkillSpector/blob/main/docs/ANALYSIS_RESOURCE_BOUNDS.md)
