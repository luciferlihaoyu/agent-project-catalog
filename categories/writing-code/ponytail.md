# Ponytail

> 仓库：https://github.com/DietrichGebert/ponytail · ⭐ 144.5K（2026-09-23 API 实测） · License: MIT · 官网：https://ponytail.dev

**一句话：** 让 AI 编程助手像房间里最懒的资深工程师思考——最好的代码是你没写出来的代码。

## 核心机制：七级懒人决策梯（动笔前必须一级级爬）
1. 这代码真的需要存在？（YAGNI）
2. 代码库里已经有了？→ 复用
3. 标准库能干？
4. 浏览器/运行时原生 API？
5. 已装依赖能搞定？→ 不新增依赖
6. 一行能写完？→ 绝不十行扩成百行
7. 都不行，才写**最小可跑实现**

## 实测数据（官方 README，真实 FastAPI+React 仓库 12 任务基准）
- 代码量 **-54%**，Token **-22%**，成本 **-20%**，速度 **+27%**
- 安全校验 100% 保留
- ⚠️ 早期宣传 -80~94% 被社区指出是单轮对比水分，作者已在 README 更正——它教 AI 不吹牛，自己也不吹牛

## 适用场景
任何"AI 手痒过度设计"的场景；支持 Claude Code / Codex / Cursor / Grok Build 等 20+ 智能体，斜杠命令 `/ponytail` / `/ponytail-review` / `/ponytail-audit`。
