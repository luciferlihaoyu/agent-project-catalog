# archify

> 仓库：https://github.com/tt-a1i/archify · ⭐ 70.1K（2026-09-23 API 实测） · JavaScript · License: MIT

**一句话：** 让 AI 画架构图但不和 Mermaid 语法搏斗——AI 输出结构化 JSON，确定性渲染器生成可交互 HTML/SVG。

## 核心能力
- 五种图：架构 / 时序 / 数据流 / 工作流 / 生命周期
- Typed JSON IR 管道（Codebase → Agent 分析 → IR → HTML/SVG），比直接生成 Mermaid 更可验证
- 节点搜索、上下游关系追踪、路径追踪（trace route）
- 深/浅主题、交互动画、导出 SVG/PNG、存档分享
- **快照对比**：开发前后各跑一次，自动标记新增/删除/移动/改路由节点——Code Review 和交接神器

## 适用场景
系统架构文档化、Code Review 辅助、团队交接、任何需要"能验证的架构图"的场合。

## 安装
`npx skills add tt-a1i/archify -g` 一行，任何 Agent 对话里描述系统即可出图。
演示页：https://tt-a1i.github.io/archify/
