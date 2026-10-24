# SnailSploit/Claude-Red

> 仓库：https://github.com/SnailSploit/Claude-Red · ⭐ 8,491（2026-10-24 API 实测） · Python · License: MIT

**一句话：** claude-red is a curated library of offensive security skills designed for the Claude skills system. —— 78 个投放到 Claude Skills 系统的**进攻性安全**技能包，每个 SKILL.md 把某个攻击面（SQLi → shellcode → EDR 绕过 → ADCS 滥用）的方法论直接灌进 Claude 上下文。

## 核心能力
- **78 个技能 / 23 个类别**，全部是结构化 SKILL.md 文件，按会话触发词**按需加载**（不用的技能不占 context）
- **Web 应用**（16 个）：SQL 注入、XSS、SSRF、SSTI、XXE、IDOR、文件上传、RCE、反序列化、竞态条件、请求走私、开放重定向、参数污染、GraphQL、WAF 绕过、业务逻辑
- **认证与身份**（Active Directory 等）：目录攻击面专章
- **横向移动 / 权限提升 / 持久化**：从初始立足点到域控的完整路径
- **EDR 绕过 / ADCS 滥用 / shellcode / 漏洞开发**：端点与二进制层
- **多安装方式**：
  - Claude Skills：`git clone https://github.com/SnailSploit/Claude-Red ~/.claude/skills/claude-red`
  - Claude Code：`cat Skills/web/offensive-sqli/SKILL.md | claude --system-file -`
  - 单类别稀疏克隆：`git sparse-checkout set Skills/web Skills/active-directory`
  - Claude.ai：手动粘贴 SKILL.md 到 Project system prompt
  - `./install.sh --category web` 交互安装
- **MIT 协议**，商业友好

## 关键数据（2026-10-24 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 8,491（今日 +226） |
| 🍴 Forks | 1,100 |
| Open Issues | 24 |
| 仓库体积 | 2.4 MB |
| 创建时间 | 2026-03-04 |
| 最后推送 | 2026-10-12T15:02:40Z |
| 主页 | 无（研究站 snailsploit.com） |
| Topics | redteam, claude-skills, claude-pt, claude-ai, redteam-tools, skills |

## 适用场景
- 授权红队演练 / 漏洞赏金初筛 / CTF 备战
- 安全工程师的「打法检索库」：先查 skill 再决定用什么工具
- 教学：把某个攻击面的完整方法论固化成可复用的文本资产
- ⚠️ 仅限授权测试环境使用

## 为什么值得关注
- **它把「安全知识」从 PDF 变成可执行上下文**。传统做法是让模型查 OWASP 页面、翻一堆博客；这里是把某个攻击面**专家级的打法、工具链、边界情况、升级路径**预先写好，Claude 一触发就直接进入专家状态。SKILL.md 本身不过几 KB，却能省掉大量检索。
- **和「防御侧 skill」形成了完整对偶生态**。本 catalog 里已有 `mukul975/Anthropic-Cybersecurity-Skills`（817 个技能，映射 MITRE ATT&CK / NIST CSF 2.0 / ATLAS / D3FEND）、`vxcontrol/pentagi`（自主渗透测试 Agent）、`NationalSecurityAgency/ghidra`（逆向）、`ifixai-ai/iFixAi`（Agent 审计）。Claude-Red 填上的是**红队技能库**这一格，攻防两侧都能用 Claude 驱动，工具链已经闭环。
- **MIT 协议 + 1,100 fork**，说明大家是「拿去改造成自己的攻击手册」而不是「读一遍就过」。技能库的价值在**改写成本低**，这正是 MIT + Markdown 格式的组合优势。
- ⚠️ 关注理由：**双刃剑属性明确**。README 自己写明「用于授权红队、赏金、CTF、培训」，但方法论完整到可以直接武器化。用于防守侧自查、规则引擎建设、Agent 安全评估是安全的正途；直接用于未授权目标存在法律与伦理风险，请自行约束。

## 参考资料
1. [GitHub 仓库](https://github.com/SnailSploit/Claude-Red)
2. [技能索引（23 类全表）](https://github.com/SnailSploit/Claude-Red#skill-index)
3. [Claude Skills 官方文档](https://docs.claude.com)
4. [研究站 snailsploit.com](https://snailsploit.com)
5. [配套：mukul975/Anthropic-Cybersecurity-Skills](../agent-skills/anthropic-cybersecurity-skills.md)
