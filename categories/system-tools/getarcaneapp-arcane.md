# getarcaneapp/arcane

> 仓库：https://github.com/getarcaneapp/arcane · ⭐ 8,728（2026-11-17 API 实测） · Go · License: BSD-3-Clause

**一句话：** Modern Docker Management, Designed for Everyone —— Go 写的自托管 Docker 管理面板，容器 / 镜像 / Compose stack / 网络卷可视化管理，单二进制部署，替代 Docker Desktop 那一套付费授权。

## 核心能力
- **容器全生命周期**：列表 / 启停 / 日志 / 终端 / 环境变量 / 端口映射，在界面里完成日常运维
- **Compose stack 管理**：docker-compose 项目可视化管理与重建，不必再到服务器上敲 compose 命令
- **镜像与清理**：镜像、卷、网络统一视图，支持回收未使用资源
- **自托管优先**：单二进制 + Docker 部署，数据与管理面全在自己机器上
- **多环境**：通过 agent 方式接管多台 Docker 主机（本地面板 + 远端 agent）
- **Go 技术栈**：编译产物小、启动快、无运行时依赖

## 关键数据（2026-11-17 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 8,728（今日 +46） |
| 🍴 Forks | 404（fork 率 4.6%） |
| Open Issues | 11 |
| 协议 | BSD-3-Clause |
| 语言 | Go |
| 创建时间 | 2025-04-19 |
| 最后推送 | 2026-11-16 |
| 主页 | https://getarcane.app |
| Topics | compose, container-management, containers, docker, docker-compose, docker-management, go, self-hosted |

## 适用场景
- NAS / 家用服务器 / 小 VPS 上跑了一堆容器，需要一个"看得见"的管理面
- 团队不想为 Docker Desktop 的商业授权付费
- 把 Docker 管理界面暴露给非运维同事（简化为点按钮而不是记命令）
- 多台 Docker 主机想统一在一个面板里看

## 为什么值得关注
- **工程质量是今天清单里最干净的**：11 个 open issues / 8.7K 星，这个比例在同类面板里罕见；fork 率仅 4.6% 说明大多数人直接拿来用而不是拿去改——"装完就能跑"的成熟度。
- **和 Coolify / Dokploy 的定位差异要看清**：Coolify 是"从 Git 源码帮你部署成 PaaS"，Arcane 偏"管你已有的 Docker 环境"。两者不冲突，很多场景会一起用（Coolify 部署、Arcane 看运行态）。
- **Go 单二进制是这个品类的正确解法**：Portainer 那类重面板的运维负担（自身也要维护、要备份、要升级）在 Arcane 这里被压到很薄。
- ⚠️ 关注理由：**管理面板 = 你服务器的 root 钥匙**，暴露公网前必须 TLS + 强认证 + 内网/隧道访问，官方也建议配合反向代理鉴权；今日 +46 的低热度意味着社区样本还少，生产先小范围验证。
