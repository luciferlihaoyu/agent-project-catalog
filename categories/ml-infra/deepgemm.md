# deepseek-ai/DeepGEMM

| 项 | 值（2026-10-08 GitHub API 实测） |
|---|---|
| 仓库 | https://github.com/deepseek-ai/DeepGEMM |
| ⭐ | 8,861 |
| 语言 / 协议 | Cuda / MIT |
| 最近更新 | 2026-09-30 |
| 收录 | GitHub Trending 每日精选 2026-10-07（+199/日） |

## 一句话
DeepSeek 出品的**干净高效的 GPU BLAS 内核库**，专攻 GEMM 核心算子。

## 核心能力
- 面向 Hopper 架构的高性能 GEMM / Grouped GEMM（含 FP8 场景）
- **JIT 编译**：运行时按需编译内核，无需预编译全部组合
- 轻量低依赖，工程实现干净（这也是它能上榜的原因：可作为 CUDA 内核学习范本）

## 适用场景
- 大模型推理 / 训练的性能优化（尤其 MoE 场景的 grouped GEMM）
- CUDA 内核开发者学习高质量 BLAS 实现

## 备注
- 本分类（ml-infra）为新增分类，用于收纳推理 / 内核 / 训练基础设施项目
