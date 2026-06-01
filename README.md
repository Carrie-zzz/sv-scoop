# Silicon Valley Daily

Daily Silicon Valley tech and startup intelligence skill.

这是一个用于生成「硅谷每天发生了什么」的 Codex skill。它会先让用户选择关注范围，再检索、核验、去重并排序硅谷、湾区科技公司、AI、创业、VC、大厂平台、政策安全等信息，最后输出带来源的中文、英文或中英双语简报。

## What It Does

- Starts with a focus-selection interaction unless the user already specified a focus.
- Produces sourced daily briefs about Silicon Valley and Bay Area tech.
- Supports Chinese, English, and bilingual output.
- Supports panorama briefs and focused briefs.
- Separates confirmed facts, lower-confidence signals, and excluded noise.

## 使用流程

### 1. 用户直接问

```text
硅谷今天发生了什么？
```

skill 不会马上开始搜，而是先问：

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

用户确认后，skill 再开始检索、核验和输出。

### 2. 用户指定方向

```text
每天早上给我一份硅谷日报，我主要关注 AI 和创业融资。
```

skill 会确认：

```text
好的，这次按「AI 模型与基础设施 + 创业融资与并购」来做。我会先核验来源，再按重要性排序输出。
```

然后优先覆盖用户选择的 1-2 个方向，并只保留其他类别里的重大事件。

### 3. 用户选择全景版

全景版不是混合新闻流，而是分领域输出。每个板块都要检查，有高信号就列新闻，没有就说明「今日无高信号」。

### 4. 可选关注范围

- Panorama / 全景版
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
用 $silicon-valley-daily 做一份今天的硅谷日报，选全景版。
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
本次关注范围：全景版

## 一句话总览

今天最重要的变化是：AI 基础设施、平台政策和创业融资仍在互相影响，创始人需要同时看技术供给、分发入口和资本信号。

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
