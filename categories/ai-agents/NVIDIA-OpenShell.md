# NVIDIA/OpenShell

> 仓库：https://github.com/NVIDIA/OpenShell · ⭐ 18,799（2026-10-24 API 实测） · Rust · License: Apache-2.0

**一句话：** OpenShell is the safe, private runtime for fleets of autonomous AI agents. —— 英伟达开源的「自主 AI Agent 安全私有运行时」：Agent 想读文件、装包、调 API、用凭据？给它这个能力，但**不**给它对你数据、密钥和网络的无限访问权。

## 核心能力
- **内核级强制策略**：每个 Agent 跑在独立沙箱里，内核控制在运行时拦截每一次文件访问、系统调用和网络连接；出网前必须过策略检查
- **凭据隔离**：Agent 永远看不到真实凭据，OpenShell 只把凭据注入到「已批准端点」的请求里
- **形式化验证策略变更**：策略改动生效前用形式化验证标出「新增了哪些危险访问」（比如能带凭据连上新主机、调用新 API），必须等人审
- **多语言 SDK**：Python（uv add openshell）、TypeScript（npm install @nvidia/openshell-sdk）、Go（github.com/NVIDIA/OpenShell/sdk/go）
- **Gateway 控制面**：沙箱 / 策略 / 访问的统一管控，K8s 部署走 Helm（CNI 需支持 NetworkPolicy）
- **可扩展**：middleware、interceptor、compute driver
- **官方 Agent Skills**：`npx skills add NVIDIA/OpenShell`，教你的 agent 驱动 CLI、写沙箱策略、调试 gateway

## 关键数据（2026-10-24 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 18,799（今日 +1,119） |
| 🍴 Forks | 1,885 |
| Open Issues | 574 |
| 仓库体积 | 93 MB |
| 创建时间 | 2026-02-24 |
| 最后推送 | 2026-10-24T00:42:43Z |
| 主页 | https://docs.nvidia.com/openshell/latest/ |
| PyPI | `openshell` |

## 适用场景
- 给编码 Agent / 自主 Agent 套一层「最小权限」沙箱，替代 `docker run --privileged` 式裸奔
- 企业内网里跑 Agent，需要审计它到底读了什么文件、连了哪些域名
- 多 Agent 集群的策略统一管控与审批流
- 跑在 K8s 集群里的 Agent 工作负载

## 为什么值得关注
- **把「Agent 权限」从提示词约束提升到内核约束**。整个行业目前几乎都在靠 system prompt 说「请不要删我的文件」，这是纸糊的护栏。OpenShell 把它变成内核里的强制点，量级完全不同。
- **形式化验证用在策略变更上**是罕见组合。多数沙箱方案是「你写 YAML，我照做」；这里是「我先证明这次变更会放开什么，再让你签字」，对合规场景（金融/医疗）有直接价值。
- **英伟达下场做 Agent 运行时**，等于官方表态：Agent 基础设施是下一个军备竞赛的主战场。而且它同时提供 Skills 和多语言 SDK，意图是成为跨厂商 Agent 的公共底座，不绑定单一 Agent 框架。
- ⚠️ 关注理由：0.1.x 刚进入稳定发布节奏，API 仍可能变动；内核级拦截意味着跨平台（macOS/Windows）实现难度不同，生产落地前建议先用 `--top` 里的 demo 沙箱验证策略表达能力。

## 参考资料
1. [GitHub 仓库](https://github.com/NVIDIA/OpenShell)
2. [官方文档](https://docs.nvidia.com/openshell/latest/index.html)
3. [架构说明](https://docs.nvidia.com/openshell/latest/about/architecture)
4. [支持矩阵（Linux / macOS Apple Silicon / WSL2）](https://docs.nvidia.com/openshell/latest/about/support-matrix)
5. [策略与 advisor/prover](https://docs.nvidia.com/openshell/latest/how-it-works/policies/overview)
6. [0.1.0 升级指南](https://docs.nvidia.com/openshell/latest/upgrade/0-1-0)
