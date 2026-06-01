# Source Strategy

Use this reference when researching, verifying, and ranking Silicon Valley daily brief items.

## Scope / 地理与主体边界

This skill is intentionally narrow. It covers events that happened in Silicon Valley or directly involve Silicon Valley/Bay Area tech actors. It is not a general US tech or global AI digest.

Default geography:

- Silicon Valley core: Palo Alto, Menlo Park, Mountain View, Sunnyvale, Santa Clara, Cupertino, San Jose, Redwood City, San Mateo, Stanford, and nearby Santa Clara/San Mateo County startup corridors.
- Bay Area tech ecosystem when relevant: San Francisco, Berkeley, Oakland, Emeryville, Fremont, San Bruno, South San Francisco, and other Bay Area locations only when the event is clearly part of the local tech/startup ecosystem.

Silicon Valley Test:

- Location: the event physically happened in the Silicon Valley/Bay Area tech ecosystem.
- Actor: the central company, fund, lab, university, community, or product team is based in Silicon Valley/Bay Area.
- Capital: the funding, M&A, fund, or partner move centers on a Silicon Valley/Bay Area company, fund, or partner.
- Local ecosystem: the event involves Stanford, Berkeley, YC, Bay Area events, Bay Area hiring/layoffs, office moves, local regulation, or local startup community changes.

Hard exclusions:

- Do not include non-Bay-Area events merely because they are AI, startup, VC, or Big Tech news.
- Do not include a New York, London, Paris, Beijing, Singapore, or remote-first company's funding round just because a Silicon Valley VC participated.
- Do not include a Washington policy item, global chip rule, cloud outage, earnings report, or product launch unless a Silicon Valley/Bay Area actor is the central subject and there is a concrete local event or direct local action.
- Do not include broad stock moves or market commentary unless tied to a local company action, filing, layoff, product, lawsuit, or acquisition.

## Time Window

Default to the user's "today" in their timezone, then map it to Pacific Time. Timezone conversion does not expand the geographic scope. If the user is in Asia, a useful reporting window often spans:

- Asia morning brief: previous Pacific calendar day.
- Asia evening brief: current Pacific morning through the latest available verified local updates.
- US morning brief: previous 24 hours ending at report time.

Always state the exact reporting window in the final report.

## Source Tiers

Tier 1 primary sources:

- Company newsroom, blog, product release notes, changelog, developer docs, status pages
- SEC filings, investor relations pages, court filings, regulator statements, official government pages
- Direct funding or acquisition announcements from company, investor, accelerator, or acquirer
- GitHub releases, model cards, technical reports, research lab publications
- Official posts from named executives, founders, researchers, or product leads

Tier 2 reputable context sources:

- Reuters, Bloomberg, Wall Street Journal, Financial Times, CNBC, New York Times
- TechCrunch, The Verge, Wired, Semafor, The Information, Axios, Fortune
- Platformer, Stratechery, Ben Thompson, Import AI, Latent Space, The Batch, or other specialist publications when relevant
- Local Bay Area business or university sources for regional developments

Tier 3 signal sources:

- Hacker News, Reddit, X/Twitter, LinkedIn, Discord or Slack community chatter, Product Hunt, app store rankings, job posts, vendor forums
- Use these for discovery and color. Do not treat them as confirmation unless the source is official or corroborated.

## Search Pattern

Start broad, then narrow:

1. Search for date-bound local queries: "Silicon Valley startup today", "Bay Area startup funding", "San Francisco AI startup", "Palo Alto startup", "Mountain View AI", "Menlo Park VC", "San Jose tech layoffs".
2. Search category queries with local filters: "startup funding San Francisco", "Bay Area acquisition startup", "Silicon Valley AI model release", "San Francisco developer platform launch", "Menlo Park venture capital", "Stanford startup".
3. Search primary source domains for high-signal companies and institutions.
4. Search social and community sources only after building a primary-source baseline.
5. For each candidate, search the company or person's name plus the claimed event and location/HQ to confirm date, details, and Silicon Valley fit.

## Focus Taxonomy

Use this taxonomy to avoid overloading the user. If the user chooses focus areas, spend most research and output space there. If the user does not choose, use a balanced overview and cap each category tightly.

AI models and infrastructure:

- Frontier model releases, evals, pricing, API changes, chips, datacenters, cloud capacity, AI developer tools, open-source models, research with near-term product implications. Include only when the lab, product team, datacenter decision, company, or event is Silicon Valley/Bay Area-centered.

Startups, funding, and M&A:

- Seed through growth rounds, shutdowns, acquisitions, spinouts, accelerator batches, notable pivots, customer traction, category formation. The target company or core transaction subject must be Silicon Valley/Bay Area, not merely backed by a Silicon Valley investor.

Big Tech and platforms:

- Apple, Google, Meta, Nvidia, OpenAI, Anthropic, xAI, Databricks, Snowflake, Salesforce, Stripe, and other Silicon Valley/Bay Area-centered platform companies. For non-local giants such as Microsoft or Amazon, include only when the event centers on their Bay Area team, local office, local acquisition, local hiring/layoff, or direct transaction with a Silicon Valley/Bay Area actor.

VC, accelerators, and talent flows:

- Silicon Valley/Bay Area fund formation, partner moves, accelerator batches, major founder departures, hiring freezes, layoffs, compensation shifts, immigration/talent constraints, university lab-to-startup movement.

Policy, litigation, and security:

- Local or actor-specific AI regulation, antitrust, copyright, privacy, export controls, court rulings, regulator actions, major breaches, platform abuse, supply-chain security. Include only when a Silicon Valley/Bay Area actor is central.

Founder/operator signals:

- GTM shifts, pricing models, enterprise adoption, developer adoption, customer complaints, procurement changes, job postings, community discussion with corroborating evidence.

Local Bay Area ecosystem:

- Stanford/Berkeley research commercialization, major events, local real estate or office moves, city/regional policy, startup community changes.

## Default Allocation

For a panorama brief, every category is part of the product experience:

- Start with 3 to 5 cross-category top stories.
- Then include all focus areas as sections.
- Put 1 to 3 verified items in each non-empty section.
- For categories with no high-signal updates, write "今日无高信号" and optionally name the type of sources checked.
- Do not move normal category items into "other important signals"; reserve that section for events outside the selected focus or taxonomy.

For a focused brief:

- Put 60 to 80 percent of the report into the selected focus areas.
- Include a small "其他重要信号 / Other important signals" section for major out-of-focus events.
- Explicitly state the selected focus at the top of the report.

For a quick brief:

- Still require focus selection first unless the user already provided it.
- If the user chooses panorama, include one strongest item per active category.

## Ranking Rubric

Use the rubric to prioritize. It does not need to appear in the final report.

- Impact, 0 to 3: affects many users, developers, customers, employees, investors, or competitors.
- Novelty, 0 to 2: new fact, not a repackage of older news.
- Credibility, 0 to 2: primary source or multiple reputable confirmations.
- Silicon Valley fit, 0 to 3: event location, central actor, or transaction subject is clearly Silicon Valley/Bay Area.
- Actionability, 0 to 1: changes what someone should watch, build, buy, sell, hire for, or investigate.
- Focus fit, 0 to 2: strongly matches the user's selected category or audience.

Lead with items scoring 8 or higher in panorama briefs, or 9 or higher when the day is crowded. Discard any item with Silicon Valley fit below 2, even if it is globally important.

## De-Duplication

Cluster coverage by underlying event. Pick one headline per event. Prefer the earliest primary source and one reputable independent context source. Do not count analysis posts, syndicated copies, and PR rewrites as separate events.

## Red Flags

- A story has no date or the date is older than the reporting window.
- The only source is a promotional post or anonymous social account.
- The article repeats a prior announcement with no new fact.
- The number in the headline does not match the body or filing.
- The event is mostly market-price movement without an operational reason.
- The item is globally interesting but has weak Silicon Valley relevance.
- The company is outside Silicon Valley/Bay Area and the only local connection is a minor investor, customer, or commentator.
