# nodejs/node

> 仓库：https://github.com/nodejs/node · ⭐ 122,865（2026-10-24 API 实测） · JavaScript · License: NOASSERTION（MIT 式 + 第三方组件段落）

**一句话：** Node.js JavaScript runtime ✨🐢🚀✨ —— Node.js 官方运行时源码仓库，JS 生态的地基，全世界数百万个生产服务跑在它上面。

## 核心能力
- **V8 引擎集成**：Node 内置 V8，GC 调优、TurboFan / Sparkplug / Maglev 即时编译
- **libuv 事件循环**：跨平台异步 I/O 抽象（epoll / kqueue / IOCP / io_uring）
- **内置 Web 标准**：fetch、FormData、Blob、WebSocket、URL、Web Streams、structuredClone、Test Runner
- **诊断工具链**：内置 inspector（DevTools 协议）、`--cpu-prof` / `--heap-prof`、诊断报告、AsyncLocalStorage
- **权限模型**：`--permission` 运行时文件/网络/子进程访问控制（稳定版特性）
- **原生 TS 支持**：从 v22 起通过 type stripping 直接运行 `.ts` 文件
- **当前版本线**：v26.x（最新 release `v26.12.1`，2026-10-21 发布）；**v26 计划于 2026-10-28 进入 LTS**（codename 待定，维护至 2027-10-20，EOL 2029-04-30）；当前 v24「Krypton」已进维护期

## 关键数据（2026-10-24 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 122,865（今日 +66） |
| 🍴 Forks | 39,832 |
| Open Issues | 1,263 |
| Watchers | 3,018 |
| 仓库体积 | 1.6 GB（**本 catalog 最大的仓库**） |
| 创建时间 | 2014-11-26（自 io.js 分叉） |
| 最后推送 | 2026-10-24T00:09:23Z |
| 主页 | https://nodejs.org |
| 最新 release | v26.12.1（2026-10-21） |

## 协议说明（重要）
GitHub API 报 `NOASSERTION` / "Other"，**非标准 SPDX 标识**。实际内容为：
- Node.js 自身部分：MIT 式许可（Copyright Node.js contributors）
- 含从 joyent/node 继承的部分：MIT 式许可（Copyright Joyent, Inc. and other Node contributors）
- 末尾附有**第三方组件段落**（bundled dependencies 各有独立许可）
> 二次分发时需保留原版权声明与许可段落，并核对 `LICENSE` 全文的第三方组件条款。

## 适用场景
- 读 Node 源码理解 JS 运行时机制（事件循环、V8 集成、异步 I/O、模块系统）
- 为 Node 写原生插件（Node-API / N-API）
- 排查性能问题与内存泄漏（内置 profiler + inspector）
- 关注 Node 路线图与新特性落地

## 为什么值得关注
- **122,865 星 / 39,832 fork —— fork 率 32%**，这是全 GitHub 头部仓库里的顶级数字。原因很直白：几乎每个前端/全栈项目都会 fork 一份 Node 源码来加原生模块或改运行时行为。**它是「可改造性」的标杆**，对比一下闭源运行时连改都改不了。
- **1.6 GB 仓库体积是全 catalog 之最**，因为它 vendored 了完整 V8 源码树 + 第三方依赖。想读 V8 优化细节，Node 是最省事的入口（不需要单独 clone googlesource + gclient 那一套）。
- **今天它的意义不在于「涨星」，而在于「基座还在原地」**。当整个 Trending 榜被 agent skill 和 AI 基建刷屏时，Node 单日 +66 星却仍守住位置——这恰恰说明它的地位来自**不可替代性**：所有那些跑在 Node 上的 AI 工具（OpenCode、Claude Code、ComfyUI、vLLM 的各种前端）都站在它身上。**AI 应用越繁荣，Node 的地基价值越高，这是一条反向的复利。**
- ⚠️ 关注理由：**v26 此刻正处于「Current（现行）」与「LTS」的交界**——按 nodejs/Release 的 schedule.json，v26 的 LTS 起点是 **2026-10-28**（距今 4 天），v24「Krypton」已转入维护期。生产环境若要上 LTS 版本，正好赶上这个窗口；另外 `NOASSERTION` 协议在企业合规扫描工具里可能直接报警（"license unknown"），商用前建议在 SBOM 里显式声明 MIT + 第三方条款。

## 参考资料
1. [GitHub 仓库](https://github.com/nodejs/node)
2. [Node.js 官网](https://nodejs.org)
3. [LICENSE 全文](https://github.com/nodejs/node/blob/main/LICENSE)
4. [Node.js Release 工作流与版本策略](https://github.com/nodejs/Release)
5. [Node-API 文档（写原生插件）](https://nodejs.org/api/n-api.html)
6. [Node.js 诊断报告文档](https://nodejs.org/api/diagnostics_report.html)
