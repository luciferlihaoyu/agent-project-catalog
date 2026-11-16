# ggml-org/ggml

> 仓库：https://github.com/ggml-org/ggml · ⭐ 15,907（2026-11-16 API 实测） · C++ · License: MIT

**一句话：** 面向机器学习的张量库 —— llama.cpp 的底座，低层张量计算 + 多硬件后端 + gguf 量化格式的源码实现。

## 关键数据（2026-11-16 API 实测）

| 项 | 值 |
|---|---|
| ⭐ Stars | 15,907（今日 +43） |
| 🍴 Forks | 2,019（fork 率 12.7%） |
| Open Issues | 386 |
| Topics | machine-learning |
| 首页 | https://github.com/ggml-org |
| 创建时间 | 2022-09-18 |
| 最后推送 | 2026-11-13 |

## 为什么值得关注

- **本体单独上榜本身是信号**：ggml 长期只作为 [llama.cpp](ggml-org-llama.cpp.md) 的隐形依赖，现在被单独推到榜单，说明有人开始绕过 llama.cpp 直接在 ggml 上搭自己的推理栈。
- **新秀的公共地基**：TensorFold（Zig / 跨 Metal·CUDA·Vulkan）、colibri（纯 C / MoE 流式加载）这批轻量推理项目走的都是从 ggml 层重新分层，而非 fork llama.cpp。
- 四年日更，386 open issues 属 1.6 万星体量下的正常水位，最后推送 11-13 维护健康。
- 想判断「本地推理赛道温度」而不只是看 llama.cpp 单点，ggml 是更纯粹的底层指标。
