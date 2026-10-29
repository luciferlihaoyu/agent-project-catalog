# ruvnet/RuView

> 仓库：https://github.com/ruvnet/RuView · ⭐ 101,055（2026-10-29 API 实测） · Rust · License: MIT · 官网 https://Cognitum.One/RuView

**一句话：** π RuView —— 用廉价 ESP32 节点抓 WiFi 的 **CSI（信道状态信息）**，把普通路由器变成空间感知系统：穿墙检测人在不在、几个人、呼吸率心率、跌倒手势、睡眠分期与呼吸暂停筛查，**全程零摄像头零穿戴**。

## 关键数据（2026-10-29 API 实测）

| 项 | 值 |
|---|---|
| ⭐ Stars | 101,055（今日 +557） |
| 🍴 Forks | 13,161（fork 率 13.0%） |
| 语言 / 协议 | Rust / MIT |
| Open Issues | 504（对 10.1 万星 = 0.50%，比例健康） |
| 创建 / 最后推送 | 2025-06-07 / 2026-10-29 |
| Topics | awesome, claude, densepose, esp32, firmware, home-assistant, home-automation, iot |
| 模型权重 | https://huggingface.co/ruvnet/wifi-densepose-pretrained |
| 收录 | GitHub Trending 每日精选 2026-10-29（+557/日） |

## 核心能力

- **感知层**：存在与人数（穿墙）、呼吸率与心率（非接触）、活动识别（走/坐/手势/跌倒）、RF 指纹房间识别与家具移动检测、过夜睡眠分期与呼吸暂停筛查。
- **无摄像头姿态**：WiFi DensePose 从 CSI 估计 17 个身体关键点。
- **模型工作流**：录制 CSI → 训练模型 → 加载 RVF 文件 → 切换 LoRA profile。
- **生态接入**：Home Assistant 一个 `--mqtt` 标志接入，**每节点 21 个实体**（11 路原始信号 + 10 路推断语义：someone-sleeping / possible-distress / room-active / elderly-inactivity-anomaly / meeting-in-progress / bathroom-occupied / fall-risk-elevated / bed-exit / no-movement / multi-room-transition）+ 3 个 HA Blueprint；Matter Bridge 接入 Apple Home / Google Home / Alexa / SmartThings。
- **统一 RF 世界模型**：可融合 WiFi CSI + 毫米波雷达 + UWB + 蜂窝感知到同一隐私边界内的场景模型。
- **治理与证据**：感知事件可附带隐私策略、不确定性、来源与见证记录。
- **MetaHarness（`@ruvnet/ruview`）**：source-cited guidance、设备访问与 CSI 实时流、固件刷写（带 boot evidence）、**一个 MCP server**（stdio 或 HTTP）、Claude Code mod、受限 Claude Code/Codex agent、确定性 verify、claim-check 诚实性检查。
- **安全默认**：agent run 默认只读，写工作区需 `--allow-write` + `--confirm`；硬件读需 `device-access` 授权；**刷固件与校准永不走 HTTP 传输**。

## 为什么值得关注

- **把「感知」的边际成本从「摄像头 + 带宽 + GPU + 布线」压到「一个几十块的 ESP32」** —— 这是成本与部署量级的碾压，不只是隐私卖点。
- **10 万星 + 1.3 万 fork + 每天仍 +557 + 有真实硬件在跑**，三者同时成立的项目极少。
- **它没停在「能演示」，而是铺到生态位上**：HA / Matter / Apple Home / Google Home / Alexa 全通 —— **「能接进别人家的智能家居」比「自己能跑」难一个数量级**，这是硬件项目能否活过第一年的分水岭。
- **给 agent 配了「不许吹牛」的护栏**：MCP + 受限 agent + 确定性 verify + `claim-check --file REPORT.md`；README 自陈「accuracy is still synthetic until real-data validation」，设备体征标注低置信。**在一个满是吹牛的赛道里，主动交代边界反而更容易拿到信任和生态位。**
- 与本库已收录的 `pollen-robotics/microduck` 同属「开源硬件/感知」赛道，但方向截然不同：microduck 是**可见的身体**，RuView 是**不可见的场**。

## ⚠️ 局限

- **精度是最大变量**：README 自己承认合成数据上的准确率不等于真实环境，这是整个 WiFi sensing 赛道的原罪，需看真实住宅长跑数据。
- **504 个 open issues** 比例仅 0.5%（健康），但绝对量说明边缘情况（多人、隔墙、多径干扰）极多。
- **硬件门槛甩不掉**：消费级路由器 CSI 质量参差，好效果依赖特定网卡/节点，环境敏感度决定它是「实验室神器」还是「家庭真能用」。
- **项目面过宽**：python/ + firmware/ + harness/ + dashboard/ + ui/ + v2/ + aether-arena/ + wifi-veil/ 多线并行，有**概念先行、收敛未完成**的味道。
- **隐私法规张力**：不用摄像头是卖点，但**无感知的呼吸/心率/存在检测本身是更高敏感度的数据**，责任边界比摄像头更模糊。

## 参考

1. [GitHub 仓库](https://github.com/ruvnet/RuView)
2. [官网 Cognitum.One/RuView](https://Cognitum.One/RuView)
3. [模型权重 huggingface](https://huggingface.co/ruvnet/wifi-densepose-pretrained)
4. [HA 集成文档](https://github.com/ruvnet/RuView/blob/main/docs/integrations/home-assistant.md)
