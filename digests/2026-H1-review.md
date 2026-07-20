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

## 5. 实践图谱：项目、产品与商业模式

> 理论之外，这 11 位创作者在 2026 H1 各自落地了什么？本章按"做了什么 → 解决什么问题 → 怎么活下来"三层结构记录。

### 5.1 Simon Willison — 开源工具链 + 独立赞助

| 项目 | 形态 | 解决什么 |
|---|---|---|
| **Datasette Agent**（05-21 发布） | 开源插件 | 自然语言 → SQLite 查询，非技术用户也能问数据库；支持图表/图片/沙箱代码执行 |
| **sqlite-utils 4.0** | 开源 CLI 库 | 5 年来首次大版本，核心代码由 Claude Fable 完成（成本 ~$149） |
| **LLM CLI 0.32a** | 开源命令行 | 无厂商锁定的本地 LLM 调用入口 |
| **shot-scraper video** | 开源工具 | 让 AI agent 自动录制操作视频作为工作证据 |
| **博客赞助实验**（02-19 启动） | 商业模式 | 纯文本广告位（无 JS/无 Cookie），按周出售；Atlassian、Teleport 已入 |

**创新点**：把"AI 辅助开发"从口号变成可审计的工程实践——每笔 AI 代码成本公开、每个工具保持可组合。赞助模式证明独立技术写作者不依赖平台算法也能养活自己。

**商业模式**：周赞助广告 + GitHub Sponsors（$10/月含月度 LLM 摘要邮件）+ "零交付物咨询"（纯顾问通话，不写报告不写代码）+ 演讲（PyCon US 2026 等）。

---

### 5.2 Zara Zhang — 开源小工具矩阵 + "Build for One"

| 项目 | 形态 | 解决什么 |
|---|---|---|
| **codebase-to-course** | 开源 GitHub 工具 | 把任意代码仓库自动转化为教学课程 |
| **youtube-to-ebook** | 开源 | YouTube 视频 → 结构化电子书 |
| **personalized-podcast** | 开源 | 为个人生成定制播客 |
| **frontend-slides** | 开源（已贡献为 QoderWork skill） | AI 驱动的演示文稿生成 |
| **lark-coding-agent-bridge** | 开源 | 飞书 ↔ 编码智能体桥接 |
| **follow-builders** | 开源 | 策展"值得关注的构建者"列表 |

**创新点**：每个工具都是"Build for One"哲学的实例——不为规模设计，为个人赋能设计。18 个 GitHub 仓库构成一个"AI 时代个人杠杆"工具集，把内容在不同形态间自由转换。

**商业模式**：Substack 付费订阅 + 演讲/工作坊 + 开源工具引流。无团队，纯个人运作。

---

### 5.3 Eugene Wei — 战略智识资本 + 天使投资

| 项目 | 形态 | 解决什么 |
|---|---|---|
| **"Remains of the Day" Newsletter** | Substack（10万+ 订阅） | 平台动力学、注意力经济、AI 对消费产品的冲击分析 |
| **天使投资组合** | 20+ 早期公司 | 消费互联网/社交/AI 消费应用的早期判断 |
| **战略顾问** | 非正式 advisory | 为创始人提供"Status as a Service"框架下的产品战略 |

**创新点**：不建产品、不写代码、不做课程——纯粹以"思维框架"作为产品。"Status as a Service"和"TikTok and the Sorting Hat"两篇文章持续被引用为行业基础文献，证明深度思考本身有市场。

**商业模式**：天使投资回报 + 顾问费 + Substack 订阅 + 演讲。无公司、无员工、无产品——"独立思想家"模式的极端案例。

---

### 5.4 Dan Shipper / Every — AI 原生媒体 × 软件工厂

| 项目 | 形态 | 解决什么 |
|---|---|---|
| **Proof**（03-11 发布，开源） | 在线文档编辑器 | 人-AI 协作编辑：绿色=人写、紫色=AI写，带修订追踪；免费、无需登录 |
| **Cora / Sparkle / Spiral / Lex** | SaaS 产品矩阵 | AI 写作/研究/工作流工具 |
| **Claudy** | 内部 AI agent | 绑定 Every 咨询业务的智能体 |
| **"Agent Native" 框架** | 方法论 + 公开指南 | 产品同时为人类和 AI agent 设计（审批、可读日志、回滚） |
| **咨询业务** | 服务 | 帮企业变成 AI-native，年收入 $1M+ |

**创新点**：5 个产品 100% AI 写代码、极小团队运营、$1.2M ARR。Proof 的"作者归属可视化"解决了 AI 协作中最基本的信任问题——谁写了什么。"Agent Native"架构把 AI agent 当一等用户而非附属工具。

**商业模式**：媒体（日更 AI newsletter + 播客）+ SaaS 产品 + 咨询（$1M+/年）。七位数总收入，Proof 零推理成本（用户自带 AI）。

---

### 5.5 Lenny Rachitsky — PM 教育帝国 + Product Pass 创新

| 项目 | 形态 | 解决什么 |
|---|---|---|
| **Newsletter**（120 万读者） | Substack #1 商业通讯 | PM/产品知识民主化 |
| **Product Pass** | 订阅权益 | 打包 25+ 付费 AI/产品工具（价值 $30,000+），订阅者免费用 |
| **Community**（4 万人 Slack） | 私有社群 | PM/创始人网络效应：mentorship、AMA、五大洲 meetup |
| **Podcast 矩阵** | 主播客 + Lenny's Reads + Lightning Round | 多格式覆盖，单期 10-20 万下载 |
| **1200 人年度峰会** | 线下活动 | 社区凝聚 + 品牌 |

**创新点**：Product Pass 是创作者经济的新物种——SaaS 公司付费获得分发渠道，订阅者获得 $30K+ 工具包，Lenny 获得增长飞轮。首次 Perplexity 合作当天创下"newsletter 历史最大增长日"。零全职员工、~10 个全球 contractor。

**商业模式**：付费订阅（$20/月或 $200/年）+ Insider 层（$400/年）+ Product Pass 合作分成 + 播客赞助 + 峰会。CNBC 确认年收入 $1M+。

---

### 5.6 Andrej Karpathy — 前沿研究 + 教育开源 + 范式定义

| 项目 | 形态 | 解决什么 |
|---|---|---|
| **加入 Anthropic**（05月） | 全职研究 | 领导预训练组，"用 Claude 加速 Claude 自身的预训练研究" |
| **nanochat**（活跃维护中） | 开源教学项目 | $48 训练一个 GPT-2 级模型（8×H100），单旋钮 `--depth` 控制复杂度 |
| **Software 3.0 框架**（Sequoia Ascent 演讲） | 思想产品 | 重新定义软件产业：代码 = prompt + 验证，非手写逻辑 |
| **Agentic Engineering 框架** | 方法论 | 取代"vibe coding"：开发者监督不可靠 agent，验证循环 + 需求优先 |
| **Eureka Labs**（暂停） | 教育创业 | LLM101n：学生 + AI tutor 配对学习（因加入 Anthropic 暂停，未关闭） |

**创新点**：nanochat 把 LLM 训练从"大厂专属"变成"任何人 $50 可复现"。Software 3.0 和 Agentic Engineering 两个框架为整个行业提供了词汇表和心智模型——"你可以外包思考，但不能外包理解"成为年度金句。

**商业模式**：Anthropic 薪资/股权 + 全开源（nanochat/nanoGPT/llm.c 均免费）+ 演讲。不直接变现产品，影响力驱动生态价值。

---

### 5.7 卫诗婕 — 独立深度访谈工作室

| 项目 | 形态 | 解决什么 |
|---|---|---|
| **《漫谈 Light the Star》播客**（79 期） | 长音频/视频访谈 | 3-4 小时创始人深度对话，2026 年聚焦具身智能/机器人 |
| **微信公众号** | 长文 | 访谈精华 + 独立商业观察 |

**创新点**："作坊式"全链路独立制作——从选题、采访、录制到剪辑一人完成，拒绝机构媒体的效率约束。影石/刘靖康访谈被创始人评价为"把我们公司拆解得最彻底的访谈"。2026 年几乎全面转向机器人赛道（仙工/智元/灵初/宇树/群核），成为中文世界具身智能访谈密度最高的独立媒体。

**商业模式**：品牌赞助 + 委托内容。无付费课程/社群/会员——明确表态"验证内容可持续生产的思路"，不靠知识付费。

---

### 5.8 硅谷101｜陈茜 — 三线并行的科技媒体公司

| 项目 | 形态 | 解决什么 |
|---|---|---|
| **播客 Season 4**（40-75 min/期） | 音频 | 中美科技/AI 对比叙事 |
| **YouTube 视频论文** | 长视频（电影级制作） | 英伟达发家史、OpenAI 成长史、孙正义等深度视觉叙事 |
| **2026 新年直播系列** | 直播 + 辩论 | "万亿基建还是 AI 泡沫？"——首次引入对抗性辩论格式 |

**创新点**：从纯音频播客转型为"播客 + 电影级视频 + 直播辩论"三线格式，利用陈茜 10 年电视制作功底（CNBC/CCTV/NYSE 现场报道）做降维打击。实体公司 Valley101.Inc 运营。

**商业模式**：品牌赞助/广告（科技/金融/出海品牌）+ 平台分成（YouTube/B站/小宇宙）。无付费课程或会员层。

---

### 5.9 数字生命卡兹克 — 一人 AI 内容工厂

| 项目 | 形态 | 解决什么 |
|---|---|---|
| **AI 生成内容工作室**（一人） | 公众号/X 内容 | 5 晚用 MidJourney+Gen2 产出预告片：693 图 → 185 镜头 → 60 终剪 |
| **公开 Prompt 模板** | 社区资源 | 降低 AI 创作门槛 |
| **腾讯元器 AI 客服** | 自动化 | 私信 AI 自动回复（每条 <100 字） |
| **AI 万人大会**（2025/2026） | 线下活动 | 万人规模 AI 创作者聚会 |

**创新点**：证明"一人公司"可以用 AI 达到媒体公司级产出。核心方法论："把任何重复 3 遍的事 AI 化"。影响力排名曾位列科技媒体第 2（超过多数机构媒体），被导演郭帆注意、登上 CCTV6。

**商业模式**：商业植入（单篇报价六位数）——头部互联网公司的 AI 产品传播预算。公开否认"两年赚 1000 万"传闻，但行业观察认为"肯定能挣到"。无付费课程/知识星球。

**行业警示**：钛媒体报道，中腰部 AI 博主 CPM 在 18 个月内下降 ~40%——"离 AI 越近的创作者，护城河反而越浅。"纯工具介绍型内容的流量窗口正在关闭。

---

### 5.10 郭宇 guoyu.eth — Vibe Coding 一人 SaaS 工厂

| 项目 | 形态 | 解决什么 |
|---|---|---|
| **tuwa.ai** | SaaS（语音） | 双向实时语音翻译（0.3s 延迟、100+ 语言）；PSTN 热线无需 App；支持 agent 接入（自动订餐等）；动态语音克隆 |
| **intentware AI**（第 16 个产品，06-06 beta） | SaaS（语音智能体） | "与另一个你深度聊天"——Mental Model Simulation + 私人数据摄入，语音原生 |
| **wanman**（第 14 个产品，开源） | Agent 工具 | 从手机"接管"其开源项目的 agent |

**创新点**：2026 年已编号发布 ~16 个"vibe product"，全部一人用 AI 编码完成。tuwa.ai 的 PSTN 路线（打电话即用，无需下载）是对"AI 产品必须做 App"假设的反叛。intentware 的"心智模型模拟"把个人数据变成可对话的数字分身。公开演讲："用 AI 经营一人公司""留给知识工作者的窗口期"。

**商业模式**：Freemium 订阅 + 用量计费（tuwa.ai：5 分钟/月免费，Pro/Ultra 付费层）+ X Creator Subscriptions（intentware beta 准入）+ 开源引流（wanman）。Web3 身份（guoyu.eth）暗示 crypto 维度。

---

### 5.11 张小珺 — 中文 AI 创始人访谈档案库

| 项目 | 形态 | 解决什么 |
|---|---|---|
| **《商业访谈录》**（146+ 期） | 超长播客（2-7 小时） | 中文世界最系统的 AI/机器人/消费电子创始人深度访谈 |
| **全球大模型季报** | 定期系列 | 模型进展的结构化追踪 |
| **创投观察 / 投资札记** | 对谈系列 | 戴雨森、Freda Duan 等投资人视角 |

**创新点**：极端时长（谢赛宁 7 小时、阳萌 4 小时、何小鹏多次回访） probing 情绪/目标/成长/战略/决策逻辑，而非产品功能。第三方 GitHub 项目（ai-founder-interviews）用 LLM 系统转录/分析她的访谈——证明其内容已成为行业"一手史料"。杨植麟/Kimi 系列访谈被广泛拆解。

**商业模式**：独立访谈媒体，品牌合作 + 平台分成。无付费课程/社群。多平台分发（YouTube/B站/小宇宙/Spotify/Apple）。

---

### 5.12 实践图谱总览

| 创作者 | 2026 核心实践 | 商业模式 | 规模信号 |
|---|---|---|---|
| Simon Willison | 开源 AI 工具链 + 赞助实验 | 广告/赞助/咨询/演讲 | 20+ 年博客，OSS 生态 |
| Zara Zhang | 18 个开源小工具 + Build for One | 订阅/演讲 | 18 repos，纯个人 |
| Eugene Wei | 战略框架 + 天使投资 | 投资/顾问/订阅 | 10 万+ 订阅，20+ 投资 |
| Dan Shipper | 5 个 AI 产品 + 咨询 | SaaS + 咨询 + 媒体 | $1.2M ARR，Proof 病毒传播 |
| Lenny Rachitsky | PM 教育 + Product Pass | 订阅/合作/赞助/峰会 | 120 万读者，$1M+ 收入 |
| Karpathy | 前沿研究 + 开源教育 + 范式定义 | Anthropic 薪资 + 开源 | 行业级框架，百万级观看 |
| 卫诗婕 | 独立深度访谈（机器人赛道） | 赞助/委托 | 79 期，一人全链路 |
| 硅谷101 | 三线媒体（播客+视频+直播） | 广告/平台分成 | Season 4，公司化运营 |
| 卡兹克 | 一人 AI 内容工厂 | 六位数商单 | 影响力 Top2，万人大会 |
| 郭宇 | 16 个 vibe product（语音 SaaS） | Freemium/订阅/开源 | tuwa.ai 上线即爆 |
| 张小珺 | 超长创始人访谈档案 | 品牌合作/平台 | 146+ 期，行业一手史料 |

**两种 2026 原型**：

- **构建者型**（Simon / Zara / Dan / Karpathy / 郭宇）：以产品/工具/代码为输出，商业模式围绕"造东西"展开。
- **叙事者型**（Eugene / Lenny / 卫诗婕 / 硅谷101 / 卡兹克 / 张小珺）：以内容/框架/访谈为输出，商业模式围绕"讲故事"展开。

**2026 共性趋势**：

1. **一人公司成为默认配置** — 11 人中至少 7 人以一人或极小团队运作，AI 是"隐形联合创始人"。
2. **开源即分发** — Simon/Zara/Karpathy/郭宇/Dan 均用开源获取注意力，再转化为付费。
3. **AI 创作者经济的护城河危机** — 钛媒体数据：中腰部 AI 博主 CPM 18 个月降 40%；纯工具介绍型内容窗口关闭；存活者要么极深（张小珺 7 小时访谈）、要么极快（郭宇 16 个产品）、要么极广（Lenny 120 万读者）。
4. **语音/Agent 是 2026 产品新前线** — 郭宇 tuwa.ai/intentware、Dan Proof、Simon Datasette Agent 不约而同押注"非文本交互"。

---

## 6. H2 阅读建议

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

## 7. 关于本文件

- 首期全量综述，覆盖 2026-01 至 2026-07 全部 11 个信源。
- 英文组中 Dan Shipper / Simon Willison / Lenny / Karpathy 为一手验证；Zara Zhang 为推断；Eugene Wei 无法获取。
- 中文组五源均通过搜索引擎 + 播客平台页面验证。
- 三轴映射基于 frameworks/ai-cognitive-science-three-propositions.md v0.2.0。
- 下一期：2026-W30 周报（2026-07-20 – 2026-07-26）。

*Generated by QoderWork · 2026-07-20*
