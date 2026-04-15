---
title: Shapes of Emotions: Multimodal Emotion Recognition in Conversations via Emotion Shifts
created: 2025-04-15
updated: 2025-04-15
type: entity
tags: [paper, multimodal, emotion-recognition, emotion-shift, dialogue, erc, conversation]
sources: [raw/papers/2112.01938v2_Shapes_of_Emotions_Multimodal_Emotion_Recognition.pdf]
related: [[情绪转移]], [[对话情绪识别]], [[MOSEI数据集]], [[IEMOCAP数据集]]
---

# Shapes of Emotions: Multimodal Emotion Recognition in Conversations via Emotion Shifts

## 基本信息

- **arXiv ID**: [2112.01938v2](https://arxiv.org/abs/2112.01938v2)
- **发布日期**: 2021年12月3日
- **分类**: cs.CL, cs.AI, cs.LG
- **文件**: `raw/papers/2112.01938v2_Shapes_of_Emotions_Multimodal_Emotion_Recognition.pdf`

## 作者

- [[Harsh Agarwal]]
- [[Keshav Bansal]]
- [[Abhinav Joshi]]
- [[Ashutosh Modi]]

## 研究背景

### 问题提出
[[对话情绪识别]]（ERC）是一个重要任务，但现有方法忽略了对话中情绪的动态变化特性。情绪不是静态的，而是随着对话进展而变化。

### 核心挑战
- 情绪的连续变化：对话中情绪会逐步转移
- 上下文依赖：当前情绪受历史情绪影响
- 多模态融合：需要整合文本、音频、视觉信息

## 研究创新

### 情绪转移组件（Emotion Shift Component）
提出情绪转移组件，专门捕捉对话中情绪的连续变化：
- 建模情绪之间的转移关系
- 保持情绪变化的连续性
- 避免情绪预测的突变

### 组件化设计
- 模块化设计，可添加到任何现有的多模态ERC模型
- 不需要重新训练整个模型
- 兼容性强，易于集成

## 技术方法

### 情绪转移建模
```
E_t = f(E_{t-1}, E_{t-2}, ..., Context_t, Multimodal_t)
```
其中：
- E_t: 当前时刻的情绪
- E_{t-1}, E_{t-2}: 历史情绪
- Context_t: 对话上下文
- Multimodal_t: 当前时刻的多模态输入

### 多模态融合
- **文本**: 使用预训练语言模型提取特征
- **音频**: 使用音频特征提取器
- **视觉**: 使用视觉特征提取器
- 融合策略：注意力机制或简单拼接

## 实验结果

### 数据集
- [[MOSEI]]: 多模态情感强度数据集
- [[IEMOCAP]]: 交互式情感二元动作数据集

### 性能表现
在两个数据集上都取得了最先进（SOTA）性能：
- 准确率显著提升
- 情绪分类的F1分数提高
- 特别在情绪转移场景下表现优异

### 消融实验
- 证明情绪转移组件的有效性
- 展示多模态融合的重要性
- 分析不同配置的性能差异

## 应用价值

### 对话系统
- 理解对话中的情绪变化
- 生成情绪合适的回复
- 改善人机对话体验

### 情感分析
- 实时检测对话情绪
- 分析情绪转移模式
- 提供情感洞察

### 心理健康
- 监测患者的情绪变化
- 辅助心理健康评估
- 早期发现情绪异常

## 技术优势

1. **捕捉动态变化**: 专门建模情绪转移，而非静态分类
2. **多模态融合**: 充分利用文本、音频、视觉信息
3. **模块化设计**: 易于集成到现有系统
4. **性能优异**: 在多个数据集上达到SOTA

## 相关概念

- **情绪转移**（Emotion Shift）: 情绪从一个状态到另一个状态的变化过程
- **对话情绪识别**（ERC）: 识别对话中每个发言者的情绪
- **多模态融合**（Multimodal Fusion）: 整合多种模态的信息
- **上下文建模**（Context Modeling）: 考虑历史信息对当前预测的影响

## 局限性

- 依赖高质量的多模态数据
- 计算复杂度较高
- 对长对话的处理可能不够有效

## 未来方向

- 更高效的情绪转移建模
- 跨语言对话情绪识别
- 少样本学习场景
- 实时情绪转移检测

---

**论文链接**: https://arxiv.org/abs/2112.01938v2
**PDF**: `raw/papers/2112.01938v2_Shapes_of_Emotions_Multimodal_Emotion_Recognition.pdf`
