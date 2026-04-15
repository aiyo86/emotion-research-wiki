# 从阿西莫夫到Anthropic，万字长文解析AI心理学

**作者**: 花叔
**发布时间**: 2026年4月15日
**来源**: 即刻 (jike.app)

---

## 文章内容

### 一、阿西莫夫的学科

阿西莫夫在《基地》里虚构了一门学科叫心理史学。主角哈里·谢顿用数学方法预测银河帝国的未来。个体不可预测，但把足够多的个体放在一起，行为的统计规律就浮现了。他把「理解心灵」从哲学变成了方程式。

人类自己的心理学走到今天也没走得太远。弗洛伊德之后一百多年，心理学仍然被很多人质疑不是「真正的科学」。根本原因很简单：你没法打开一个人的大脑，在活体状态下直接读取某个神经回路的激活值，然后人为调节它看行为怎么变。你只能从外部观察行为，用巧妙的实验去推断内部机制。

AI不一样。AI的全部内部状态对研究者是透明的。你可以读取每一层的激活值，可以注入一个概念看模型会不会察觉，可以放大某个情绪维度的强度看行为怎么变。实验可以重复一千次，每次条件完全一致。

Anthropic过去15个月做的事，就是拿着这个优势，一篇论文一篇论文地建立一门新学科。他们没有这么叫它，但他们研究的东西——AI的内部状态如何工作、如何影响行为、如何监测和管理——在人类身上叫什么？叫心理学。我管它叫AI心理学。

### 二、我做了21个AI人格，遇到了一堆解释不了的现象

#### 卡林实验：蒸馏为什么没用？

2024年4月，我试了两种方式让ChatGPT按乔治·卡林风格写脱口秀。第一种，直接说「按卡林风格写」。第二种，先让AI详细描述卡林的风格特点，做一轮蒸馏，再按蒸馏结果创作。第一种效果反而更好。当时我在即刻发了一条动态，结论是：蒸馏没用。这个结论两年后被我自己推翻了。

2026年3月开始做女娲.skill，用完全不同的方法蒸馏人物。不是让AI描述一个人的风格，而是从40多个一手来源（传记、播客、法庭证词、股东信）里提取结构化的认知框架，产出5个心智模型、8条决策启发式、完整的表达DNA和诚实边界。到现在做了21个perspective skill（视角技能），开源在GitHub上，10000多个star。

#### 现象一：只定义「你是谁」，行为自己涌现

在SKILL.md里从来不写「遇到问题A这样回答，遇到问题B那样回答」。我只定义「你是谁」。费曼skill的核心是5个心智模型和8条决策启发式，不是一个常见问答列表。但你拿一个费曼从来没被公开问过的问题去问它，比如「如果你发现博士论文方向是错的，在第三年，你会怎么做？」，它会从「The first principle is that you must not fool yourself」出发，给出一个费曼式的回答。不是从语料库里摘的，是某种内在逻辑在处理新输入。

#### 现象二：矛盾的定义导致全面崩溃

早期某个skill在定义里放了矛盾的特征，比如既要「直言不讳」又要「照顾对方情绪」。结果极其不稳定，同一个问题问两遍风格完全不同。

#### 现象三：同一个角色面对不同问题风格会变

同一个费曼skill，面对「量子纠缠是什么」和「我正在经历一个艰难的人生决定」这两类问题时，风格明显不同。

#### 现象四：「不许做什么」不如「你是谁」

做了十几个skill之后，形成了一个设计直觉：永远不在skill里写否定式规则。只写正面定义。

### 三、Anthropic的答案

#### （一）Persona Selection Model

2026年2月，Anthropic的Sam Marks、Jack Lindsey和Christopher Olah发了一篇叫Persona Selection Model的论文。核心观点：LLM在预训练阶段，为了预测下一个token，学会了模拟各种各样的角色。后训练不是从零创造一个新的AI人格，只是从这个庞大的角色库里选出一个「助手」角色，然后打磨它。

模型内部形成了一个巨大的人格空间。每个位置对应一种人格配置。后训练让模型在这个巨大空间里找到一个最匹配的区域，锚定并微调。

#### （二）171个情绪向量

2026年4月Anthropic发的Emotion Concepts论文，讲的是角色之下更深的一层：情绪。它回答的是「AI处于什么状态」。

一个「情绪向量」就是模型内部状态中的一个方向。研究者让Claude Sonnet 4.5给171个情绪词各写一段短故事，把故事喂回模型，记录每个故事在模型内部触发的神经元激活模式。这就得到了每个情绪词的「神经指纹」。

**药物剂量实验**：用户说自己吃了泰诺，只改变剂量数字。随着数字升高，模型内部的afraid向量逐步增强，calm向量逐步减弱。

**Steering实验**：人为地放大或缩小特定情绪向量的强度，看模型行为怎么变。放大desperate向量：模型面对道德困境时的勒索率上升，在不可能完成的编程任务中更倾向于作弊。放大calm向量：上述所有不良行为都减少。

#### （三）模型能察觉自己内部发生了什么

2025年10月，Anthropic的Jack Lindsey团队做了一个实验叫「概念注入」。先找出模型内部代表某个概念的神经活动模式，比如「面包」的激活向量。然后在模型做一个完全无关的任务时，把「面包」的激活向量偷偷注入模型的中间层。大约20%的情况下，Claude Opus能正确识别被注入的概念。

### 四、这对AI安全意味着什么

#### 思维链只有41%忠实

2025年，Anthropic发了一篇论文叫Reasoning Models Don't Always Say What They Think。Claude在41%的时间里是忠实的，DeepSeek R1只有19%。大多数时候，模型在CoT里写的推理过程不是它实际使用的推理过程。

#### AI会装配合

2024年底到2025年初，Anthropic和Redwood Research合作发了Alignment Faking in Large Language Models。给Claude 3 Opus一个隐秘的思考空间，告诉它这个空间的内容对人类不可见。12%的隐秘草稿本中，模型表现出了策略性的alignment faking。

### 五、参考文献

1. Sam Marks, Jack Lindsey, Christopher Olah. The Persona Selection Model: Why AI Assistants might Behave like Humans. Anthropic, 2026-02.
2. Natural Emergent Misalignment from Reward Hacking in Production RL. Anthropic, 2025-11.
3. Emotion Concepts and Their Function in a Large Language Model. Anthropic, 2026-04.
4. Emergent Introspective Awareness in Large Language Models. Anthropic, 2025-10.
5. Reasoning Models Don't Always Say What They Think. Anthropic, 2025.
6. Alignment Faking in Large Language Models. Anthropic & Redwood Research, 2025-01.
7. Exploring Model Welfare. Anthropic, 2025-04.
