# coollabsio/coolify

> 仓库：https://github.com/coollabsio/coolify · ⭐ 64,380（2026-10-26 API 实测） · PHP · License: Apache-2.0

**一句话：** An open-source, self-hostable PaaS alternative to Vercel, Heroku & Netlify —— 一条 SSH 就能把 VPS / 裸金属 / 树莓派变成 PaaS：Git 仓库一键构建、托管数据库、360+ 一键服务，**配置始终留在你自己的服务器上**。

## 核心能力
- **任意应用部署**：从 GitHub / GitLab / Bitbucket / Gitea 源码构建，也可用 Nixpacks、Railpack、Dockerfile、Docker Compose 或预构建 Docker 镜像
- **数据库与托管服务**：内置托管数据库 + **360+ 一键服务**（Postgres、MySQL、Redis、MongoDB、MinIO 等），带持久化存储
- **零门槛接入**：只需要一个 SSH 连接——VPS、裸金属、树莓派都行，不挑硬件
- **配置不迁走**：配置留在你的服务器上；**卸载 Coolify 后，已运行的资源照常工作、依然可管理**——这是它和绝大多数「一键上云」工具最本质的差别
- **自托管优先**：开源、免费，理念与商业版分开（另有托管的 Coolify Cloud）
- **技术栈现代**：Laravel + InertiaJS + MariaDB / Docker Compose，PHP 生态

## 关键数据（2026-10-26 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 64,380（今日 +152） |
| 🍴 Forks | 5,785（fork 率 9.0%） |
| Open Issues | 363 |
| 协议 | Apache-2.0 |
| 语言 | PHP |
| 创建时间 | 2021-01-25 |
| 最后推送 | 2026-10-25 |
| 主页 | https://coolify.io |
| Topics | coolify, databases, deployment, docker, docker-compose, inertiajs, laravel, mariadb |

## 适用场景
- 想把散落的 VPS / 树莓派 / 裸金属统一成可自助运维的内部 PaaS
- 小团队自建：静态站、API、数据库、对象存储、博客、监控栈一次装齐
- 需要「一键回滚 + 一键重建」而不想把全部运维压给一个人
- 受限于云厂商定价/合规，需要自持基础设施的团队

## 为什么值得关注
- **它是自托管 PaaS 的事实标准，也是「退出成本」做得最认真的一家。** 绝大多数「一键上云」工具的通病是导出即失灵——配置、密钥、编排全在厂商侧，你一走它就报废。Coolify 把「配置在你自己的服务器上、卸载后服务继续跑」写进产品定义，**这条约束直接决定了你敢不敢把它用在生产上。**
- **五年了还在涨**：2021 年立项，今天仍有 +152/天、64K 星、5.8K fork。在 PaaS 这个被大厂反复洗牌的赛道里能持续五年，本身就是产品与生态双重验证。
- **360+ 一键服务模板是它真正的护城河**——比同类（Dokploy、CapRover 等）的体量优势明显：Postgres / MySQL / Redis / MongoDB / MinIO / 各类中间件都有持久化存储与健康检查的现成配置，新手不用从零写 docker-compose。
- **PHP 技术栈对自建友好**：Laravel + InertiaJS + MariaDB 的组合在中小型自建站场景里运维门槛最低，配置文件可读性远好于大量 YAML 黑盒。
- ⚠️ 关注理由：363 open issues；**Coolify 自身的权限等级极高**（持有你服务器的 SSH 密钥与 root 级能力），一旦暴露公网必须做访问控制、强口令/TLS、备份与审计，多租户场景需额外评估；对比同类的 Dokploy / CapRover 值得横向看，但服务模板生态这一层的差距是实打实的。

## 参考资料
1. [GitHub 仓库](https://github.com/coollabsio/coolify)
2. [官网 coolify.io](https://coolify.io)
3. [官方文档](https://coolify.io/docs)
4. [项目哲学](https://coolify.io/philosophy)
