# Silicon Valley Daily

[English](#english) | [中文](#中文)

## English

Silicon Valley Daily is a portable agent skill package for producing sourced daily briefings on what happened in Silicon Valley. It is intentionally narrow: the event must happen in Silicon Valley/Bay Area or directly center on a Silicon Valley/Bay Area company, fund, university, lab, or community.

The package first asks the user to choose a focus area, then retrieves, verifies, de-duplicates, ranks, and drafts a Chinese, English, or bilingual brief with citations.

### Portability

This package is designed for agent platforms that support skill-style instruction folders.

The core installable folder is `silicon-valley-daily/`:

- `SKILL.md` contains the trigger description and operating workflow.
- `references/` contains source strategy, watchlists, and report templates loaded as needed.
- `agents/openai.yaml` is optional UI metadata for compatible platforms. Platforms that do not support this file can ignore it.

The host platform should provide web search, browser access, X/Twitter access, or another current-news retrieval tool. Without live retrieval, the agent should say the brief cannot be verified instead of inventing current events.

For platforms that import one skill folder at a time, install or upload `silicon-valley-daily/` rather than the whole repository.

### What It Does

- Starts with a focus-selection interaction unless the user already specified a focus.
- Produces sourced daily briefs about Silicon Valley and local Bay Area tech actors.
- Excludes global tech news unless a Silicon Valley/Bay Area actor is the central subject.
- Supports Chinese, English, and bilingual output.
- Supports panorama briefs and focused briefs.
- Separates confirmed facts, lower-confidence signals, and excluded noise.
- Includes a built-in source stack and X/Twitter watchlist for discovery.

### Usage Flow

User asks:

```text
What happened in Silicon Valley today?
```

The agent asks for focus first:

```text
Which Silicon Valley Daily mode do you want? Pick one main mode, optionally with one extra focus:

1. Panorama: scan all areas and list important news by section
2. AI models and infrastructure
3. Startups, funding, and M&A
4. Big Tech, platforms, and developer ecosystem
5. VC, accelerators, and talent flows
6. Policy, litigation, and security
7. Founder and operator signals
8. Local Bay Area ecosystem, universities, events, and communities

Reply with a number, such as "1" or "1 + 2", or describe what you care about most.
```

After the user confirms, the agent researches and drafts the brief.

### Focus Areas

- Panorama
- AI models and infrastructure
- Startups, funding, and M&A
- Big Tech, platforms, and developer ecosystem
- VC, accelerators, and talent flows
- Policy, litigation, and security
- Founder and operator signals
- Local Bay Area ecosystem, universities, events, and communities

### Example Prompts

```text
What happened in Silicon Valley today?
```

```text
Use Silicon Valley Daily for a panorama brief on Silicon Valley today.
```

```text
Use Silicon Valley Daily for today's Silicon Valley brief, focused on AI infrastructure and startup funding.
```

```text
Use Silicon Valley Daily for a bilingual founder/investor brief on Silicon Valley today.
```

If your platform supports explicit skill tags:

```text
Use $silicon-valley-daily to brief me on what happened in Silicon Valley today in Chinese.
```

### Output Shape

A panorama brief is not a mixed news feed. It should be sectioned:

```markdown
# What Happened in Silicon Valley Today

Reporting window: ...
Focus: Panorama

## Executive Takeaway

...

## Top Stories

1. **Headline**
   What happened: ...
   Why it matters: ...
   Who is affected: founders / investors / developers / Big Tech / users
   Confidence: high / medium / low
   Source: [Source](https://example.com)

## By Sector

### AI Models and Infrastructure

- **Headline**: What happened. Why it matters. Source: [Source](https://example.com)

### Startups, Funding, and M&A

- **Headline**: Key facts such as amount, round, investors, buyer, or strategic rationale. Source: [Source](https://example.com)

### Big Tech, Platforms, and Developer Ecosystem

- **Headline**: Platform, customer, developer, or competitive impact. Source: [Source](https://example.com)

### VC, Accelerators, and Talent Flows

- No high-signal update today: checked VC announcements, reputable media, and hiring/personnel signals.

### Policy, Litigation, and Security

- **Headline**: Risk, regulatory milestone, or security event. Source: [Source](https://example.com)

### Founder and Operator Signals

- **Headline**: Pricing, GTM, customer adoption, hiring, or developer feedback. Source: [Source](https://example.com)

### Local Bay Area Ecosystem

- No high-signal update today.

## Signals to Watch

- ...

## Source Notes

- Verified sources: ...
- Low-confidence or excluded items: ...
```

### Package Files

- `silicon-valley-daily/SKILL.md`: Trigger description and core workflow.
- `silicon-valley-daily/references/source-strategy.md`: Source tiers, focus taxonomy, and ranking rules.
- `silicon-valley-daily/references/watchlist.md`: Built-in source stack, daily research methods, and X/Twitter watchlist.
- `silicon-valley-daily/references/report-formats.md`: Chinese, English, and bilingual report templates.
- `silicon-valley-daily/agents/openai.yaml`: Optional UI metadata for compatible platforms.

## 中文

Silicon Valley Daily 是一个可跨平台安装的 agent skill package，用来生成「硅谷每天发生了什么」日报。

它的产品边界是小而美：事件必须发生在硅谷/湾区，或核心主体是硅谷/湾区公司、基金、大学、实验室、社区。只是泛科技相关、只是 AI 很热、只是某个硅谷 VC 参投外地公司，默认不收录。

这个 package 会先让用户选择关注范围，再检索、核验、去重、排序，并输出带来源的中文、英文或中英双语简报。

### 跨平台说明

这个仓库面向支持 skill-style instruction folder 的 agent 平台。

核心安装对象是 `silicon-valley-daily/` 文件夹：

- `SKILL.md`：触发描述和核心工作流。
- `references/`：按需加载的信源策略、关注名单和报告模板。
- `agents/openai.yaml`：可选 UI metadata。平台不支持时可以忽略。

宿主平台需要提供网页搜索、浏览器访问、X/Twitter 访问，或其他实时新闻检索能力。没有实时检索能力时，agent 应该说明无法核验，而不是编造当天新闻。

如果某个平台一次只能导入一个 skill 文件夹，请导入 `silicon-valley-daily/`，不要导入整个仓库。

### 功能

- 如果用户没有提前指定关注范围，先发起关注范围选择。
- 生成带来源的硅谷和本地湾区科技主体日报。
- 排除泛全球科技新闻，除非核心主体是硅谷/湾区主体。
- 支持中文、英文和中英双语输出。
- 支持全景版和聚焦版。
- 区分已确认事实、低可信信号和未纳入噪音。
- 内置可信信源栈和 X/Twitter 关注名单，用于发现线索。

### 使用流程

用户问：

```text
硅谷今天发生了什么？
```

Agent 不会马上开始搜，而是先问：

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

用户确认后，agent 再开始检索、核验和输出。

### 可选关注范围

- 全景版
- AI 模型与基础设施
- 创业公司、融资与并购
- 大厂、平台与开发者生态
- VC、孵化器与人才流动
- 政策、诉讼与安全
- 创始人和经营信号
- 湾区本地生态、大学、活动与社区

### 示例 prompt

```text
硅谷今天发生了什么？
```

```text
使用 Silicon Valley Daily，做一份今天的硅谷日报，选全景版。
```

```text
使用 Silicon Valley Daily，做一份今天的硅谷日报，重点看 AI 基础设施和创业融资。
```

```text
使用 Silicon Valley Daily，做一份今天的创始人/投资人版中英双语硅谷日报。
```

如果平台支持显式 skill tag，也可以：

```text
Use $silicon-valley-daily to brief me on what happened in Silicon Valley today in Chinese.
```

### 输出样式

全景版不是混合新闻流，而是分领域输出：

```markdown
# 硅谷今天发生了什么

报告窗口：...
本次关注范围：全景版

## 一句话总览

...

## 最值得看的 5 件事

1. **标题**
   发生了什么：...
   为什么重要：...
   影响对象：创始人 / 投资人 / 开发者 / 大厂 / 用户
   可信度：高 / 中 / 低
   来源：[Source](https://example.com)

## 分领域简报

### AI 模型与基础设施

- **标题**：发生了什么。为什么重要。来源：[Source](https://example.com)

### 创业、融资与并购

- **标题**：金额、轮次、投资方、并购方或战略意义。来源：[Source](https://example.com)

### 大厂、平台与开发者生态

- **标题**：平台、客户、开发者或竞争格局影响。来源：[Source](https://example.com)

### VC、孵化器与人才流动

- 今日无高信号：已检查 VC/孵化器公告、可信媒体和公开招聘/人事信号，未发现足够重要的新进展。

### 政策、诉讼与安全

- **标题**：风险、监管节点或安全事件。来源：[Source](https://example.com)

### 创始人和经营信号

- **标题**：定价、GTM、客户采用、岗位变化或开发者反馈。来源：[Source](https://example.com)

### 湾区本地生态、大学、活动与社区

- 今日无高信号：未发现足够重要的新进展。

## 接下来值得盯的信号

- ...

## 信源说明

- 已核验来源：...
- 低可信或未纳入事项：...
```

### 文件结构

- `silicon-valley-daily/SKILL.md`：触发描述和核心工作流。
- `silicon-valley-daily/references/source-strategy.md`：信源分层、关注分类和排序规则。
- `silicon-valley-daily/references/watchlist.md`：内置信源栈、每日检索方法和 X/Twitter 关注名单。
- `silicon-valley-daily/references/report-formats.md`：中文、英文和中英双语报告模板。
- `silicon-valley-daily/agents/openai.yaml`：兼容平台可用的可选 UI metadata。
