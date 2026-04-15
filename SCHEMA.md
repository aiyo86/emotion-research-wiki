# Wiki Schema - 情绪研究知识库

## Domain

情绪研究的完整知识库，包括：
- 情绪识别与检测技术
- 多模态情绪分析
- 情感计算理论与方法
- 情绪数据集与基准测试
- 情绪相关模型与算法
- 情绪应用场景与案例
- 研究者、机构与项目
- 情绪在AI系统中的应用

## Conventions

### 文件命名
- 使用小写字母
- 单词之间用连字符 `-` 连接
- 不使用空格
- 示例：`multimodal-emotion-recognition.md`, `mosei-dataset.md`

### Frontmatter（必需）
每个 Wiki 页面必须包含 YAML frontmatter：

```yaml
---
title: 页面标题
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [从下方标签分类中选择]
sources: [raw/papers/paper-name.md]
related: [[相关页面1]], [[相关页面2]]
contradictions: [] # 如果有矛盾信息，列出冲突页面
---
```

## Tag Taxonomy（标签分类）

### 核心概念
- `emotion` - 情绪理论、情绪模型
- `affective-computing` - 情感计算
- `sentiment` - 情感分析
- `emotion-recognition` - 情绪识别
- `emotion-detection` - 情绪检测
- `emotion-classification` - 情绪分类

### 技术方法
- `multimodal` - 多模态融合
- `transformer` - Transformer架构
- `cnn` - 卷积神经网络
- `rnn` - 循环神经网络
- `attention` - 注意力机制
- `fusion` - 多模态融合
- `transfer-learning` - 迁移学习
- `fine-tuning` - 微调
- `self-supervised` - 自监督学习

### 数据类型
- `text` - 文本数据
- `audio` - 音频数据
- `video` - 视频数据
- `image` - 图像数据
- `physiological` - 生理信号
- `facial-expression` - 面部表情
- `speech` - 语音
- `gestures` - 手势

### 应用领域
- `healthcare` - 医疗健康
- `education` - 教育学习
- `finance` - 金融投资
- `social-media` - 社交媒体
- `gaming` - 游戏娱乐
- `human-computer-interaction` - 人机交互
- `mental-health` - 心理健康
- `customer-service` - 客户服务

### 任务类型
- `classification` - 分类任务
- `regression` - 回归任务
- `generation` - 生成任务
- `reasoning` - 推理任务
- `prediction` - 预测任务
- `dialogue` - 对话系统

### 评估指标
- `accuracy` - 准确率
- `f1-score` - F1分数
- `precision` - 精确率
- `recall` - 召回率
- `auc` - ROC曲线下面积
- `mse` - 均方误差
- `mae` - 平均绝对误差

### 模型类型
- `llm` - 大语言模型
- `mllm` - 多模态大语言模型
- `multimodal-model` - 多模态模型
- `emotion-model` - 专用情绪模型
- `foundation-model` - 基础模型

### 数据集与基准
- `dataset` - 数据集
- `benchmark` - 基准测试
- `corpus` - 语料库
- `evaluation` - 评估方法

### 研究者与机构
- `researcher` - 研究者
- `institution` - 研究机构
- `lab` - 实验室
- `company` - 公司
- `open-source` - 开源项目

### 特殊主题
- `emotion-conflict` - 情绪冲突
- `emotion-shift` - 情绪转移
- `cross-modal` - 跨模态
- `fine-grained` - 细粒度
- `real-time` - 实时
- `cross-lingual` - 跨语言

## Page Thresholds

- **创建实体页面** 当一个实体（研究者、机构、数据集、模型）在2+来源中提及，或对1个来源至关重要
- **创建概念页面** 当一个概念/主题在2+来源中讨论，或需要详细解释
- **添加到现有页面** 当新信息扩展已存在的实体/概念
- **不创建页面** 对于一次性提及、次要细节、领域外的内容
- **拆分页面** 当页面超过200行时，拆分为子主题并交叉链接
- **归档页面** 当内容完全被新内容取代时，移至 `_archive/`，从索引中移除

## Entity Pages

实体页面每个重要实体一个页面，包括：

### 研究者页面
- 个人简介和背景
- 主要研究领域
- 代表性论文
- 学术影响
- 相关实体（合作者、机构）

### 机构/实验室页面
- 机构介绍
- 主要研究项目
- 重要成果
- 相关研究者

### 数据集页面
- 数据集描述
- 数据规模和来源
- 标注方式
- 评估任务
- 使用情况和引用

### 模型页面
- 模型架构
- 训练方法和数据
- 性能表现
- 优势和局限
- 应用场景
- 相关模型对比

## Concept Pages

概念/主题页面，包括：
- 定义和解释
- 当前知识状态
- 开放问题和争议
- 相关概念（[[wikilinks]]）
- 研究进展时间线

## Comparison Pages

对比分析页面，包括：
- 对比对象和原因
- 对比维度（表格格式优先）
- 结论或综合
- 数据来源
- 争议点

## Update Policy

当新信息与现有内容冲突时：

1. **检查日期** - 较新的来源通常覆盖较旧的来源
2. **记录矛盾** - 如果真正矛盾，注明两个观点及其日期和来源
3. **标记矛盾** - 在 frontmatter 中标记：`contradictions: [page-name]`
4. **用户审查** - 在 lint 报告中标记供用户审查

## Cross-Reference Rules

- 每个新页面必须通过 `[[wikilinks]]` 链接到至少2个其他页面
- 检查现有页面是否需要反向链接
- 优先链接到已存在的实体和概念页面
- 避免孤立页面（无入链）

## File Organization

### raw/ 目录规则
- `raw/articles/` - 网络文章、博客、新闻报道
- `raw/papers/` - 学术论文、技术报告
- `raw/transcripts/` - 会议记录、访谈、演讲
- `raw/assets/` - 图片、图表、音频、视频

**重要**：raw/ 中的文件是只读的，代理永远不会修改这些文件。所有更正和注释都应在 Wiki 页面中进行。

## Index Management

- 每个新页面必须添加到 `index.md` 的正确部分，按字母顺序排列
- 更新索引头部的 "Total pages" 数量和 "Last updated" 日期
- 当任何部分超过50个条目时，按首字母或子域拆分为子部分
- 当索引超过200个条目时，创建 `_meta/topic-map.md` 按主题分组

## Log Management

- 每次操作必须追加到 `log.md`
- 格式：`## [YYYY-MM-DD] action | subject`
- 操作类型：ingest, update, query, lint, create, archive, delete
- 当 log.md 超过500条目时，轮转：重命名为 log-YYYY.md，重新开始

## Language and Style

- 主要使用中文，保留关键术语的英文原文
- 使用专业但易懂的语言
- 保持页面简洁，30秒内可读完
- 使用清晰的结构和标题
- 提供实际例子和案例

## Quality Standards

- **准确性**：信息必须准确，有来源支持
- **完整性**：重要信息不遗漏
- **一致性**：术语和格式统一
- **时效性**：定期更新过时信息
- **可读性**：清晰、结构化、易于理解
