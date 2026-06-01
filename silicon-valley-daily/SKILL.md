---
name: silicon-valley-daily
description: "Produce a sourced Chinese, English, or bilingual daily briefing on Silicon Valley, Bay Area, and US tech/startup events. Use when users ask what happened in Silicon Valley today, 硅谷今天发生了什么, 硅谷日报, Silicon Valley daily digest, daily AI/startup/VC news briefings, startup funding or M&A updates, founder or investor intelligence, or a concise morning/evening digest with citations."
---

# Silicon Valley Daily

## Overview / 概览

Create a reliable daily intelligence brief about Silicon Valley: what happened, why it matters, who is affected, and what to watch next.

生成一份可信、带来源的硅谷日报：今天发生了什么、为什么重要、影响谁、接下来该盯什么。默认用中文输出；如果用户用英文提问或明确要求 English/bilingual，则输出英文或中英双语。

## Core Workflow / 核心流程

1. Define the reporting window / 定义报道窗口。If the user says "today", use the user's current date and timezone, then also state the corresponding Pacific Time window because Silicon Valley news often lands on PT.
2. Select focus first / 先选择关注范围。If the user has not already specified a focus, ask the focus question below and stop. Do not research or draft the brief until the user chooses a focus.
3. Confirm and proceed / 确认后再执行。After the user chooses, briefly confirm the selected focus and reporting mode, then research. Do not ask for a second confirmation unless the user's choice is ambiguous.
4. Gather source-backed items / 采集有来源支撑的信息。Use available web/search/browser tools. If live web access is unavailable, state that the brief cannot be verified rather than inventing current events.
5. Search broadly first, then target primary sources / 先广搜，再查一手来源。Read `references/source-strategy.md` when gathering sources, ranking signals, or deciding whether an item belongs in the brief.
6. Cluster duplicate coverage / 合并重复报道。Prefer the earliest primary source plus one reputable independent source when available.
7. Rank items / 排序筛选。Rank by impact, novelty, credibility, Silicon Valley relevance, actionability, and the user's selected focus. Include fewer, stronger items rather than a long feed of weak mentions.
8. Draft in the requested language and format / 按用户要求输出。Read `references/report-formats.md` when drafting the final report or adapting it for different audiences.
9. Cite every factual item / 每个事实都给来源。Use absolute dates, distinguish confirmed facts from rumors, and call out notable gaps in coverage.

## Interaction Contract / 交互规则

For broad requests such as "硅谷今天发生了什么" or "What happened in Silicon Valley today", ask this first:

```text
你想看哪种硅谷日报？选 1 个主模式，也可以加 1 个重点方向：

1. 全景版：各领域都扫一遍，按板块列出重要新闻
2. AI 模型与基础设施
3. 创业公司、融资与并购
4. 大厂、平台与开发者生态
5. VC、孵化器与人才流动
6. 政策、诉讼与安全
7. 创始人和经营信号
8. 湾区本地生态、大学、活动与社区

你可以回复编号，比如「1」或「1 + 2」，也可以直接说你最关心什么。
```

If the user already says "重点看 AI 和融资" or "founder/investor brief", skip the menu, confirm the focus in one sentence, and proceed.

If the user selects "全景版 / panorama", produce a category-by-category report covering every focus area. Include "今日无高信号" for a category only after checking it; do not fill empty categories with weak news.

## Focus Areas / 关注范围

Use the same focus taxonomy in the interaction menu, source gathering, ranking, and final report:

- AI models and infrastructure / AI 模型与基础设施
- Startups, funding, and M&A / 创业公司、融资与并购
- Big Tech and platforms / 大厂、平台与开发者生态
- VC, accelerators, and talent flows / VC、孵化器与人才流动
- Policy, litigation, and security / 政策、诉讼与安全
- Founder/operator signals / 创始人和经营信号
- Local Bay Area ecosystem / 湾区本地生态、大学、活动与社区

## Reporting Modes / 报告模式

- Quick / 快讯：after focus selection, 5 to 8 bullets, each with one source and a short "why it matters".
- Panorama / 全景版：top takeaway plus sectioned lists for all focus areas.
- Standard / 标准日报：executive summary, ranked top stories, category sections, watchlist, and source ledger.
- Deep / 深度版：standard brief plus implications for founders, investors, operators, or a named company/category.
- Focused / 聚焦版：prioritize 1 to 2 selected focus areas and summarize other categories only if they contain major events.
- English / 英文版：same structure as standard, written for global readers.
- Bilingual / 双语版：Chinese main text with English proper nouns, or Chinese bullets followed by short English summaries.

## Inclusion Rules / 收录规则

Include an item when it changes how a founder, investor, builder, operator, or tech observer understands the day. Strong examples include product launches, model or infrastructure releases, funding rounds, M&A, layoffs and hiring shifts, regulatory actions, litigation, notable security incidents, platform policy changes, developer ecosystem shifts, and high-signal AI or startup research.

只有当一件事会改变创始人、投资人、开发者、运营者或科技观察者对当天的判断时，才收录。不要收录普通 PR、例行高管发言、股价日常波动、重复转载、未核实爆料，或没有新增事实的旧新闻。

## Verification Rules / 核验规则

- Treat company blogs, official filings, regulator/court documents, product changelogs, and direct announcements as primary sources.
- Treat reputable media and specialist newsletters as context, not automatic confirmation.
- Treat social posts, forums, and anonymous tips as leads until corroborated.
- If only low-confidence sources exist, either omit the item or label it clearly as unconfirmed.
- Never fabricate citations, dates, figures, or source titles. If a fact cannot be verified, say so plainly.

## Output Principles / 输出原则

- Lead with synthesis, not a link dump.
- Translate technical events into consequences: customer behavior, competitive positioning, fundraising climate, platform risk, developer opportunity, or policy pressure.
- Keep proper nouns accurate in English. Explain unfamiliar names briefly in Chinese.
- Prefer concise Chinese paragraphs and scannable bullets.
- When writing in English, keep the same analytical structure and avoid newsletter-style hype.
- End with "接下来值得盯的信号" when useful.
