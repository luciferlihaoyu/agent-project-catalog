# google-research/paper-orchestra

> 仓库：https://github.com/google-research/paper-orchestra · ⭐ 1,517（2026-11-17 API 实测） · Python · License: Apache-2.0

**一句话：** PaperOrchestra is a multi-agent framework for automated AI research paper writing —— Google Research 的多 agent 论文写作框架，把「调研 → 大纲 → 写作 → 图表 → 修订」拆成流水线。

## 核心能力
- **多 agent 分工**：不同 agent 承担文献调研、结构规划、章节撰写、图表生成、自我修订
- **端到端流水线**：从一个研究主题/实验结论出发，产出可读的论文草稿
- **研究向定位**：topics 为 ai-research-assistant / multi-agent-systems，是研究工具而非写作软件
- **官方项目页**：配套实验说明与示例（yiwen-song.github.io/paper_orchestra）
- **Apache-2.0**：商用友好，改造成本低

## 关键数据（2026-11-17 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 1,517（今日 +313） |
| 🍴 Forks | 238（fork 率 15.7%） |
| Open Issues | 33 |
| 协议 | Apache-2.0 |
| 语言 | Python |
| 创建时间 | 2026-05-01 |
| 最后推送 | 2026-11-15 |
| 主页 | https://yiwen-song.github.io/paper_orchestra/ |
| Topics | ai-research-assistant, multi-agent-systems |

## 适用场景
- 综述类论文的文献组织与初稿骨架（最稳的用法）
- 课题组内部的写作流程实验：对比"人写" vs "agent 起草 + 人修订"
- 多 agent 编排的学习样本：看 Google Research 怎么切分写作任务、怎么做 agent 间校验
- 论文相关产物（摘要、相关工作、实验描述）的半自动生成

## 为什么值得关注
- **fork 率 15.7% 是今天新收录最高的**——在 1.5K 星的小体量下，这个比例说明有相当一部分人装完立刻在改（改 prompt 链、改领域、改输出格式），而不是只看 README。
- **Google Research 出手意味着方法论有背书**：多 agent 写作这件事被学术界认真做成了可复现框架，而不是自媒体的"AI 写论文神器"。
- **它对 agent 编排的启发大于对写作的启发**：怎么拆任务、怎么让一个 agent 校验另一个 agent 的产出，这套结构可以搬到报告、技术文档、审稿意见生成。
- ⚠️ 关注理由：**学术诚信红线自己把握**——能起草不等于能署名，绝大多数期刊/会议要求实质贡献与数据真实性，把它做成"全文代写"是自毁前程；另外 1.5K 星体量 + 33 open issues，工程成熟度还在早期，别指望开箱即用。
