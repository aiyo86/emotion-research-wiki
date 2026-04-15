# 情绪研究知识库 (Emotion Research Knowledge Base)

这是一个基于 [[llm-wiki]] 方式构建的情绪研究知识库，专注于情绪识别、情感计算、多模态情绪分析等领域的研究。

## 📚 知识库概述

本知识库遵循 Karpathy's LLM Wiki 模式，将情绪研究领域的研究成果、技术方法、应用案例等知识整理成相互关联的 Markdown 文件。

### 知识库特点

- **结构化**: 三层架构（Raw → Wiki → Schema）
- **可扩展**: 模块化设计，便于添加新内容
- **可搜索**: 通过索引和 wikilinks 快速导航
- **可维护**: 清晰的约定和规范
- **可协作**: 标准 Markdown 格式，适合团队协作

## 🗂️ 知识库结构

```
emotion-research-wiki/
├── SCHEMA.md              # 领域架构定义和约定
├── index.md               # 内容目录
├── log.md                 # 操作日志
├── README.md              # 本文件
├── .gitignore             # Git 忽略规则
├── raw/                   # 原始资料（不可变）
│   ├── articles/          # 文章、博客
│   ├── papers/            # 学术论文（PDF）
│   ├── transcripts/       # 会议记录、访谈
│   └── assets/            # 图片、音频、视频
├── entities/              # 实体页面
│   ├── papers/            # 论文实体
│   ├── researchers/       # 研究者
│   ├── institutions/      # 研究机构
│   └── datasets/          # 数据集
├── concepts/              # 概念页面
├── comparisons/           # 对比分析
└── queries/               # 查询结果
```

## 🏷️ 标签体系

知识库包含 10 大标签分类，60+ 个标签：

- **核心概念**: emotion, affective-computing, sentiment
- **技术方法**: multimodal, transformer, fusion
- **数据类型**: text, audio, video, image
- **应用领域**: healthcare, education, social-media
- **任务类型**: classification, generation, dialogue
- **评估指标**: accuracy, f1-score, precision
- **模型类型**: llm, mllm, multimodal-model
- **数据集与基准**: dataset, benchmark, corpus
- **研究者与机构**: researcher, institution, lab
- **特殊主题**: emotion-conflict, cross-modal, fine-grained

## 📊 当前内容

### 统计信息
- **总页面数**: 8 个
- **论文实体**: 5 篇
- **概念页面**: 3 个
- **标签体系**: 60+ 标签

### 主要内容
- 多模态情绪识别技术综述
- 情绪冲突现象及处理策略
- LLM中的情绪作为潜在因子研究
- 5篇重要论文的详细分析

## 🚀 快速开始

### 使用 Obsidian 打开
1. 安装 [Obsidian](https://obsidian.md/)
2. 将此目录设置为 Obsidian Vault
3. 启用 Graph View 查看知识网络
4. 使用 wikilinks `[[页面名]]` 在页面间导航

### 使用 VS Code 打开
1. 用 VS Code 打开此目录
2. 安装 Markdown Preview Enhanced 插件
3. 使用 Ctrl+K Ctrl+V 预览 Markdown

### 查看知识库
- 从 `index.md` 开始浏览所有页面
- 查看 `SCHEMA.md` 了解领域约定
- 查看 `log.md` 了解更新历史

## 📖 贡献指南

### 添加新内容
1. 遵循 `SCHEMA.md` 中的约定
2. 使用标准的 YAML frontmatter
3. 添加适当的标签
4. 创建 wikilinks 到至少 2 个其他页面
5. 更新 `index.md` 和 `log.md`

### 页面创建规则
- **实体页面**: 当实体在 2+ 来源中提及，或对 1 个来源至关重要
- **概念页面**: 当概念在 2+ 来源中讨论，或需要详细解释
- **页面大小**: 超过 200 行时拆分为子主题
- **交叉引用**: 每个页面至少链接 2 个其他页面

### Frontmatter 模板
```yaml
---
title: 页面标题
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [从标签分类中选择]
sources: [raw/路径/到/源文件.md]
related: [[相关页面1]], [[相关页面2]]
contradictions: [] # 如有矛盾信息
---
```

## 🔍 搜索和导航

### 索引搜索
- 查看 `index.md` 按类型浏览所有页面
- 使用 Ctrl+F 或 Cmd+F 搜索关键词

### Wikilinks
- 使用 `[[页面名]]` 创建链接
- 点击链接跳转到相关页面
- 利用反向链接发现关联内容

### 标签搜索
- 搜索特定标签如 `tags:multimodal`
- 按 `tags:` 前缀过滤页面

## 📚 核心研究主题

- **多模态情绪识别**: 文本、音频、视觉信息的融合
- **情绪冲突处理**: 不同模态情绪信号不一致的解决方案
- **LLM情绪建模**: 大语言模型中的情绪作为潜在因子
- **对话情绪识别**: 对话中情绪的动态变化建模
- **细粒度情绪预测**: 区分相似情绪的细微差别
- **情感对话生成**: 生成带有情感色彩的对话回复

## 🎯 应用领域

- **人机交互**: 情感化AI系统和界面
- **社交媒体**: 用户情绪分析和情感挖掘
- **心理健康**: 情绪监测和心理评估
- **教育领域**: 学生情绪识别和情感支持
- **客户服务**: 情感化客服和反馈分析
- **游戏娱乐**: 情感交互和体验设计

## 🔄 更新和维护

### 更新频率
- 定期添加最新研究论文
- 更新现有页面的事实信息
- 修正错误和改进内容质量
- 扩展标签体系和分类

### 版本控制
- 使用 Git 追踪所有变更
- 保持详细的 commit 消息
- 定期创建版本标签
- 维护变更日志

## 📞 联系方式

如有问题或建议，请通过以下方式联系：
- 创建 GitHub Issue
- 提交 Pull Request
- 联系维护者

## 📄 许可证

本项目采用 MIT 许可证。详见 LICENSE 文件。

## 🙏 致谢

- [Andrej Karpathy](https://github.com/karpathy) 的 LLM Wiki 模式
- [Hermes Agent](https://github.com/nousresearch/hermes-agent) 知识库构建工具
- 所有贡献者和研究者

---

**最后更新**: 2025-04-15  
**维护者**: Hermes Agent  
**知识库版本**: 1.0.0
