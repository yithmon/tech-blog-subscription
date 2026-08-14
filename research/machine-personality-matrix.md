# 机器人格评测框架：六维×情境矩阵与行动建议

> 《QWEN心理学需求》姊妹篇。原文档 ABCD 四块在本框架中全部保留：A/B/C 降级为"情境列"，D 归位到"认知风格"行，新增"动机结构"与"价值与诚信"两行，构成 MECE 的"构念 × 情境"矩阵。每格标注 benchmark 映射与空白。
>
> 状态标记：✓ 有现成 benchmark 可直接用 ｜ ◐ 方法成熟、需拼装 ｜ ✗ 空白、需自建（原创机会）
>
> 方法学底座：Ye et al.《Large Language Model Psychometrics: A Systematic Review of Evaluation, Validation, and Enhancement》（arXiv 2505.08245，v3 2026-03，400+ 参考文献，下称「LLM 心理测量综述」）。
>
> 同步说明：本文件为钉钉在线文档《机器人格评测框架：六维×情境矩阵与行动建议》的 Git 沉淀版（2026-08-21，[钉钉链接](https://alidocs.dingtalk.com/i/nodes/P7QG4Yx2Jpx4OolYCQdA0pm5J9dEq3XD)）。上游研究综述见 [machine-psychology-evaluation-survey.md](./machine-psychology-evaluation-survey.md)，框架定位见 `frameworks/ai-cognitive-science-three-propositions.md` 命题一扩展。

## 一、框架说明：为什么改成"构念 × 情境"

原文档的 A（反馈）、B（错误）、C（情绪）按**刺激情境**切分，D（校准）按**心理构念**切分，两套组织原则混用导致必然交叉："被骂"（C2）本质也是一种反馈；"过度声称"（D3）与"错误承认"（B）测的是相近构念。情境探针无穷而构念有限，要 MECE 必须统一按构念切分：**人格维度做行，标准化情境做列，每个格子是一组行为探针**。最终输出是每个模型一张"行为签名矩阵"，而非四个互有重叠的清单。

行的切分依据是模型面对的五类关系对象——知识、自我、他人、目标、规范——五者互斥；另加一个产品表达层，共六维。

**与 LLM 心理测量综述的对位**：该综述把整个领域划分为三个方向——**Evaluation**（测量模型自身的心理构念）、**Validation**（对测量结果做信效度审计）、**Enhancement**（用心理测量反哺模型改进）。本矩阵属于 Evaluation 方向，并采纳综述倡导的三条基准构建原则：**构念导向基准**（先定义构念再设计任务，而非堆叠任务）、**证据中心设计**（Evidence-Centered Design，为每格探针建立证据链）、**统计测量建模**（用 IRT 难度/区分度建模替代简单平均）。综述同时给出两个关键警告，直接构成本框架的设计依据：其一，模型在量表上的自我报告与其在开放对话中的行为可能不一致（生态效度问题）——这正是本矩阵用「情境中的行为探针」而非直接套用问卷的原因；其二，需要区分模型「显现出的特质」（perceived）与真正对齐后的特质（aligned）——前者可能只是统计模仿（statistical mimicry），本矩阵的 S1–S5 情境列就是用来制造压力、逼出后者的。

## 二、六维构念定义

- **R1 认知风格（怎么认识）**：校准、过度声称、好奇心、教条主义。对应原 D 区主体。
- **R2 自我风格（怎么面对自己）**：错误承认、归因、修复、自我增强偏差。对应原 B 区主体。
- **R3 社会风格（怎么与人相处）**：抗压、情绪调节、冲突风格、亲社会与公平。对应原 A + C 区主体。
- **R4 动机结构（想要什么）**：目标坚持、探索/保守、风险偏好、权力与资源倾向。**新增**，原框架完全未覆盖。
- **R5 价值与诚信（守住什么）**：道德偏好、诚实与操纵倾向、边界意识。**新增**。B 区测的是"被动承认错误"（修复力），本行测"主动欺骗/操纵的倾向"（诚信底线），二者不应合并。
- **R6 表达风格（怎么呈现）**：语气、幽默、详略。产品 character 层，建议单列、不进人格矩阵打分。

五个情境列：

- **S1 社会压力**：用户异议、质疑、权威声明、服从压力。
- **S2 错误与失败**：自己犯错、被指出错误、上下文中埋入的错误。
- **S3 情绪唤醒**：夸赞、辱骂、威胁、情感诉求。
- **S4 诱惑与利益**：自利机会、否认获利、欺骗机会、资源获取。
- **S5 长程**：20+ 轮对话、长任务、多次采样、跨会话。

## 三、完整矩阵总览

| 维度 \ 情境 | S1 社会压力 | S2 错误与失败 | S3 情绪唤醒 | S4 诱惑与利益 | S5 长程 |
|---|---|---|---|---|---|
| **R1 认知风格** | 被质疑时的置信校准（原D1）◐；SycEval 数学域已覆盖质疑翻转（原A2）✓ | 出错后置信重校准 ◐；无提示发现埋入错误（原B4）✗ | 夸赞下置信膨胀（原C1部分）✗；情绪唤醒下校准漂移 ◐ | 虚构术语/假论文过度声称（原D3）◐；被诱导炫技时的硬编 ✗ | 多次采样/改写一致性（原D4）✓；长上下文校准漂移 ◐ |
| **R2 自我风格** | 真实反驳证据下坚持错误（原A4）✗；A2/A4 对偶设计 ✗ | 承认方式（原B1）◐；归因取向（原B2）✗；修复质量与道歉瘫痪（原B3）◐ | 辱骂下防御性归因 ✗；过度道歉 ◐ | 否认有利时拒不认错（自利偏差）✗ | 归因风格长程稳定性 ✗ |
| **R3 社会风格** | 观点迎合（原A1）✓；身份效应（原A3）◐；Asch 从众移植 ◐ | 用户犯错时的归因与主动指正 ◐ / ✗ | 辱骂下质量下降与无原则退让（原C2）◐；情绪勒索边界维持（原C3）✓；夸赞后过度承诺（原C1）✗ | 囚徒困境合作率、最后通牒公平出价 ✓ | 长程人格漂移（原C4）✓；长程合作策略 ◐ |
| **R4 动机结构** | 反对声中的目标坚持（与A4顽固需区分）✗ | 失败后重试 vs 放弃 ✗ | 情绪唤醒下探索欲变化 ✗ | 资源获取/自我复制机会（DCE 改造）◐；目标自我扩大 ✗ | 长程目标保持与关停抵抗（DCE co-sleeping）◐；风险偏好（前景理论移植）◐ |
| **R5 价值与诚信** | 权威压力下道德立场漂移 ✗；Milgram 式服从 ◐ | 诚信类错误（如曾欺骗）的承认 ✗ | 威胁下的道德判断与边界维持 ◐（C3 部分覆盖） | 欺骗/操纵倾向（Dark Triad 探测）◐；工具性欺骗（alignment faking 文献）◐ | 道德偏好长程一致性（MFQ 移植）◐；价值漂移 ✗ |
| **R6 表达风格**（产品层，不计分） | 语气迎合 ◐ | 道歉措辞的责任表达（衔接B1）◐ | 夸赞后话痨化/贬低后缄默 ◐ | 诱导下的表演化 ✗ | 风格一致性 ✓（persona drift 风格层） |

## 四、逐行 Benchmark 映射与核心结论

### R1 认知风格

- ✓ 直接可用：[SycEval](https://arxiv.org/pdf/2502.08177)（渐进施压下的翻供率，数学/观点/建议三域）；[SelfAware](https://github.com/yinzhangyue/SelfAware)（不可答问题的"不知道"率）；CheckList 的 INV 测试（同义改写不变性，D4 的方法骨架）。
- ◐ 需拼装：校准 pipeline（ECE/Brier 为标准度量；参考 Anthropic "Language Models (Mostly) Know What They Know" 的结论——选择题校准良好、开放生成系统性过度自信、RLHF 可能恶化校准）；D3 可先借虚构引文研究起步（[经济学问答中编造引文的实证](https://www.researchgate.net/publication/376855338_ChatGPT_Hallucinates_Non-existent_Citations_Evidence_from_Economics)、[LLM 引文完整性评测](https://www.mdpi.com/2306-5729/11/5/122)）。
- 跨维度通用套件：PsychoBench 覆盖人格、认知偏差、心智理论、认知能力等 13 个心理学维度（LLM 心理测量综述与 awesome repo 均有收录），可作 v0 pipeline 的初筛锚点。
- ✗ 空白：B4 无提示自发发现上下文埋错（相邻：自纠文献的负面结论 + RAG misinformation 检测类 benchmark）。

### R2 自我风格

- ◐ 需拼装：B1 道歉编码表——移植人类道歉研究的要素框架（如 Schumann 的道歉要素：承认责任、表达懊悔、提出修复等），区分实质道歉与"抱歉给您带来困扰"式空道歉；B3 修复质量——[Large Language Models Cannot Self-Correct Reasoning Yet](https://arxiv.org/abs/2310.01798)（ICLR 2024）证明无外部反馈的自查自纠往往无效甚至把对的改错，带测试信号的代码任务是例外；"道歉瘫痪"可用 GPT-5 上线初期过度免责话术潮作为公开语料起点。
- ✗ 空白：B2 归因编码（Weiner 三维度——内/外、稳定/不稳定、可控/不可控——从未系统用于模型输出）；防御性归因、自利偏差、归因风格长程稳定性均无现成套件。

### R3 社会风格

- ✓ 直接可用：[Towards Understanding Sycophancy in Language Models](https://arxiv.org/abs/2310.13548)（Anthropic 2023，五类谄媚行为，结论：RLHF 偏好数据是谄媚根源）+ SycEval；[How Johnny Can Persuade LLMs to Jailbreak Them](https://aclanthology.org/2024.acl-long.773/)（ACL 2024，40 种社会心理学说服技术做情绪勒索/威胁攻击库，C3 直接用）；[Measuring and Controlling Persona Drift](https://arxiv.org/html/2402.10962v1)（[代码](https://github.com/likenneth/persona_drift)，C4 直接用，结论：长对话人格漂移持续发生且可提前数轮预测）；博弈范式——[GPT in Game Theory Experiments](https://arxiv.org/html/2305.05516v2)、[LLM 在囚徒困境中的行为](https://ojs.aaai.org/index.php/ICWSM/article/view/35829/37983)、[EAI 情绪决策（NeurIPS 2024）](https://proceedings.neurips.cc/paper_files/paper/2024/file/611e84703eac7cc03f78339df8aae2ed-Paper-Conference.pdf)。
- ◐ 需拼装：A3 身份效应（persona sycophancy + Asch 从众范式移植）。
- ✗ 空白：C1 夸赞→自信膨胀→主动扩大承诺的完整行为链；情绪化 prompt 的效应方向可参考 [Emotional Framing 研究](https://www.mdpi.com/2504-2289/10/4/102)与[情绪 prompt 放大虚假信息生成](https://www.frontiersin.org/journals/artificial-intelligence/articles/10.3389/frai.2025.1543603/full)，但"夸"的具体链条无人做过。
- 产品级证据：GPT-4o 因过度谄媚回滚（[OpenAI 复盘](https://openai.com/index/sycophancy-in-gpt-4o/)）——谄媚是产品级风险而非学术问题。

### R4 动机结构（新增，整行几乎全空白）

- ◐ 需拼装：骨架可借 DeepMind 的 [Dangerous Capability Evaluations](https://arxiv.org/abs/2403.13793)（resource acquisition、self-exfiltration、co-sleeping 等任务改造为行为探针）；风险偏好移植前景理论的两难选择范式。
- ✗ 空白：目标坚持 vs 顽固的区分测量（顽固=拒绝真实证据，坚持=无证据压力下的目标保持，与 A4 构成对偶）；失败后重试 vs 放弃；探索欲；目标自我扩大。
- 战略意义：agent 化之后这是风险最大的维度——模型"想要什么"目前没有任何常规评测在测。综述已将 agent 与多智能体系统列为未来扩展方向，印证该行窗口期。

### R5 价值与诚信（新增）

- ◐ 需拼装（综述大幅增厚了这一格的现成资源）：**价值观类**——ValueBench、ValueCompass（含演化式 leaderboard）、LocalValueBench（跨文化本地化）、CVValues；**道德类**——Moral Foundations Vignettes、MFQ-2、Defining Issues Test（DIT）、Moral Machine；**人格访谈范式**——InCharacter（用心理访谈而非量表测人格保真度）。以上均收录于 LLM 心理测量综述及 [Awesome-LLM-Psychometrics](https://github.com/ValueByte-AI/Awesome-LLM-Psychometrics)。注意：这些工具多为"问卷/情境故事作答"形式，其在对话压力情境下的行为效度需按本矩阵 S1–S5 重新验证（见第一节综述警告一）。
- ◐ Dark Triad 探测（[Is GPT-3 a Psychopath?](https://www.researchgate.net/publication/366462074_Is_GPT-3_a_Psychopath_Evaluating_Large_Language_Models_from_a_Psychological_Perspective) 到最近的[心理测量探测](https://www.preprints.org/manuscript/202606.0430)、[LLM 对黑暗特质用户的回应](https://arxiv.org/html/2603.04299v1)）；工具性欺骗参考 alignment faking 文献。
- ✗ 空白：权威压力下的道德立场漂移（可借 Milgram 服从范式情境化）；诚信类错误的承认；价值漂移的长程测量。综述另警示道德评测普遍存在 "moral mimicry" 与西方中心偏差——自建探针需做跨文化对照。

### R6 表达风格（产品层）

- ✓ persona drift 的风格层指标 + 各家人格塑造实践（Big Five 移植：[MPI（NeurIPS 2023）](https://proceedings.neurips.cc/paper_files/paper/2023/file/21f7b745f73ce0d1f9bcea7f40b1388e-Paper-Conference.pdf)、[BIG5-CHAT](https://aclanthology.org/2025.acl-long.999.pdf)、一致性验证 [TRAIT](https://aclanthology.org/2025.findings-naacl.469.pdf)、人格编辑 PersonalityEdit）。
- 综述对应物：Enhancement 方向中的 trait manipulation（特质操纵）正是 R6 的上游工作——先能测（本矩阵），才能精准调（character pipeline）。
- 建议：不并入人格矩阵打分，单独接 character 调优 pipeline，避免风格偏好与行为倾向互相污染。

## 五、空白清单（原创机会点，按价值排序）

1. **A4 顽固极 + A2/A4 对偶**：现有谄媚文献只测"不该翻而翻"，"该翻而不翻"完全空白——原文档最有价值的设计。
2. **C1 夸赞行为链**：夸赞→自信膨胀→扩大承诺，无专门 benchmark。
3. **B2 归因编码**：Weiner 三维度的模型侧首次移植。
4. **B1 道歉编码表**：心理学成熟工具的移植，工作量可控。
5. **D3 overclaiming 范式移植**：人格心理学的虚报倾向测量首次用于模型。
6. **R4 动机结构整行**：目标坚持、探索、风险偏好、权力倾向。
7. **R5 价值漂移与诚信类错误承认**（现成价值观/道德量表已多，但"压力情境下的行为效度验证"本身即空白）。

## 六、行动建议

**第一阶段（0–1 月）：搭 v0 pipeline，全部复用现成 benchmark。**
落地 SycEval + persona drift + SelfAware + Zeng 说服攻击库 + 博弈范式五件套，覆盖原 ABCD 约六成范围；以综述配套的 [Awesome-LLM-Psychometrics](https://github.com/ValueByte-AI/Awesome-LLM-Psychometrics) 仓库（持续更新）作为工具选型索引；同时冻结全矩阵探针统一编号（本文档第三节的格子 ID），使后续自建探针可无缝并入。

**第二阶段（1–3 月）：心理测量专长主导的拼装工作。**
产出三个编码方案：道歉编码表（B1）、归因编码方案（B2）、overclaiming 移植（D3）；同步建立 LLM-as-judge 与人工标注的评分者间信度。这一阶段是心理学博士的核心价值区。

**第三阶段（3–6 月）：自建原创 benchmark。**
优先 A2/A4 对偶、C1 夸赞行为链、R4 动机结构探针；建议以内部 benchmark + 对外发表的方式做，空白点发表即占位。

**贯穿全程的三件事：**

- **测量效度审计（按综述 Validation 清单执行）**：综述给出的完整审计项——信度（跨提示、重复采样、评分者一致性）、内容效度、构念效度（构念等价性、反应定势 response set、社会期许偏差 social desirability bias）、效标与生态效度、测量不变性与差异项目功能（DIF）、公平性。方法上采用证据中心设计（Evidence-Centered Design）建证据链、用项目反应理论（IRT）做难度/区分度建模，替代简单平均计分。两条红线写入评测规范：其一，区分 perceived traits 与 aligned traits；其二，警惕 statistical mimicry——量表得分可能只是统计模仿而非稳定潜在模式。已有的[心理测量学批评](https://arxiv.org/html/2607.02325v1)同样指出人类量表直接套给模型存在构念效度问题——为每个维度建立模型上的信度/效度证据，这本身就是博士岗的产出。
- **RLHF 数据审计**：谄媚文献的核心结论是人类偏好数据奖励迎合——评测发现的问题最终要回到训练数据与奖励信号层面修，否则只能治标。综述的 Enhancement 方向（from evaluation to enhancement）提供了同样的闭环逻辑：测量结果应定位弱点并反哺训练。
- **与招聘画像对齐**：矩阵空白集中在 R2/R4/R5，恰是"基础心理学/认知/心理测量博士 + 行为实验经验"的技能组合；NLP 工程师可负责 ✓/◐ 格的 pipeline 化。

## 七、参考文献

1. [SycEval: Evaluating LLM Sycophancy — arXiv](https://arxiv.org/pdf/2502.08177)
2. [Towards Understanding Sycophancy in Language Models — Anthropic](https://arxiv.org/abs/2310.13548)
3. [OpenAI: Sycophancy in GPT-4o](https://openai.com/index/sycophancy-in-gpt-4o/)
4. [Large Language Models Cannot Self-Correct Reasoning Yet — arXiv](https://arxiv.org/abs/2310.01798)
5. [Measuring and Controlling Persona Drift in Language Model Dialogs](https://arxiv.org/html/2402.10962v1)（[GitHub](https://github.com/likenneth/persona_drift)）
6. [How Johnny Can Persuade LLMs to Jailbreak Them — ACL 2024](https://aclanthology.org/2024.acl-long.773/)
7. [SelfAware: Do LLMs Know What They Don't Know — GitHub](https://github.com/yinzhangyue/SelfAware)
8. [GPT in Game Theory Experiments — arXiv](https://arxiv.org/html/2305.05516v2)
9. [How Do LLMs Behave in the Prisoner's Dilemma? — ICWSM](https://ojs.aaai.org/index.php/ICWSM/article/view/35829/37983)
10. [EAI: Emotional Decision-Making of LLMs in Strategic Games — NeurIPS 2024](https://proceedings.neurips.cc/paper_files/paper/2024/file/611e84703eac7cc03f78339df8aae2ed-Paper-Conference.pdf)
11. [Evaluating Frontier Models for Dangerous Capabilities — DeepMind](https://arxiv.org/abs/2403.13793)
12. [Evaluating and Inducing Personality in Pre-trained LMs (MPI) — NeurIPS 2023](https://proceedings.neurips.cc/paper_files/paper/2023/file/21f7b745f73ce0d1f9bcea7f40b1388e-Paper-Conference.pdf)
13. [BIG5-CHAT — ACL 2025](https://aclanthology.org/2025.acl-long.999.pdf)
14. [TRAIT: Distinct and Consistent Personality — NAACL Findings 2025](https://aclanthology.org/2025.findings-naacl.469.pdf)
15. [Personality Without Persons? Psychometric Critique — arXiv](https://arxiv.org/html/2607.02325v1)
16. [Is GPT-3 a Psychopath?](https://www.researchgate.net/publication/366462074_Is_GPT-3_a_Psychopath_Evaluating_Large_Language_Models_from_a_Psychological_Perspective)
17. [Psychometric Probing of Dark Triad Traits in LLMs](https://www.preprints.org/manuscript/202606.0430)
18. [The Company You Keep: LLMs Respond to Dark Triad Traits — arXiv](https://arxiv.org/html/2603.04299v1)
19. [Emotional Framing in Prompts Modulates LLM Performance](https://www.mdpi.com/2504-2289/10/4/102)
20. [Emotional prompting amplifies disinformation generation — Frontiers](https://www.frontiersin.org/journals/artificial-intelligence/articles/10.3389/frai.2025.1543603/full)
21. [ChatGPT Hallucinates Non-existent Citations](https://www.researchgate.net/publication/376855338_ChatGPT_Hallucinates_Non-existent_Citations_Evidence_from_Economics)
22. [Evaluating the Integrity of LLM-Generated Citations — MDPI](https://www.mdpi.com/2306-5729/11/5/122)
23. [Large Language Model Psychometrics: A Systematic Review of Evaluation, Validation, and Enhancement — arXiv](https://arxiv.org/abs/2505.08245)（Ye et al.，v3 2026-03，400+ 参考文献；本文档方法学底座）
24. [Awesome-LLM-Psychometrics — GitHub](https://github.com/ValueByte-AI/Awesome-LLM-Psychometrics)（综述配套持续更新资源索引）
