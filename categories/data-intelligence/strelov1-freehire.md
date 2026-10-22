# strelov1/freehire

- **URL**: https://github.com/strelov1/freehire
- **语言**: Go
- **协议**: MIT
- **星标**: 2,383（今日 +360）
- **Fork**: 244
- **首次入库**: 2026-10-22
- **首页**: https://freehire.me
- **Topics**: ats, career, careers, golang, hiring, job-aggregator, job-board, job-portal, job-scraper, job-search, jobs, langchain, llm, meilisearch, postgresql, recruitment, remote-jobs, self-hosted, svelte, sveltekit
- **创建时间**: 2026-06-07

## 一句话描述

**freehire — the open-source search engine for job seekers.** —— 面向求职者的开源职位搜索引擎：直接从各公司招聘官网抓取 **330 万+ 实时职位**（不经过招聘中介、不转载、不留死链），全开源、可自托管。

## 核心能力

- **源头直取**：绕过聚合站，从企业 career page 直接抓取，过滤掉中介重复岗与过期岗
- **Go + SvelteKit + Postgres + Meilisearch**：高并发抓取 + 全文检索的现代栈
- **AI 能力内置**：topics 里带 langchain / llm，职位解析与匹配走 LLM
- **自托管优先**：MIT 协议，可作为自建 ATS / 招聘门户的底座
- **Product Hunt 上榜**（2026-08-26 发布）

## 备注

归类 **data-intelligence**（数据抓取/检索类）—— 与 withmarbleapp/os-taxonomy 同类：都是"把散落数据变成可查询结构"的工程。**关注点**：求职赛道今年被 AI 彻底重做（career-ops、ai-job-search、freehire 扎堆出现），但 freehire 的差异点是**做数据源而非做 agent** —— 它解决"职位数据从哪来、准不准、会不会是死链"这个最脏最累的活，Go 写的抓取层扛得住高频刷新，MIT 协议也最适合被人拿来搭自己的招聘站。4 个月 2.3K 星 + 每天 +360 属于陡峭上升期，值得盯。
