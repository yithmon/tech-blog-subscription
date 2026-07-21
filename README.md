# Tech Blog Subscription Hub

Personal curated tech blog/newsletter subscription tracker. Focused on AI cognition, individual builders, and tech-humanities intersection.

**Owner:** yithmon (Cognitive Psychology | Data Scientist | Human-AI ‌collaboration‌)
**Started:** 2026-07-18
**Update cadence:** Weekly digest (every Friday)

## Structure

```
.
├── README.md              # This file - subscription list & reading guide
├── frameworks/            # Foundational thinking frameworks (long-lived, extensible)
│   └── ai-cognitive-science-three-propositions.md  # 3-proposition coordinate system
├── reviews/               # Periodic content reviews
│   └── 2026-H1-review.md # 2026 H1 comprehensive review
├── digests/               # Weekly digests (auto-generated)
│   └── 2026-W29.md       # First issue (scaffold + H1-review seed)
├── config/
│   └── sources.yaml       # Machine-readable subscription config (drives automation)
├── scripts/
│   └── generate_digest.py # Weekly digest generator (zero-dep, reads sources.yaml)
└── .github/workflows/
    └── weekly-digest.yml  # Scheduled: every Fri 16:00 Asia/Shanghai
```

## Subscription List

### English (Priority)

#### Core Seeds

| # | Author | Platforms | Positioning | Reading Focus |
|---|--------|-----------|-------------|---------------|
| 1 | Zara Zhang | [Substack](https://zarazhang.substack.com) · [X @ZaraZhangRui](https://x.com/ZaraZhangRui) · [GitHub](https://github.com/zarazhangrui) | AI + humanities, Harvard psych, side-project builder | Narrative structure, "build for one" philosophy |
| 2 | Eugene Wei | [Substack](https://www.eugenewei.substack.com) · [X @eugenewei](https://x.com/eugenewei) | Tech media philosophy, platform evolution | Attention economy, status games, deep thinking |
| 3 | Dan Shipper | [Every.to](https://every.to/chain-of-thought) · [X @danshipper](https://x.com/danshipper) · [YouTube: AI & I](https://www.youtube.com/@aiandishow) | AI-era solo builder, one-person company | Agent deployment practice, workflow design |
| 4 | Simon Willison | [Blog](https://simonwillison.net) · [X @simonw](https://x.com/simonw) · [GitHub](https://github.com/simonw) · [Substack](https://simonw.substack.com) | Django creator, hands-on AI tools | Tool building, AI evaluation, agentic engineering |
| 5 | Lenny Rachitsky | [Newsletter](https://www.lennysnewsletter.com) · [X @lennysrachitsky](https://x.com/lennysrachitsky) · [YouTube](https://www.youtube.com/@LennyRachitsky) · [Podcast](https://www.lennyspodcast.com/) · [Community](https://www.lennysnewsletter.com/p/community) | Ex-Airbnb PM, product + AI industry | AI product sense, industry case studies |
| 6 | Andrej Karpathy | [Substack](https://karpathy.substack.com) · [X @karpathy](https://x.com/karpathy) · [GitHub](https://github.com/karpathy) · [YouTube](https://www.youtube.com/@AndrejKarpathy) | Ex-OpenAI/Anthropic, AGI philosophy | Software 3.0, jagged intelligence, tech philosophy |

#### AI Engineering Practice

| # | Author | Platforms | Positioning | Reading Focus |
|---|--------|-----------|-------------|---------------|
| 7 | Addy Osmani | [Blog](https://addyosmani.com/blog/) · [X @addyosmani](https://x.com/addyosmani) · [GitHub](https://github.com/addyosmani) | Google Chrome/Gemini eng lead; agentic coding at scale | Agent orchestration, loop engineering, production patterns |
| 8 | Eugene Yan | [Blog](https://eugeneyan.com/) · [X @eugeneyan](https://x.com/eugeneyan) · [GitHub](https://github.com/eugeneyan) | Anthropic MTS; applied-llms.org co-author | LLM production architecture, evals, reusable patterns |
| 9 | Jason Liu | [Blog](https://jxnl.co/) · [X @jxnlco](https://x.com/jxnlco) · [GitHub](https://github.com/jxnl) | Instructor lib author; structured LLM outputs | Agent architecture, contrarian takes with working code |
| 10 | Hamel Husain | [Blog](https://hamel.dev/) · [X @HamelHusain](https://x.com/HamelHusain) · [Substack](https://hamelhusain.substack.com/) · [GitHub](https://github.com/hamelsmu) | Evals specialist; Parlance Labs; OSS ML tooling | AI measurement, debugging, "does it actually work?" |
| 11 | swyx (Shawn Wang) | [Latent Space](https://www.latent.space/) · [X @swyx](https://x.com/swyx) · [ai.engineer](https://www.ai.engineer/) | "AI Engineer" movement founder; AINews daily | Field mapping, who's building what, emerging patterns |

#### AI Product & Design

| # | Author | Platforms | Positioning | Reading Focus |
|---|--------|-----------|-------------|---------------|
| 12 | Julie Zhuo | [Substack: The Looking Glass](https://lg.substack.com/) · [X @joulee](https://x.com/joulee) | Ex-Meta VP Design (13yr); AI taste & craft | AI × design judgment, product craft in AI era |
| 13 | Sachin Rekhi | [Substack](https://www.sachinrekhi.com/) · [X @sachinrekhi](https://x.com/sachinrekhi) | AI-era PM practitioner frameworks | Hands-on AI PM craft, prototyping, ops |

#### AI + Cognitive Science

| # | Author | Platforms | Positioning | Reading Focus |
|---|--------|-----------|-------------|---------------|
| 14 | Dan Williams | [Substack: Conspicuous Cognition](https://www.conspicuouscognition.com/) · [X @danwilliams](https://x.com/danwilliams) · [Podcast](https://www.conspicuouscognition.com/) | Cognitive scientist; AI × metacognition research | What AI does to human thinking, cognitive offloading |
| 15 | Amanda Askell | [X @AmandaAskell](https://x.com/AmandaAskell) · [Blog](https://askell.io/) | Anthropic Claude character designer; philosophy PhD | AI character/values, philosophy of mind in practice |
| 16 | Eva Keiffenheim | [Substack](https://evakeiffenheim.substack.com/) · [X @EvaKeiffenheim](https://x.com/EvaKeiffenheim) | Learning sciences MSc; AI × creativity & cognition | AI's cognitive impact, collective creativity, learning |

#### Indie AI Builders

| # | Author | Platforms | Positioning | Reading Focus |
|---|--------|-----------|-------------|---------------|
| 17 | Marc Lou | [Newsletter: Just Ship It](https://newsletter.marclou.com/) · [X @marc_louvion](https://x.com/marc_louvion) · [shipfa.st](https://shipfa.st/) | 35+ startups in 4yr; $1M+ revenue; AI-first micro-SaaS | Solo builder economics, ship-fast, revenue-transparent |
| 18 | Thorsten Ball | [Newsletter: Register Spill](https://registerspill.thorstenball.com/) · [X @thorstenball](https://x.com/thorstenball) · [GitHub](https://github.com/tsball) | Ex-Zed (built coding agents); implementation depth | Building agents (not using them), code + beauty |

### Chinese

| # | Author | Platform | Link | Positioning | Reading Focus |
|---|--------|----------|------|-------------|---------------|
| 1 | 卫诗婕 | WeChat + Podcast | 小宇宙: 卫诗婕｜漫谈Light the Star | Deep industry long-form + founder interviews | AI industry narrative, business case-study |
| 2 | 硅谷101 陈茜 | WeChat + Podcast | 小宇宙: 硅谷101 | China-US AI comparison, Silicon Valley intel | Industry economics, compute geopolitics |
| 3 | 数字生命卡兹克 | WeChat + X | X: @Rockhazix | Design-background AI individual builder | AI workflow, side-project practice, open-source |
| 4 | 郭宇 | X + Mirror | X: @turingou | Ex-ByteDance, tech aesthetics, AI-era choices | Knowledge work future, individual choices |
| 5 | 张小珺 | WeChat + Podcast | 小宇宙: 张小珺Jùn｜商业访谈录 | Ultra-deep interviews, AI capital narrative | Power structures behind tech, 3h+ deep dives |

## Weekly Reading Priority

1. **Simon Willison** - experiments + AI thinking (most aligned with evaluation work)
2. **Zara Zhang** - narrative paradigm reference
3. **Eugene Wei** - elevate media/humanity-level thinking
4. **数字生命卡兹克 / 卫诗婕** - domestic AI industry perspective

## Tips

- Substack: subscribe to free tier only; paid unlocks deep columns
- Read in weekly batches, avoid fragmented scrolling
- Focus on their structure: question -> reasoning -> small project validation

## 周刊如何运作 (Weekly Digest)

周刊是**脚手架 + 手填批注**的混合体：脚本负责把「本周该读谁、在三轴上该看什么位」自动排好，真实批注由 owner 每周读完手填（对应 frameworks 里的「我的批注」占位）。

**自动生成（CI）**
- `.github/workflows/weekly-digest.yml` 每周五 16:00 (Asia/Shanghai) 触发，运行 `scripts/generate_digest.py`，把新周刊提交到 `digests/YYYY-Www.md`。
- 频率规则：`daily` / `weekly` 源每周纳入；`monthly` 源约每 4 周纳入一次（ISO 周号 % 4 == 1）。
- 来源清单、优先级、频率全部来自 `config/sources.yaml`，改配置即改周刊，无需动脚本。

**本地手动生成**
```bash
python scripts/generate_digest.py                 # 最近一个已结束的周
python scripts/generate_digest.py --week 2026-W29 # 指定周
python scripts/generate_digest.py --dry-run       # 只预览不写文件
```
脚本零外部依赖（内置 YAML 子集解析，优先用 PyYAML），本地与 CI 均可直接跑。

**每期结构**
1. 本周阅读清单（按优先级 + 频率筛选，含预计时长）
2. 三命题坐标 · 本周落点（待填）
3. 逐源笔记位（三轴定位 / 补了哪块 / 我的批注）
4. 跨源信号（待填）
5. 关于本文件（自动化说明）
