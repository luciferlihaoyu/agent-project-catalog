# OpenBMB/VoxCPM

> 仓库：https://github.com/OpenBMB/VoxCPM · ⭐ 40,257（2026-10-24 API 实测） · Python · License: Apache-2.0

**一句话：** VoxCPM2: Tokenizer-Free TTS for Multilingual Speech Generation, Creative Voice Design, and True-to-Life Cloning. —— 面壁智能（OpenBMB）开源的 **tokenizer-free** 语音合成系统，绕过离散 tokenization，直接用端到端 **diffusion autoregressive** 架构生成连续语音表征。

## 核心能力
- **2B 参数**模型，训练数据 **超 200 万小时**多语言语音，基于 [MiniCPM-4](https://github.com/OpenBMB/MiniCPM) 骨干
- **30 种语言**直接合成，无需打语言标签：中文、英文、日、韩、俄、法、德、西、葡、阿拉伯、印地、希伯来、越南、泰、印尼等
- **中文方言**：四川话、粤语、吴语、东北话、河南话、陕西话、山东话、天津话、闽南话
- **Voice Design**：仅凭自然语言描述（性别/年龄/语气/情绪/语速）造出全新声音，**无需参考音频**
- **Controllable Cloning**：短参考片段克隆音色 + 可选风格引导（情绪/语速/表现力）
- **Ultimate Cloning**：参考音频 + 对应转写文本，模型从参考处无缝续说，忠实保留音色/节奏/情绪/风格
- **48kHz 录音棚音质**：接受 16kHz 参考音频，AudioVAE V2 非对称编解码 + 内建超分，无需外挂 upsampler
- **Context-Aware Synthesis**：从文本内容自动推断合适的韵律与表现力
- **实时流式**：RTF 低至 ~0.3（RTX 4090）；经 [Nano-vLLM](https://github.com/a710128/nanovllm-voxcpm) 或 [vLLM-Omni](https://github.com/vllm-project/vllm-omni) 加速至 ~0.13
- **完全开源可商用**：权重 + 代码 Apache-2.0

## 关键数据（2026-10-24 API 实测）
| 项 | 值 |
|---|---|
| ⭐ Stars | 40,257（今日 +150） |
| 🍴 Forks | 4,579 |
| Open Issues | 146 |
| 仓库体积 | 4.2 MB |
| 创建时间 | 2025-09-16 |
| 最后推送 | 2026-10-08T03:26:41Z |
| 主页 | https://voxcpm.com |
| 技术报告 | https://arxiv.org/abs/2606.06928 |
| 权重 | [HuggingFace](https://huggingface.co/openbmb/VoxCPM2) / [ModelScope](https://modelscope.cn/models/OpenBMB/VoxCPM2) |

## 适用场景
- 中文场景的本地化 TTS 替代方案（对标 ElevenLabs）
- 有声书 / 视频配音 / 游戏语音批量生成
- 隐私敏感场景：权重 + 代码全开源，权重 Apache-2.0 可自行托管推理
- 音频数据集 / 解码器研究的基线模型

## 为什么值得关注
- **"Tokenizer-free" 是一次路线级选择，不是营销词**。主流 TTS（VALL-E 系、AudioLM 系）都把语音离散成 token 再自回归生成，好处是能复用 LLM 架构，代价是量化损失 + 解码器失真。VoxCPM 直接在连续潜空间做 diffusion autoregressive，绕开这一步。**用 2B 参数 + 200 万小时数据达到 48kHz 录音棚音质**，说明这条路线在中小模型规模上是成立的——这对想自己做 TTS 而不想背 Llama-级别算力开销的团队是重大信号。
- **本地 TTS 生态在快速成熟**。本 catalog 里已有 `debpalash/VoiceStudio`（83,354 星 / AGPL-3.0，646 语言的本地 ElevenLabs 替代品）—— 两者规模接近但协议相反：VoiceStudio 是 AGPL，VoxCPM 是 **Apache-2.0**。**要商用、要改、要闭源分发，Apache-2.0 的 VoxCPM 是更省心的那个**，这是它 4,579 fork 率和大量商业集成的关键原因。
- **和已归档的 `ml-infra` / `vllm-project/vllm` 形成了完整推理链路**：VoxCPM 权重 → vLLM-Omni 提供 PagedAttention + OpenAI 兼容 API 部署。**这是本期唯一一个"模型 + 推理引擎 + 协议"三层都齐的 TTS 项目**，落地成本极低。
- ⚠️ 关注理由：仓库最后推送 2026-10-08，v2 大版本发布后更新节奏放缓；2B 模型的 48kHz 输出在长文本连贯性和情感一致性上仍需按自己的业务场景实测（README 提供的 [DemoPage](https://openbmb.github.io/voxcpm2-demopage/) 有音频样例可先听）。

## 参考资料
1. [GitHub 仓库](https://github.com/OpenBMB/VoxCPM)
2. [中文 README](https://github.com/OpenBMB/VoxCPM/blob/main/README_zh.md)
3. [技术报告 arXiv:2606.06928](https://arxiv.org/abs/2606.06928)
4. [HuggingFace 模型页](https://huggingface.co/openbmb/VoxCPM2)
5. [在线 Demo 音频样例](https://openbmb.github.io/voxcpm2-demopage/)
6. [HuggingFace Space 实时体验](https://huggingface.co/spaces/OpenBMB/VoxCPM-Demo)
7. [配套：debpalash/VoiceStudio](../AI-语音合成-本地化工具/VoiceStudio.md)
