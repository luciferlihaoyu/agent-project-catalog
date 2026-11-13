# ashhart/TensorFold

> 仓库：https://github.com/ashhart/TensorFold · ⭐ 1,938（2026-11-13 API 实测） · Zig · License: Apache-2.0

**一句话：** LLM Inference Engine for Metal, CUDA and Vulkan —— 用 Zig 写的跨后端 LLM 推理引擎，一套内核同时吃苹果 Metal、NVIDIA CUDA、通用 Vulkan。

## 关键数据（2026-11-13 API 实测）

| 项 | 值 |
|---|---|
| ⭐ Stars | 1,938（今日 +54） |
| 🍴 Forks | 391（fork 率 20.2%，今日收录最高） |
| Open Issues | 522 |
| Topics | ai, ai-tools, llm, llm-inference, llm-tools |
| 首页 | https://tensorfold.dev |
| 创建时间 | 2026-06-19 |
| 最后推送 | 2026-11-13 |

## 为什么值得关注

- 直接对标 llama.cpp 的后端格局：一条代码路径覆盖 Metal / CUDA / Vulkan，而 llama.cpp 的 Metal+Vulkan 走 ggml 后端、CUDA 相对独立。做得成就是「一次编译，三类硬件」。
- **fork 率 20.2% 是本批最高**，说明拿到本地真编译真跑的人多，不只是点星收藏；Apache-2.0 可商用。
- 选 Zig 有技术合理性：无 CMake 生态包袱、编译期泛型写 kernel 顺手，与 lightpanda-io/browser 一起构成 Zig 进入「性能基础设施」的第二波证据。
- ⚠️ 522 open issues vs 1,938 星 = 每 3.7 星一个 issue，硬件矩阵远未铺平；**当学习样本和实验台可以，别直接替换生产里的 llama.cpp**。
