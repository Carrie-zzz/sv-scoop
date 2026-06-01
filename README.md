# Silicon Valley Daily

Daily Silicon Valley tech and startup intelligence skill.

这是一个用于生成「硅谷每天发生了什么」的 Codex skill。它会检索、核验、去重并排序硅谷、湾区科技公司、AI、创业、VC、大厂平台、政策安全等信息，最后输出带来源的中文、英文或中英双语简报。

## What It Does

- Produces sourced daily briefs about Silicon Valley and Bay Area tech.
- Supports Chinese, English, and bilingual output.
- Handles broad daily overviews and focused reports.
- Asks the user to choose focus areas when the topic is too broad or meant for recurring use.
- Separates confirmed facts, lower-confidence signals, and excluded noise.

## 使用流程

### 1. 用户直接问

```text
硅谷今天发生了什么？
```

默认输出「全景版」：先给当天最重要的 5 件事，再按类别整理。

### 2. 如果信息太多，用户可以指定方向

```text
每天早上给我一份硅谷日报，我主要关注 AI 和创业融资。
```

skill 会优先覆盖用户选择的 1-2 个方向，并只保留其他类别里的重大事件。

### 3. 如果用户没有选择方向，但场景适合长期订阅

skill 会先问一句：

```text
硅谷每天信息量比较大。你希望我之后优先关注哪 1-2 块？
可选：AI 模型与基础设施、创业公司/融资/并购、大厂与平台生态、VC/孵化器/人才流动、政策/诉讼/安全、创始人经营信号、湾区本地生态。
```

### 4. 可选关注范围

- AI models and infrastructure / AI 模型与基础设施
- Startups, funding, and M&A / 创业公司、融资与并购
- Big Tech and platforms / 大厂、平台与开发者生态
- VC, accelerators, and talent flows / VC、孵化器与人才流动
- Policy, litigation, and security / 政策、诉讼与安全
- Founder/operator signals / 创始人和经营信号
- Local Bay Area ecosystem / 湾区本地生态、大学、活动与社区

## Example Prompts

```text
Use $silicon-valley-daily to brief me on what happened in Silicon Valley today in Chinese.
```

```text
用 $silicon-valley-daily 做一份今天的硅谷日报，重点看 AI 基础设施和创业融资。
```

```text
Use $silicon-valley-daily for a bilingual founder/investor brief on Silicon Valley today.
```

## Output Format Example

The example below shows the format only. Real briefs must be generated with live sources.

```markdown
# 硅谷今天发生了什么

报告窗口：2026-06-01 08:00 至 2026-06-01 18:00（Asia/Shanghai）；对应 Pacific Time：2026-05-31 17:00 至 2026-06-01 03:00
覆盖范围：硅谷、湾区科技公司、AI/创业/VC，以及影响硅谷生态的美国科技事件
本次关注范围：AI 模型与基础设施、创业融资与并购

## 一句话总览

今天最重要的变化是：AI 基础设施和资本流向继续集中到少数高确定性平台，创业公司需要更清楚地证明分发、成本或数据优势。

## 最值得看的 5 件事

1. **某 AI 平台发布新的开发者能力**
   发生了什么：公司发布了新的 API、模型或工具链更新。
   为什么重要：这可能改变开发者构建 AI 应用的成本结构和产品边界。
   影响对象：开发者 / AI 创业公司 / 企业客户
   可信度：高
   来源：[Company Blog](https://example.com)

2. **某湾区创业公司完成新一轮融资**
   发生了什么：公司宣布融资金额、轮次和主要投资方。
   为什么重要：说明资本仍在流向具备明确商业化路径的细分方向。
   影响对象：创始人 / 投资人
   可信度：高
   来源：[Funding Announcement](https://example.com)

## 分领域简报

### AI 模型与基础设施

- **标题**：发生了什么。为什么重要。来源：[Source](https://example.com)

### 创业、融资与并购

- **标题**：金额、轮次、投资方、并购方或战略意义。来源：[Source](https://example.com)

### 其他重要信号

- **标题**：不属于本次重点，但足够重要，所以保留。来源：[Source](https://example.com)

## 接下来值得盯的信号

- 是否有开发者从旧平台迁移到新工具链。
- 新融资公司是否能披露真实客户、收入或使用量。
- 大厂平台政策是否改变创业公司的分发和成本结构。

## 信源说明

- 已核验来源：公司公告、监管/备案文件、可信媒体报道。
- 低可信或未纳入事项：未被一手来源或可信媒体确认的社交媒体爆料。
```

## Skill Files

- `silicon-valley-daily/SKILL.md`: Trigger description and core workflow.
- `silicon-valley-daily/references/source-strategy.md`: Source tiers, focus taxonomy, and ranking rules.
- `silicon-valley-daily/references/report-formats.md`: Chinese, English, and bilingual report templates.
- `silicon-valley-daily/agents/openai.yaml`: UI metadata.
