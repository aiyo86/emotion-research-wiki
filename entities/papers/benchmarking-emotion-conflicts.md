---
title: Benchmarking and Bridging Emotion Conflicts for Multimodal Emotion Reasoning
created: 2025-04-15
updated: 2025-04-15
type: entity
tags: [paper, multimodal, emotion-recognition, emotion-conflict, mllm, benchmark, fusion]
sources: [raw/papers/2508.01181v2_Benchmarking_and_Bridging_Emotion_Conflicts.pdf]
related: [[MoSEAR框架]], [[CA-MER基准]], [[多模态情绪识别]]
---

# Benchmarking and Bridging Emotion Conflicts for Multimodal Emotion Reasoning

## 基本信息

- **arXiv ID**: [2508.01181v2](https://arxiv.org/abs/2508.01181v2)
- **发布日期**: 2025年8月2日
- **分类**: cs.AI, cs.CV, cs.MM, cs.SD, eess.AS
- **文件**: `raw/papers/2508.01181v2_Benchmarking_and_Bridging_Emotion_Conflicts.pdf`

## 作者

- [[Zhiyuan Han]]
- [[Beier Zhu]]
- [[Yanlong Xu]]
- [[Peipei Song]]
- [[Xun Yang]]

## 研究亮点

### 问题提出
现有[[多模态大语言模型]]（MLLMs）在多模态情绪推理中表现强劲，但往往忽略情绪冲突场景，即不同模态的情绪信号不一致的情况。

### CA-MER基准测试
引入了CA-MER（Conflict-Aware Multimodal Emotion Reasoning）基准测试，包含三个子集：
- **video-aligned**: 视频对齐，只有视觉模态反映真实情绪
- **audio-aligned**: 音频对齐，只有音频模态反映真实情绪  
- **consistent**: 一致，所有模态都反映真实情绪

### 关键发现
评估发现当前最先进的情绪MLLMs在情绪冲突时**系统性过度依赖音频信号**，忽视了视觉模态的关键线索。

### MoSEAR框架
提出MoSEAR（Modality-Specific Experts with Attention Reallocation）框架，包含两个模块：

1. **MoSE（Modality-Specific Experts）**
   - 模态特定专家网络
   - 正则化门控机制
   - 减少微调头部的模态偏差

2. **AR（Attention Reallocation）**
   - 注意力重分配机制
   - 在推理时重新平衡冻结骨干网络的模态贡献

### 框架优势
- 缓解情绪冲突问题
- 提高一致样本的性能
- 在音频和视觉模态之间无权衡

## 实验结果

在多个基准测试上取得最先进性能：
- [[MER2023]]
- [[EMER]]
- [[DFEW]]
- [[CA-MER]]（新基准）

特别是在模态冲突条件下表现优异。

## 应用价值

- **视频分析**: 改善视频情绪理解的鲁棒性
- **情感计算**: 提供更可靠的多模态情绪分析
- **人机交互**: 增强AI系统对冲突情绪信号的理解
- **多模态学习**: 为其他多模态任务提供框架参考

## 技术贡献

1. **新基准**: CA-MER填补了情绪冲突评估的空白
2. **问题发现**: 揭示了现有MLLMs的音频偏差问题
3. **解决方案**: MoSEAR提供了有效的模态平衡方法
4. **实用价值**: 框架可应用于其他多模态任务

## 相关研究

- 多模态融合技术
- 注意力机制在情感计算中的应用
- 情绪冲突检测与处理
- 模态特定专家网络

## 未来方向

- 扩展到更多模态组合
- 研究其他类型的模态冲突
- 探索在不同应用场景中的适应性
- 结合更复杂的注意力机制

---

**论文链接**: https://arxiv.org/abs/2508.01181v2
**PDF**: `raw/papers/2508.01181v2_Benchmarking_and_Bridging_Emotion_Conflicts.pdf`
