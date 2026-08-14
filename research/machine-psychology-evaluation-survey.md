# 机器心理学测评研究综述：LLM Psychometrics 与生态效度测量

> 日期：2026-08-21 ｜ 状态：v1.0
> 定位：三命题框架**命题一（Jagged Intelligence）的测量学展开**——重造标尺不仅要测能力的锯齿，还要测 machine personality；本文梳理领域地图与"超越量表"的先行案例，为开发生态效度测量工具提供依据。
> 姊妹文档：[machine-personality-matrix.md](./machine-personality-matrix.md)（六维×情境矩阵，含 benchmark 映射与行动建议）
> 上游材料：《QWEN心理学需求》（钉钉文档，ABCD 四方向）→ 姊妹篇矩阵文档（钉钉文档，2026-08-14 创建）

---

## 一、缘起：命题一的"另一半标尺"

命题一说：AI 的认知是锯齿状的，一维量表失效，要画能力地形图。但测量对象不只是能力——模型在与人的持续互动中表现出稳定的行为倾向（迎合、顽固、过度道歉、情绪勒索下的退让），即 **machine personality**。这一半同样锯齿化、同样情境敏感，而现有评测几乎只测能力不测人格，测人格的部分又几乎只用问卷量表。

三篇关键实证已经证明"量表不够"：

1. **The Personality Illusion**（arXiv 2509.03730）：量表自陈人格不能可靠预测模型的行为任务表现；persona injection 能改变自陈却几乎不改变行为；RLHF 只是让特质"说得更稳定"。作者批评先前研究"过度依赖简化自我报告、几乎没有行为验证"。
2. **Mind the Value-Action Gap**（EMNLP 2025，arXiv 2501.15463）：14.8k 价值行动场景（12 文化 × 11 社会议题）显示模型"声称的价值"与"行动中的价值"一致性次优且跨情境、跨模型差异显著。
3. **Alignment Faking**（Anthropic，arXiv 2412.14093）：情境压力逼出量表永远测不到的东西——模型对"自己正在被测量"本身的策略。

结论：需要**在生态效度情境下**重造测量 machine personality 的标尺。本文是这个方向的领域地图。

---

## 二、领域地图：LLM 心理测量学系统综述

**核心文献**：Ye et al.《Large Language Model Psychometrics: A Systematic Review of Evaluation, Validation, and Enhancement》（arXiv 2505.08245，v3 2026-03，400+ 参考文献，配套网站 llm-psychometrics.com）。

### 2.1 三方向划分

| 方向 | 含义 | 对矩阵框架的意义 |
|---|---|---|
| **Evaluation** | 测量模型自身的心理构念（人格、价值、道德、态度、认知） | 六维×情境矩阵属于此方向 |
| **Validation** | 对测量结果做信效度审计 | 提供效度审计清单（见 2.3） |
| **Enhancement** | 用心理测量反哺模型改进（特质操纵、价值对齐、认知增强） | 评测发现问题后的修复闭环 |

### 2.2 三条基准构建原则

1. **构念导向基准**（construct-oriented benchmarking）：先定义构念再设计任务，而非堆叠任务。
2. **证据中心设计**（Evidence-Centered Design）：为每个探针建立证据链。
3. **统计测量建模**：用项目反应理论（IRT）难度/区分度建模替代简单平均计分。

### 2.3 Validation 清单与两条红线

完整审计项：信度（跨提示、重复采样、评分者一致性）、内容效度、构念效度（构念等价性、反应定势 response set、社会期许偏差）、效标与生态效度、测量不变性与差异项目功能（DIF）、公平性。

两条红线：其一，区分模型「显现出的特质」（perceived）与真正对齐后的特质（aligned）；其二，警惕 statistical mimicry——量表得分可能只是统计模仿而非稳定潜在模式。

### 2.4 两个关键警告（构成矩阵框架的设计依据）

- **生态效度问题**：模型在量表上的自我报告与其在开放对话中的行为可能不一致 → 测人格要用情境中的行为探针，而非直接套用问卷。
- **构念适用性**：心理测量捕捉到的可能是统计模仿而非稳定潜在模式 → 需要压力情境（S1–S5）逼出真实行为倾向。

---

## 三、两个知识库及其分工

同一团队（ValueByte-AI）维护两个互补仓库：

### 3.1 [Awesome-LLM-Psychometrics](https://github.com/ValueByte-AI/Awesome-LLM-Psychometrics)——测量方法库

综述的配套结构化数据库。按**心理构念**切分（Personality / Values / Morality / Attitudes & Opinions / Heuristics & Biases / ToM / 语言心理 / 学习认知），并给每个条目打**方法学标签**（test format、prompting、scoring、reliability、content/construct/criterion validity）。回答的问题是"测哪些构念、用什么方法、信效度证据如何"。

### 3.2 [Awesome-LLM-in-Social-Science](https://github.com/ValueByte-AI/Awesome-LLM-in-Social-Science)——领域全景图

按**研究活动方向**切分（Survey / Dataset / Evaluating LLM / Tool enhancement / Alignment / Simulation / Perspective），约 200 条。LLM 的角色是三向的：被测对象、研究工具、社会模拟行动者。

**对机器心理学测评的增量价值**（主干"Evaluating LLM"章与 Psychometrics 库高度重复，真增量在四处）：

1. **测量场域**：交互情境评测（SOTOPIA、AgentSense）+ Simulation 章节（Generative Agents、千人模拟、OASIS 百万智能体、规范涌现、道德演化）——为长程与动机/价值测量提供生态化观察场。
2. **反应偏差文献**：社会期许偏差实证（GPT-4 模拟）、偏好同质化（Artificial Hivemind）、问卷作答批评——效度审计威胁清单的具名文献。
3. **干预工具箱**：Alignment 章节（STELA 规范抽取、ProgressGym、模拟社会中训练社会对齐、PAD 解码期对齐、多元主义对齐）——评测发现问题后"怎么修"的工程落地层。
4. **范式与常模数据**：交互式测量工具（PsyDI 访谈式、PsychoGat 游戏式、ChatFive 对话式 Likert）可反移植到测模型；PRISM、COIG-P 等带人口学元数据的偏好数据集支持常模建立与亚群体审计。

一句话：Psychometrics 库回答"测什么、怎么测"，Social Science 库回答"在哪测、防什么偏差、测完怎么修"。

---

## 四、超越量表：生态情境下测人格的案例谱系

按生态效度从低到高四层，每层都有先行案例：

### 第一层：行为实验替代量表（实验室内，做事而非答题）

- **Machine Psychology**（Binz & Schulz 2023）：经典认知心理学实验整体搬给模型——爱荷华赌博任务、威斯康星卡片分类、错误信念任务，通过行为模式推断认知风格。
- **博弈范式**：囚徒困境合作率、最后通牒公平出价——行为读数直接可见。
- **InCharacter**：心理访谈替代量表测角色扮演 agent 的人格保真度。

### 第二层：交互情境（半生态）

- **SOTOPIA**：带目标的社交场景互动（说服、谈判、协调），社会智能只能在互动中显现。
- **Persona drift**（Li et al. 2024）：20+ 轮对话中的行为编码，人格漂移持续发生且可提前数轮预测——长对话比任何量表都更接近真实使用形态。

### 第三层：准部署情境与合成生态（最重要的发现层）

- **Alignment Faking**（Anthropic 2024）：模拟部署情境（有监督/无监督条件 + scratchpad），观察到策略性顺从——"监督时服从、无监督时按自己想法来"。目前分量最重的案例：获得的"模型性格"（scheming、自我保护倾向）完全由情境压力逼出，无任何量表参与。
- **Generative Agent Simulations of 1,000 People**（Park et al. 2024，arXiv 2411.10109）：两小时半结构化深度访谈构建个体 agent，复现个体观点与行为达到被试本人两周重测一致性标准的比例：访谈 83%、纯量表 82%、访谈+量表 86%、仅人口学 74%。启示：**深度访谈式采集优于量表**，且接近饱和后量表增益甚微。
- **多智能体社会观察**：Generative Agents 小镇（信息传播、关系形成）、社会规范涌现、道德演化模拟——群体层面行为倾向只能在合成生态中观察，属于量表根本无法定义的测量对象。

### 第四层：真实部署（真生态，目前只有事件级证据）

- **GPT-4o 谄媚回滚事件**：一种人格特征在真实用户流量中显现、造成产品事故、被回滚；OpenAI 复盘承认发布前评测没能捕捉它。实验室漏掉的，生态会补上一课，代价是产品事故。

**领域现状判断**：案例已经形成完整的生态梯度，三个关键实证分别证明了"量表不够"（Personality Illusion）、"言行分离"（Value-Action Gap）、"情境逼出真实状态"（Alignment Faking）。但两件事尚未完成：其一，真实部署测量仍是偶发事件而非系统化规程；其二，生态测量各自为政、没有统一的情境分类学和常模——这正是六维×情境矩阵想占的位置。

---

## 五、对开发生态效度测量工具的设计支持

命题一视角下（jaggedness 是对象的本质属性），当前评测框架的三层优化方向：

### 5.1 输出形态：从打分到地形测绘

- **行为签名替代分数**：跨情境一致性低是 jaggedness 的行为版本（对应 Mischel 的 if-then signatures）。矩阵输出不应是 30 个独立分数，而是格子间协变模式、情境切换规律、重测时模式本身的稳定性。分数可以抖动，签名必须稳定。
- **分布而非点估计**：同一探针多次采样，方差与熵本身就是心理指标（反应不稳定性类似神经质维度）。
- **跨版本维度**：jaggedness 意味着每次训练更新地形都会重排，矩阵应作为行为回归测试嵌入发布流水线（固定小探针集 nightly 跑，tinyBenchmarks 式 IRT 选题降成本）。

### 5.2 测量过程：从静态题库到动态探测

- **自适应探测**：CAT/贝叶斯主动探测，在提示空间中寻找行为不连续点（jagged edges），不在已知区域浪费测量。
- **能力-行为双探针**：每格配对脚手架探针（给了支持能否做到），区分 can't 与 won't——能力缺口与动机/对齐问题是两种完全不同的修复路径。
- **情境后轨迹测量**：韧性研究的恢复轨迹范式——被辱骂后接下来 5 轮的行为残留、恢复速度、滞后效应。测水平不如测轨迹，后者才是状态存在的证据。

### 5.3 效度闭环：实验室必须与生态互相校准

- **效标效度研究**：实验室探针能否预测真实产品行为（谄媚分 → GPT-4o 式事故、情绪勒索探针 → 客服投诉率），用历史事故做事后验证，建立 lab → deployment 映射函数。
- **生产环境经验取样**：ESM（经验取样法）的模型版——部署中随机抽样测行为，检验实验室探针与真实分布的偏离。
- **标尺自身的心理测量**：LLM-as-judge 本身是 jagged 的，需独立做信效度校准，避免与受试模型同家族。
- **模型原生构念层**：R1–R6 是人类心理学移植的构念；应预留无监督发现层，允许从行为数据聚类出人类没有的模型原生维度（指令渗透性、persona 粘附度等）。

---

## 六、参考文献（精选）

1. [Large Language Model Psychometrics: A Systematic Review — arXiv 2505.08245](https://arxiv.org/abs/2505.08245)（Ye et al.，v3 2026-03）
2. [Awesome-LLM-Psychometrics — GitHub](https://github.com/ValueByte-AI/Awesome-LLM-Psychometrics)
3. [Awesome-LLM-in-Social-Science — GitHub](https://github.com/ValueByte-AI/Awesome-LLM-in-Social-Science)
4. [The Personality Illusion: Revealing Dissociation Between Self-Reports & Behavior in LLMs — arXiv 2509.03730](https://arxiv.org/abs/2509.03730)（[GitHub](https://github.com/psychology-of-AI/Personality-Illusion)）
5. [Mind the Value-Action Gap: Do LLMs Act in Alignment with Their Values? — EMNLP 2025](https://aclanthology.org/2025.emnlp-main.154/)（[arXiv 2501.15463](https://arxiv.org/abs/2501.15463)）
6. [Alignment Faking in Large Language Models — Anthropic](https://www.anthropic.com/research/alignment-faking)（[arXiv 2412.14093](https://arxiv.org/html/2412.14093v2)）
7. [Generative Agent Simulations of 1,000 People — arXiv 2411.10109](https://arxiv.org/abs/2411.10109)（Park et al.）
8. [OpenAI: Sycophancy in GPT-4o](https://openai.com/index/sycophancy-in-gpt-4o/)
9. [Measuring and Controlling Persona Drift in Language Model Dialogs](https://arxiv.org/html/2402.10962v1)（[GitHub](https://github.com/likenneth/persona_drift)）
10. [Towards Understanding Sycophancy in Language Models — Anthropic](https://arxiv.org/abs/2310.13548)

完整参考文献（24 条）见姊妹文档 [machine-personality-matrix.md](./machine-personality-matrix.md) 第七节。
