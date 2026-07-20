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

| # | Author | Platform | Link | Positioning | Reading Focus |
|---|--------|----------|------|-------------|---------------|
| 1 | Zara Zhang | Substack | [zarazhang.substack.com](https://zarazhang.substack.com) | AI + humanities, Harvard psych, side-project builder | Narrative structure, "build for one" philosophy |
| 2 | Eugene Wei | Substack | [eugenewei.substack.com](https://www.eugenewei.substack.com) | Tech media philosophy, platform evolution | Attention economy, status games, deep thinking |
| 3 | Dan Shipper | Every | [every.to/chain-of-thought](https://every.to/chain-of-thought) | AI-era solo builder, one-person company | Agent deployment practice, workflow design |
| 4 | Simon Willison | Blog | [simonwillison.net](https://simonwillison.net) | Django creator, hands-on AI tools | Tool building, AI evaluation, agentic engineering |
| 5 | Lenny Rachitsky | Newsletter | [lennysnewsletter.com](https://www.lennysnewsletter.com) | Ex-Airbnb PM, product + AI industry | AI product sense, industry case studies |
| 6 | Andrej Karpathy | Substack/Blog | [karpathy.substack.com](https://karpathy.substack.com) | Ex-OpenAI, AGI philosophy | Software 3.0, jagged intelligence, tech philosophy |

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
