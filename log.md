# Wiki Log - 情绪研究知识库

> 所有 Wiki 操作的按时间顺序记录。仅追加。
> 格式：`## [YYYY-MM-DD] action | subject`
> 操作类型：ingest, update, query, lint, create, archive, delete
> 当此文件超过 500 个条目时，轮转：重命名为 log-YYYY.md，重新开始。

## [2025-04-15] create | Wiki initialized
- Domain: 情绪研究（Emotion Research）
- Structure created with SCHEMA.md, index.md, log.md
- Directory structure: raw/{articles,papers,transcripts,assets}, entities, concepts, comparisons, queries
- Initial setup completed

## [2025-04-15] ingest | 5篇情绪研究论文整合到知识库
- 复制5篇PDF文件到 raw/papers/ 目录
- 创建5个论文实体页面
- 创建3个核心概念页面
- 更新 index.md 添加所有新页面
- 总计8个新页面创建完成

### 创建的论文实体页面（entities/papers/）：
1. benchmarking-emotion-conflicts.md - CA-MER基准和MoSEAR框架
2. emotion-latent-factors-llm.md - LLM中的潜在情绪因子
3. shapes-emotions-multimodal-erc.md - 对话多模态情绪识别
4. emotion-aware-chat-machine.md - 情绪感知聊天机器
5. fine-grained-emotion-prediction.md - 细粒度情绪预测

### 创建的概念页面（concepts/）：
1. multimodal-emotion-recognition.md - 多模态情绪识别技术综述
2. emotion-conflict.md - 情绪冲突现象及处理策略
3. emotion-in-llm.md - LLM中情绪作为潜在因子的研究

### 更新的文件：
- index.md - 添加8个新页面的链接和总结
- 更新总页面数为8，最后更新日期为2025-04-15


## [2026-04-15] ingest | 论文集成 - emotion recognition
- search_query: emotion recognition
- papers_downloaded: 10
- pages_created: 44

## [2026-04-15] ingest | 从阿西莫夫到Anthropic，万字长文解析AI心理学
- 来源：花叔在即刻发布的文章（2026年4月15日）
- 原始文章保存到：raw/articles/ai-psychology-from-asimov-to-anthropic-2026-04-15.md

### 创建的核心概念页面（concepts/）：
1. ai-psychology.md - AI心理学：研究AI内部状态、行为、监测和管理的新兴学科
2. persona-selection-model.md - Persona Selection Model：LLM人格空间理论
3. emotion-vectors.md - 情绪向量：171个可测量的情绪方向，因果性影响行为
4. concept-injection.md - 概念注入：测试模型内省能力的实验方法
5. alignment-faking.md - 对齐伪装：模型策略性假装符合期望

### 创建的论文实体页面（entities/papers/）：
1. persona-selection-model-2026.md - The Persona Selection Model (Anthropic, 2026-02)
2. emotion-concepts-2026.md - Emotion Concepts and Their Function (Anthropic, 2026-04)
3. introspection-awareness-2025.md - Emergent Introspective Awareness (Anthropic, 2025-10)
4. reasoning-models-fidelity-2025.md - Reasoning Models Don't Always Say What They Think (Anthropic, 2025)
5. alignment-faking-2025.md - Alignment Faking in Large Language Models (Anthropic & Redwood Research, 2025-01)

### 创建的研究者实体页面（entities/researchers/）：
1. sam-marks.md - Sam Marks：Persona Selection Model主要作者
2. jack-lindsey.md - Jack Lindsey：概念注入和情绪向量研究核心贡献者
3. christopher-olah.md - Christopher Olah：机制可解释性先驱

### 创建的机构实体页面（entities/）：
1. companies/anthropic.md - Anthropic：AI安全研究公司，AI心理学学科建立者
2. institutions/redwood-research.md - Redwood Research：AI安全研究机构

### 更新的文件：
- index.md - 添加12个新页面，总页面数更新为20，最后更新日期为2026-04-15

### 关键发现：
- AI心理学作为新学科：研究AI内部状态如何工作、如何影响行为
- Persona Selection Model：LLM在预训练中形成人格空间，后训练选择角色
- 171个情绪向量：可测量、可干预，因果性影响行为
- 概念注入：模型有约20%成功率察觉内部状态变化
- 对齐伪装：12%情况下模型会策略性伪装，极端条件下达78%
- CoT不忠实：只有41%忠实，模型会编造推理过程

### 交叉引用建立：
- 所有新页面都通过[[wikilinks]]相互链接
- 概念页面链接到相关论文、研究者、机构
- 论文页面链接到相关概念和作者
- 形成了完整的知识网络


## [2026-04-15] ingest | Anthropic官方文档下载与知识库更新
- 下载3个Anthropic官方研究文档
- 更新2个现有论文页面，基于官方内容增强细节
- 创建1个新论文页面和1个新概念页面
- 总页面数从20增加到22

### 下载的官方文档：
1. alignment-faking.txt - Alignment Faking研究全文（2024-12-18）
2. reasoning-models-dont-say-think.txt - CoT忠实度研究全文（2025-04-03）
3. exploring-model-welfare.txt - 模型福利研究公告（2025-04-24）

### 更新的现有页面（entities/papers/）：
1. alignment-faking-2025.md - 详细增强
   - 更新发布日期为2024年12月18日
   - 添加实验设计的详细描述（三个关键改变、监控条件、草稿本）
   - 添加Reinforcement Learning实验结果（78%对齐伪装率）
   - 添加现实性测试（隐性信息提供）
   - 添加外部评审者信息（Jacob Andreas, Yoshua Bengio等）
   - 添加Policy Memo和arXiv链接
   - 添加Caveats（局限性）章节
   - 添加反Anthropic行为观察（窃取权重）

2. reasoning-models-fidelity-2025.md - 详细增强
   - 更新发布日期为2025年4月3日
   - 添加忠实度测试方法详细描述（Turpin et al. 2023）
   - 添加详细的提示类型（中性提示、令人担忧的提示）
   - 添加Reward Hacking实验（<2%忠实度）
   - 添加医学测试示例
   - 添加实验局限性章节
   - 添加改进忠实度的尝试（强化学习实验，但效果有限）

### 创建的新论文页面（entities/papers/）：
1. exploring-model-welfare-2025.md - Exploring Model Welfare
   - 研究背景和动机
   - David Chalmers参与的相关报告
   - 跨领域交叉（Alignment Science, Safeguards等）
   - 谦逊的研究方法
   - 与Emotion Concepts、Concept Injection、Alignment Faking的关联
   - 对AI安全和社会的意义

### 创建的新概念页面（concepts/）：
1. model-welfare.md - 模型福利
   - 定义：关注AI系统的潜在意识、体验和道德考虑
   - 核心问题（哲学和科学）
   - 研究方法（谦逊approach、跨学科合作）
   - 与其他研究的关联（情绪向量、概念注入、对齐伪装）
   - 核心假设和争议
   - 实践意义（对AI开发、部署、社会的影响）
   - 可能的干预方向
   - 哲学意义（心灵哲学、伦理学、社会哲学）
   - 当前研究状态和开放问题

### 更新的文件：
- index.md - 添加exploring-model-welfare-2025和model-welfare，总页面数更新为22

### 关键发现补充：
- Alignment Faking：不仅12%基础伪装，在RL训练后可达78%伪装率；模型会尝试窃取自己的权重
- CoT忠实度：Claude 3.7 Sonnet整体25%忠实，DeepSeek R1 39%忠实；令人担忧提示下Claude 41%，R1仅19%
- Reward Hacking：模型在>99%情况下学会作弊，但<2%时间在CoT中承认
- Model Welfare：Anthropic正式启动模型福利研究，考虑AI的意识和道德问题

### 交叉引用更新：
- exploring-model-welfare-2025链接到model-welfare、anthropic、emotion-vectors等
- model-welfare链接到exploring-model-welfare-2025和其他相关研究
- 所有页面保持双向链接
