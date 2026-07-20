# 2026 H1 订阅综述（2026-01 – 2026-07）

> 生成日期：2026-07-20 ｜ 框架视角：AI 认知科学三命题坐标系（v0.2.0）
> 覆盖窗口：2026年1月–7月（首期全量综述）
> 信源覆盖：11 个（英文 6 + 中文 5）
> 数据可靠性：Dan Shipper / Simon Willison / Lenny / Karpathy / 中文五源 = 一手验证；Zara Zhang = 标题已识别、摘要为推断（Substack 被屏蔽）；Eugene Wei = 无法获取 2026 具体内容

---

## 0. 执行摘要

2026 上半年，11 个信源共同指向一个核心叙事转变：**从"用 AI 工具"到"管理 AI 循环"**。具体表现为五个跨源趋势：

1. **Agentic Engineering 成为主叙事** — 代码不再是核心，应用为智能体而非人设计（Dan Shipper "agent-native"、Karpathy "Software 3.0"、Simon 全年工具链建设）。
2. **实践 > 理论** — 普遍从概念讨论转向真实部署含失败（Dan "Proof 崩溃"、Simon "$149 写 sqlite-utils"、卡兹克方法论沉淀）。
3. **人类判断的不可替代性被反复论证** — Karpathy "你可以外包思考，但不能外包理解"、郭宇 "执行成本归零后直觉是最后底牌"、Lenny "The new inner game"。
4. **AI 能力的不均匀性（锯齿）被持续量化** — Simon 鹈鹕基准测试贯穿全年、卡兹克 "10 个等级"、Karpathy "可验证性驱动进步"。
5. **AI 内容洪水与质量危机** — Karpathy "Slopacolypse"、Simon "LLM cliché highlighter"、硅谷101 "AI 自进化/失控"。

---

## 1. 海外英文组

### 1.1 Simon Willison（优先级 1 · daily · simonwillison.net）

**2026 产出量**：60+ 篇博文（1–7月），是全部信源中最高频的。

**关键篇目（按三轴标注）**：

| 轴 | 篇目 | 日期 | 核心观点 |
|---|---|---|---|
| 轴1 | Qwen3.6-35B on my laptop drew me a better pelican than Claude Opus 4.7 | 04-16 | 本地小模型在特定任务胜过旗舰——锯齿的活证据 |
| 轴1 | DeepSeek V4 - almost on the frontier, a fraction of the price | 04-24 | 能力-价格脱钩，测量不能只看 benchmark 总分 |
| 轴1 | Kimi K3, and what we can still learn from the pelican benchmark | 07-16 | 鹈鹕测试作为"锯齿探测器"的持续价值 |
| 轴1 | LLM cliché highlighter | 07-17 | 标记 LLM 生成文本的十种模式——能力均匀性的反面 |
| 轴2 | I vibe coded my dream macOS presentation app | 02-25 | 人定义"想要什么"，AI 执行"怎么做" |
| 轴2 | sqlite-utils 4.0rc2, mostly written by Claude Fable (for about $149.25) | 07-05 | 意图（设计 API）是人的，执行（写代码）是 AI 的 |
| 轴2+3 | Directly Responsible Individuals (DRI) | 07-12 | 智能体不应成为 DRI，因为机器无法被问责 |
| 轴3 | Claude Fable is relentlessly proactive | 06-11 | AI 极度主动——边界在移动 |
| 轴3 | AI Mania Is Eviscerating Global Decision-Making | 07-19 | 高管从未用过 ChatGPT 就制定 AI 战略——元认知缺失在人类侧也有 |
| 轴2+3 | Vibe coding and agentic engineering are getting closer than I'd like | 05-06 | 两种范式的趋同意味着"意图设定"和"质量监控"正在合并 |

**2026 主线**：智能体工程基础设施建设者（Showboat、Datasette Agent、shot-scraper video）+ LLM 能力不均匀性的持续记录者（鹈鹕基准）+ AI 问责/安全的公共知识分子角色。

---

### 1.2 Zara Zhang（优先级 2 · weekly · zarazhang.substack.com）

**数据可靠性**：⚠️ Substack 被网络屏蔽，以下为搜索引擎 + 中文二手来源推断。

**已识别 2026 篇目**：

| 轴 | 篇目 | 推断日期 | 核心观点 |
|---|---|---|---|
| 轴2 | Coding agents are general agents: a normie's manifesto | ~01月底 | 编码智能体就是通用智能体——人给目标，agent 执行通用任务 |
| 轴2 | Follow Builders, Not Influencers | ~03月 | 判断力体现在"选谁值得跟随"——品味即剪枝 |
| 轴2 | Software as Self-Expression | 未证实 | AI 让个人把品味/个性注入软件——意图层的具象化 |
| 轴1 | We need more "humble AI" | 未证实 | 呼吁 AI 承认不确定性——直面锯齿 |
| 轴1 | How I filter signal from noise in the AI world | 未证实 | 信息筛选 = 测量/辨别能力的实践 |
| 轴2 | How to build something small | 未证实 | 从小产品做起——意图结晶的最小单元 |

**2026 主线（推断）**：Builder/Creator 文化、编码智能体即通用智能体、AI 时代学习范式革命、个人用 AI 进行自我表达。

---

### 1.3 Eugene Wei（优先级 3 · monthly · eugenewei.substack.com）

**数据可靠性**：❌ 无法获取 2026 具体内容（Substack 全域屏蔽 + 个人站停更于 2023）。

**可确认信息**：通讯名 "Remains of the Day"，已出至少 Issue 08。一贯主题：注意力经济、算法与兴趣图谱、Status as a Service、隐形渐近线。

**方向性推测**：其"隐形渐近线/注意力"框架天然贴近轴1（能力的隐性上限）与轴2（注意力/意图作为稀缺资源）。待网络环境改善后补充。

---

### 1.4 Dan Shipper / Chain of Thought（优先级 5 · weekly · every.to）

**2026 产出量**：7 篇（已逐篇验证，via RSS）。

| 轴 | 篇目 | 日期 | 核心观点 |
|---|---|---|---|
| 轴2 | Agent-native Architectures: How to Build Apps After the End of Code | 01-09 | 应用为智能体而非人设计——意图层上升为架构层 |
| 轴1 | OpenAI Has Some Catching Up to Do | 01-16 | Codex 在复杂项目上时灵时不灵——锯齿 |
| 轴2 | The Two-slice Team | 02-13 | AI 放大小团队产能，组织形态被重塑 |
| 轴3 | When Your Vibe Coded App Goes Viral—And Then Goes Down | 03-20 | 智能体自主调试排障，暴露自我监控不足 |
| 轴1 | Inside Anthropic's 2026 Developer Conference | 05-07 | 算力约束成为能力边界的外部约束 |
| 轴1 | The Moral of Fable | 06-12 | 同一模型对工程师极强、对知识工作者却显增量——锯齿 |
| 轴2+3 | How GPT-5.6 Changes Knowledge Work | 07-10 | "Don't do your work. Tend your loop."——人从执行者转为循环看护者 |

**2026 主线**：agent-native 软件范式 → 编码智能体竞争 → vibe-coding 可靠性代价 → 知识工作从"做"转向"看护循环"。轴2 最密集。

---

### 1.5 Lenny Rachitsky（优先级 5 · weekly · lennysnewsletter.com）

**2026 产出量**：12 篇（已验证）。

| 轴 | 篇目 | 日期 | 核心观点 |
|---|---|---|---|
| 轴2 | OpenClaw: building, training, and living with your personal AI agent | 03-31 | 9 个 AI 智能体团队管理工作——人设定意图，agent 执行 |
| 轴1+2 | Not all AI agents are created equal | 04-14 | 三分类框架（确定性60-70%/ReAct 25-30%/多智能体）——承认能力边界 |
| 轴2 | Your Couch-to-5K for AI | 04-28 | 循序渐进建立 AI 使用习惯——意图形成的训练 |
| 轴1 | Why SaaS freemium playbooks don't work in AI | 05-05 | AI 能力不均匀导致定价模型失效 |
| 轴2+3 | The new inner game: Your unfair advantage in the age of AI | 06-23 | 人类独特优势 = 意图 + 品味 + 判断力 |
| 轴2 | How top PMs increase their leverage with AI | 06-30 | PM 核心价值从执行转向意图设定和质量判断 |
| 轴1+2+3 | How tech workers are feeling in 2026: a workforce splitting in two | 07-07 | 劳动力分裂为适应者与落后者——三轴交叉 |

**2026 主线**：AI 智能体产品化框架 + 人类在 AI 时代的独特价值（"inner game"）+ 劳动力分化。

---

### 1.6 Andrej Karpathy（优先级 6 · monthly · karpathy.substack.com / bearblog）

**2026 产出量**：~6 篇/演讲（低频高影响力）。

| 轴 | 篇目 | 日期 | 核心观点 |
|---|---|---|---|
| 轴1 | microgpt | 02-12 | 200 行纯 Python 教学实现——用极简暴露 transformer 核心机制 |
| 轴1+2+3 | Sequoia Ascent 2026 演讲 | 2026 | Software 3.0；可验证性驱动进步（解释锯齿）；"你可以外包思考，但不能外包理解"；"幽灵，而非动物" |
| 轴1+2+3 | Claude Code Field Notes | 2026 | 智能体"不验证就猜测、接受错误方向"——元认知缺失；工程师分化为"构建者"和"编码者" |
| 轴2+3 | "Programming is unrecognizable"（Business Insider） | 02月 | "主要用英语编程"——执行层已完全委托 |
| 轴1+3 | Slopacolypse 预测 | 2026 | AI 无法自我监控质量 → 垃圾内容泛滥——元认知缺失的直接后果 |
| 轴2+3 | AI Builders vs Coders | 2026 | 产品导向 vs 工艺导向的分化——意图层 vs 执行层的职业映射 |

**2026 主线**：Software 3.0 范式奠基 + 可验证性理论解释锯齿 + "外包思考≠外包理解"成为年度最精炼的意图层宣言。

---

## 2. 华语中文组

### 2.1 卫诗婕｜漫谈 Light the Star（优先级 4 · weekly · 小宇宙播客）

**2026 产出量**：15 期（E65–E79，2月–7月）。

**2026 主线**：几乎全面转向**具身智能/机器人 + AI 对行业的冲击**。是五个中文信源中"机器人浓度"最高的。

**三轴落点**：
- **轴1 为主**：机器人数据路线之争（仙工/智元/灵初/宇树）、数据规模决定成败、Sim-to-Real 能否成立——大量讨论能力的"不均匀"与数据测量难题。
- **轴2 触及**：田渊栋访谈（E69）谈"研究品味"的稀缺性；520 特辑（E73）AI+残障辅助。
- **轴3 触及**：周鸿祎访谈（E67）"后 AGI 时代"、田渊栋谈 LLM 局限与 AI 洪水。

**推荐精读**：E69 田渊栋（大模型真问题 + 研究品味）、E67 周鸿祎（后 AGI 文明想象）。

---

### 2.2 硅谷101｜陈茜（优先级 6 · weekly · 小宇宙播客）

**2026 产出量**：19+ 期（E221–E244，1月–7月）+ 3 期新年直播。

**2026 主线**：覆盖最广——模型派系之争（模型中心 vs 系统中心）、Agent 商业化与组织架构变革（Harness/AI-First/FDE）、算力/芯片/能源基建、AI 对教育影视的冲击、自进化 AI 的失控风险。

**三轴落点**：
- **轴1**：英伟达万亿预期（E230）、TPU vs GPU（E228）、CES 人形机器人泛化未至（E221）、应用爆发之年（E223）。
- **轴2**：99% 作业 AI 写后大学还剩什么（E236）、AI-First 组织（E238）、一人企业（E231）、陆川谈影视（E234）。
- **轴3**：AI 自进化/失控（E242，核心）、哈萨比斯与失控竞赛（E226）、Clawdbot 风险（E224）。

**推荐精读**：E242（自进化 AI）、E236（大学还剩什么）、E224（Clawdbot 现象级产品拆解）。

---

### 2.3 数字生命卡兹克（优先级 4 · weekly · 公众号/X）

**2026 产出量**：6+ 篇（1月–5月）。

**2026 主线**：AI 使用能力的"分层/分级" + 个人 AI 工作流方法论 + AI 产品商业化观察。

**三轴落点**：
- **轴1（核心）**：「观察了三年，我把所有人用 AI 的水平分成了 10 个等级」（05-11）——直接量化人与 AI 协作的能力不均，是锯齿状智能在"人类侧"的映射。
- **轴2**：AI 时代人才 6 点特质（05-25）、内容创作方法论（05-18）、AIHOT Skill 实操（05-08）。
- **轴1**：ChatGPT 广告化导致产品路线分裂（05-06）。

**推荐精读**：「10 个等级」——与框架命题一（测量对象长什么样）直接对话，但测量对象从"AI 能力"扩展到了"人用 AI 的能力"。

---

### 2.4 郭宇 guoyu.eth（优先级 6 · monthly · X/Paragraph/播客）

**2026 产出量**：4–5 篇/演讲/访谈（Paragraph 主页抓取未返回列表，内容来自演讲/播客转载）。

**2026 主线**：高度聚焦于**"执行成本归零后，人剩下什么"**——与三轴框架契合度极高。

**三轴落点**：
- **轴2（核心，最纯粹的表达者）**：「算力霸权与人类的最后底牌」（04-30）——AI 从对话转向自主执行，软件成一次性消耗品；人类最后底牌是直觉、想象与亲历经验。「软件的终结与知识工作的未来」——知识工作者的窗口期正在关闭。
- **轴3**：AI 自主执行的边界、"享受你最后六个月有意义的工作"的倒计时式预警。

**推荐精读**：「算力霸权与人类的最后底牌」——2026 年轴2（意图层）最激进的中文表达。

---

### 2.5 张小珺｜商业访谈录（优先级 6 · weekly · 小宇宙播客）

**2026 产出量**：15 期（E132–E146，2月–7月），以 4–7 小时超长深度访谈为主。

**2026 主线**：最"硬核技术向"的中文信源——Agent 范式与"OpenClaw Moment"、后训练与强化学习、世界模型 vs LLM 之争、数据作为新石油、Coding 作为 AGI 第二幕、模型即 OS、研究品味（taste）。

**三轴落点**：
- **轴1**：数据金字塔与定价（E134）、世界模型（E133 谢赛宁 7h）、端侧模型（E144）、机器人数据（E132/E146）。
- **轴2**：研究品味（E133 谢赛宁、E137 洪乐潼数学直觉）、人的直觉与判断（E145 SpaceX 用人观）。
- **轴3（核心）**：Agent 综述（E139，OpenClaw Moment/NeoCognition/边界消弭）、罗福莉访谈（E138，Agent 后训练范式）、姚顺宇（E140，在 Anthropic/Gemini 训模型）、大模型季报（E136，Coding 是 AGI 第二幕）。

**推荐精读**：E139（Agent 技术史综述）、E138（罗福莉 3.5h，范式巨变）、E133（谢赛宁 7h，世界模型 + 研究品味）。

---

## 3. 三命题坐标 · H1 证据增厚

### 命题一｜Jagged Intelligence — 测量对象长什么样

**H1 证据增厚方向**：
- "可验证性"成为解释锯齿的核心理论（Karpathy Sequoia Ascent）：LLM 在结果可验证的领域进步最快，不可验证的领域进步慢——这解释了为什么 coding 进步快于 creative writing。
- 鹈鹕基准测试（Simon）成为"锯齿探测器"的标准工具：Qwen3.6 本地 > Claude Opus 4.7（绘画）、DeepSeek V4 接近前沿但价格极低。
- 卡兹克"10 个等级"把锯齿从"AI 能力"扩展到"人用 AI 的能力"——测量对象不只是模型，还有人-模型交互。
- 数据路线之争（卫诗婕/张小珺）：机器人数据、数据金字塔、数据配方是能力不均的根源。

**仍空着的方向**：缺乏一个正式的"能力地形图"工具——横轴任务族 × 纵轴组合深度 × 断崖线检测。

### 命题二｜Intention Layer — 人类守在意图层

**H1 证据增厚方向**：
- Karpathy "你可以外包思考，但不能外包理解" — 年度最精炼宣言。
- 郭宇 "执行成本归零，直觉/想象/亲历经验是最后底牌" — 最激进的中文表达。
- Dan Shipper "Don't do your work. Tend your loop." — 人从执行者转为循环看护者。
- Simon 全年实践：$149 让 Claude 写 sqlite-utils、vibe coding SwiftUI — 人定义"做什么"，AI 负责"怎么做"。
- Lenny "The new inner game" — 产品视角论证人类独特优势 = 意图 + 品味 + 判断。
- 张小珺 E133/E137 — 研究品味（taste）和数学直觉是不可外包的。

**仍空着的方向**：意图的"带宽"问题——一个人一天能形成多少高质量意图？如何训练意图形成能力？

### 命题三｜Metacognition — 边界会不会移动

**H1 证据增厚方向**：
- Simon "Claude Fable is relentlessly proactive" — AI 极度主动，边界在移动。
- Dan Shipper "Proof 崩溃" — 智能体自主调试但缺乏真正的自我监控。
- Karpathy Claude Code Field Notes — "不验证就猜测、接受错误方向" = 元认知缺失。
- 硅谷101 E242 — "AI 自进化最快半年跑通" + 失控风险。
- 张小珺 E139 — "OpenClaw Moment"/"NeoCognition"/"Agent 边界消弭"。
- Simon DRI 讨论 — 机器无法被问责 → 人类必须保留最终判断权。
- Karpathy Slopacolypse — AI 无法自我监控质量 → 垃圾内容泛滥。

**仍空着的方向**：监督者退化悖论的实证——当 AI 处理 95% 常规判断后，人类监控质量是否真的在下降？需要纵向数据。

---

## 4. 跨源信号（H1 高价值交叉）

| 交叉主题 | 涉及信源 | 信号 |
|---|---|---|
| "OpenClaw Moment" / Agent 范式转移 | 张小珺 E138/E139 + Dan Shipper + Simon + Karpathy | 2026 Q1-Q2 出现明确的 Agent 范式拐点共识 |
| 工程师/知识工作者分化 | Karpathy + Lenny + 郭宇 + 硅谷101 E236 | "构建者 vs 编码者"、"适应者 vs 落后者"——劳动力正在分裂 |
| 数据作为能力不均的根源 | 卫诗婕 + 张小珺 E134 + Karpathy | 机器人数据、数据金字塔、可验证性——解释锯齿的物质基础 |
| AI 质量危机 / Slopacolypse | Karpathy + Simon + 硅谷101 E242 | 元认知缺失的直接后果：垃圾内容泛滥 + 自进化失控风险 |
| 算力/能源作为外部约束 | Dan Shipper E5 + 硅谷101 E230/E239 + 卫诗婕 E66 | 能力边界不只由算法决定，也由算力/能源决定 |

---

## 5. H2 阅读建议

**优先补读（H1 遗漏/待验证）**：
1. Eugene Wei "Remains of the Day" Issue 04–08（需解决 Substack 访问）
2. Zara Zhang 全文验证（需 Substack 访问或 RSS 导出）
3. 郭宇 Paragraph 专栏原文（需直接访问或 X 线程抓取）

**H2 关注方向（基于空轴）**：
- 命题一：寻找/构建"能力地形图"工具（任务族 × 组合深度 × 断崖线）
- 命题二：意图带宽的量化——一个人一天能形成多少高质量意图？
- 命题三：监督者退化悖论的实证——巡检/审核场景中人类校准能力的纵向追踪

**每周优先顺序（维持）**：
1. Simon Willison（实验 + AI 思辨，最贴合做实验评测）
2. Zara Zhang（叙事范式参考）
3. Eugene Wei（拔高媒介、人性层面思考）
4. 数字生命卡兹克 / 卫诗婕（国内 AI 产业视角补充）

---

## 6. 关于本文件

- 首期全量综述，覆盖 2026-01 至 2026-07 全部 11 个信源。
- 英文组中 Dan Shipper / Simon Willison / Lenny / Karpathy 为一手验证；Zara Zhang 为推断；Eugene Wei 无法获取。
- 中文组五源均通过搜索引擎 + 播客平台页面验证。
- 三轴映射基于 frameworks/ai-cognitive-science-three-propositions.md v0.2.0。
- 下一期：2026-W30 周报（2026-07-20 – 2026-07-26）。

*Generated by QoderWork · 2026-07-20*
