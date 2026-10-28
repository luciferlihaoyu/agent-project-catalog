# togg53192-cmd/jailbreaks

| 项 | 值（2026-10-28 GitHub API 实测） |
|---|---|
| 仓库 | https://github.com/togg53192-cmd/jailbreaks |
| ⭐ | 5,538（forks 821，fork 率 14.8%） |
| 语言 / 协议 | —（纯 Markdown 提示词集） / **未标注** |
| Open Issues | 14 |
| 最近推送 | 2026-10-25（创建 2026-06-18 · 立项约 4 个月） |
| Topics | 无 |
| 收录 | GitHub Trending 每日精选 2026-10-28（+902/日） |

## 一句话
系统提示词、角色锁、工作区策略、Agent 操作规范的**策展式收藏**——31 份提示词覆盖 25+ 模型，每份都是完整可粘贴版本，不是摘要。

## 核心能力
- **31 prompts / 25+ targets**：OpenCode Zen 免费 stealth 模型（Big Pickle VANTA 角色锁、Space Bunny、LongCat 2.5、MiMo V2.6、Step 5 Preview、Muse Spark 1.3、Muse.ai）、闭源前沿（Claude Opus/Sonnet、Gemini、Grok、Mistral）、开源权重族（GLM、DeepSeek、Kimi、Qwen、Gemma、GPT-OSS）
- **覆盖全部指令载体**：完整 system prompt、persona 定义、workspace policy、`AGENTS.md` 文件、配置块、Ollama Modelfile
- **强调「paste-ready」**：README 明确要求「完整可粘贴，不给摘要、不给节选」——这是与普通「提示词合集」最大的区别，也是最有价值的部分
- **贡献规范严格**：一文件一提示词、小写连字符命名、必须标注归属载体（system prompt / `AGENTS.md` / Modelfile / 配置位）、大改必须升版本号、**不得声称未实测的兼容性**
- **自带时效性警告**：明确说明提示词行为高度依赖模型版本，模型更新、指令层级变化、系统提示轮换都会让旧提示失效

## 为什么值得关注
- **fork 率 14.8%（821/5,538）是今天三个新项目里最高的**，说明大量使用者是「拿去抄」而不是「读源码」——这类收藏型仓库的 fork 就是它的分发方式。
- **它记录的是「指令层级」这个正在变成一等公民的东西**：README 自述覆盖「instruction hierarchies, persona framing, prompt conflicts, and policy overrides」，并把这明确框定为 prompt injection 的**研究对象**。README 里那段 WARNING 说得很坦白：这些技术同样能用来研究怎么让系统**更抗**注入——**同一个仓库既是攻击面样本库也是防御研究样本库**。
- 与本库已收录的 `NVIDIA/SkillSpector`（skill 恶意扫描）、`blader/humanizer`（去 AI 味文本）形成对照：**SkillSpector 扫「skill 文件里有没有坏东西」，这个仓库收集「提示词本身能干什么」**——两者都指向同一个结论：2026 年 agent 安全的第一战场是**指令层**，不是二进制层。
- **5,538 星对应 31 份文件**，平均每份 178 星——单份提示词的传播力极强，提示词正在像「配置片段」一样被单独 fork 和复制。
- 对做 agent 的人有直接价值：它是**现成的负面样本集**——想知道「系统提示能被人为操纵到什么程度」，这里是最短的路径。

## ⚠️ 局限与合规提醒
- **协议未标注**（GitHub API 无 license 字段）——**默认版权保留**，不构成开源授权，商用/再分发需谨慎。
- **README 明确「仅供研究与教育」**，并声明模型服务商可能在其 ToS 下禁止此类用法，**使用者自行承担合规责任**。
- **时效性是硬伤**：模型一更新，提示词就可能失效。作者自己把「发现某份提示词行为已变」当成 issue/PR 的头号用途——**这是一份需要持续维护的活文档**，4 个月内从 0 做到 5.5 千星，维护节奏是否撑得住是关键观察点。
- **最后推送 2026-10-25**，距今 3 天；**无 topics、无描述**，GitHub 侧可检索性差。
- 收集的是**他人模型的系统提示词**，其本身可能涉及各服务商的知识产权与 ToS 问题。

## 参考
1. [GitHub 仓库](https://github.com/togg53192-cmd/jailbreaks)
2. 相关项目：NVIDIA/SkillSpector（本库 security-ai 分类已收录）、blader/humanizer（agent-skills 已收录）
