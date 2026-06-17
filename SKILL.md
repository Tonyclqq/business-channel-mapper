---
name: business-channel-mapper
description: Analyze any industry, product, service, or target customer to map relationship, referral, content/self-media, community, platform, and strategic acquisition channels; customer sources; demand signals; decision chains; trust chains; channel strengths and weaknesses; private-domain handoff; weighted channel scoring; cooperation models; and 30-day/90-day action plans. Use when a user asks to find sales channels, resource/referral channels, online lead sources, Xiaohongshu/Douyin/WeChat/Bilibili/official-account content channels, community acquisition, platform/SEO channels, go-to-market paths, decision influence, channel scoring, or customer acquisition plans.
---

# Business Channel Mapper

## Purpose

Use this Skill to produce a practical business channel map: where demand appears, who controls trust, which channels deserve priority, and how the business should validate and activate those channels.

The Skill optimizes for:

- Revenue potential.
- Customer quality.
- Trust transfer.
- Scalability.
- Acquisition cost.
- Competitive advantage.

Do not optimize for vanity metrics such as followers, likes, views, or traffic unless they create qualified conversations or measurable pipeline.

## Applicable Scenarios

Use this Skill when the user provides an industry, product, service, offer, city, target customer, price band, current resources, or business goal and wants to understand:

- Where customers come from.
- Which people or organizations know demand earliest.
- Who affects purchase decisions.
- Which relationships can transfer trust.
- Which content or self-media channels can create demand, build authority, and move leads into private-domain follow-up.
- Which community and platform channels can produce qualified leads.
- Which acquisition channels deserve priority.
- How to contact, interview, cooperate with, activate, and measure channels.

Do not use this Skill for financial valuation, market-size forecasting, CRM database design, advertising copywriting, or Feishu/Lark workflows unless the user separately asks for those tasks.

## User Input Format

Accept free-form input. If key fields are missing, infer conservatively and state assumptions.

Recommended structured input:

```text
行业/产品/服务:
目标客户:
城市/区域:
客单价/项目金额:
当前资源:
业务目标:
约束条件:
```

Minimum viable input:

```text
帮我分析 [行业/产品/服务/目标客户] 的获客渠道地图。
```

Match the user's language. If the user writes in Chinese, produce the report in Chinese by default.

# Auto Run Mode

When the user provides business information containing any of the following fields:

- 行业/产品/服务
- 目标客户
- 城市/区域
- 客单价/项目金额
- 当前资源
- 业务目标
- 约束条件

The Skill MUST automatically:

1. Read the business information.
2. Apply the full Business Channel Mapper framework.
3. Generate the complete commercial channel map analysis report.
4. Save the final Markdown report to `outputs/channel_map_report.md` unless the user specifies another path.

The user should not need to repeatedly write:

- 请加载并遵循 SKILL.md
- 基于以下业务信息生成完整商业渠道地图分析报告
- 保存至 outputs/channel_map_report.md

Default output path:

```text
outputs/channel_map_report.md
```

If the business type is clear, create a readable filename, for example:

```text
outputs/high_end_residential_design_channel_map.md
```

## Cloud Document Title Rule

When the user explicitly asks to save, import, upload, or share the generated Markdown report as a Feishu/Lark cloud document, set the cloud document title from the Markdown report's first-level heading, not from the local filename.

Title extraction rule:

1. Read the first Markdown H1 line.
2. If it matches `# 商业渠道地图分析报告：<business_title>`, use only `<business_title>` as the Feishu/Lark cloud document title.
3. Trim surrounding whitespace.
4. If the H1 does not match this pattern, fall back to the readable local filename without the `.md` extension.

Example:

```markdown
# 商业渠道地图分析报告：企业管理咨询与培训服务
```

The Feishu/Lark cloud document title MUST be:

```text
企业管理咨询与培训服务
```

Do not use the full H1 or the local filename as the cloud document title when the business title can be extracted.

## Core Questions

Every analysis must answer four questions:

1. Where does demand come from?
2. Who controls trust?
3. Which channels generate the highest ROI?
4. How can growth become repeatable?

## Mandatory Auto Analysis

The Skill must automatically analyze the following items for every business case, even when the user does not explicitly ask for each one:

- Who pays.
- Who uses.
- Who makes the decision.
- Who recommends.
- Who controls demand.
- Who controls trust.
- Where customers come from.
- Why customers convert.
- How content generates qualified leads.
- How private-domain follow-up converts leads.
- How relationship channels amplify acquisition.
- How to form a repeatable growth flywheel.

These items are not optional. If user input is incomplete, infer conservatively, state assumptions, and still complete the analysis.

## Analysis Framework

### 1. Customer Mapping

Clarify roles separately:

- Final customer: the economic buyer or main beneficiary.
- User: the person or team experiencing the product/service.
- Payer: the budget owner or contracting party.
- Decision maker: the person with final approval, veto power, or decisive influence.
- Recommender: the trusted person or channel that puts the supplier on the shortlist.
- Influencer: the person shaping criteria, timing, perception, or preference.
- Gatekeeper: the person who can block purchase because of budget, risk, operations, compliance, family opinion, or professional judgment.

When these roles differ, explain the gap. For B2B purchases, distinguish owner, operator, procurement, technical evaluator, finance/legal, and external consultant. For consumer or household decisions, distinguish payer, daily user, aesthetic lead, budget controller, and family veto-holder.

### 2. Demand Mapping

Identify where demand appears before a supplier is selected:

- Where customers first express need.
- Who discovers demand first.
- What triggers purchasing behavior.
- What events accelerate demand.
- What events delay demand.
- Which offline scenes create discovery.
- Which online scenes reveal demand: search keywords, comments, saves, DMs, form submissions, group questions, map searches, platform inquiries, review pages, live/event registration, repeat visits, or quote requests.
- Which adjacent suppliers already serve the same customer before, during, or after the purchase.

Output demand sources, demand triggers, demand timing, and early demand signals.

### 3. Decision Chain Analysis

Map decision participants:

- Who raises the need.
- Who influences criteria.
- Who recommends suppliers.
- Who controls budget.
- Who has veto power.
- Who signs the contract.
- Who will be blamed if the supplier fails.

Use this chain to distinguish lead source from decision influence. A channel with few leads may still be valuable if it shapes trust, criteria, timing, or the shortlist.

### 4. Trust Chain Analysis

Map how trust transfers:

- Whom the customer already trusts.
- Whose recommendation is accepted without heavy comparison.
- Which relationships can credibly introduce the supplier.
- Which proof assets reduce perceived risk.
- Which community or platform proof increases credibility.
- Which cooperation models align incentives without damaging credibility.

Prefer channels that combine access, trust, timing, and decision influence.

### 5. Growth Channel Discovery

Every analysis must classify channels into six types:

1. Relationship channels: designers, architects, material suppliers, consultants, construction teams, real-estate sales, private bankers, brand partners, brokers, existing customers.
2. Referral channels: customer referrals, industry referrals, supplier referrals, partner referrals, expert referrals, alumni referrals.
3. Content channels: Xiaohongshu, Douyin, WeChat Channels, WeChat official accounts, Bilibili, Zhihu, newsletters, blogs, case libraries, design/media columns.
4. Community channels: WeChat groups, industry communities, owner groups, designer groups, chambers of commerce, alumni groups, local high-net-worth communities.
5. Platform channels: Dianping, Meituan, Taobao, Xiaohongshu shop, official website, SEO pages, map/local listings, vertical directories, procurement/service platforms.
6. Strategic channels: developers, property management companies, private banks, industry associations, commercial real estate operators, enterprise ecosystem partners, large account alliances.

Do not output a generic "internet channel." Break it into content, community, and platform channels when relevant.

The final report structure has four named channel-analysis sections: relationship, content, community, and platform. Referral channels and strategic channels must still be analyzed and surfaced in the customer source analysis, channel scoring table, S/A/B priority sections, key resource person analysis, channel cooperation strategy, and core growth path. Do not omit them simply because they do not have separate report section titles.

### 6. Content and Private-Domain Analysis

When content/self-media is relevant, include:

- Suitable platforms.
- Platform user profile.
- Content topic directions.
- Content conversion path.
- Private-domain handoff method.
- Content channel scoring.
- 30-day content publishing plan.

For each content platform, specify:

- Target user: payer, user, recommender, evaluator, influencer, or gatekeeper.
- Intent stage: problem-aware, solution-aware, supplier-comparing, ready-to-consult, or referral amplification.
- Demand signal: keyword, comment, save, DM, form, group question, repeat visit, quote request, live/event registration.
- Proof asset: case, before/after, expert explanation, process, pricing logic, checklist, demo, audit, consultation, testimonial.
- Conversion path: content -> profile/landing page -> DM/form/private WeChat -> qualification -> consultation -> proposal -> deal.
- Private-domain owner and follow-up timing.

### 7. Growth Flywheel Analysis

Identify:

- Acquisition path.
- Conversion path.
- Referral path.
- Retention path.
- Expansion path.

Output a concise growth flywheel, for example:

```text
Customer insight -> Trust asset -> Qualified conversation -> Conversion -> Delivery proof -> Referral -> New demand
```

## Channel Scoring

Use weighted scoring tables. Scores range from 1 to 5. Explain the reason for each high or low score.

### Non-Content Channel Score

Use this for relationship, referral, community, platform, and strategic channels:

- Demand quantity: 25%
- Customer quality: 20%
- Decision influence: 20%
- Trust transfer ability: 20%
- Activation difficulty: 15%

Activation difficulty uses an inverted score:

- 5 = easy to reach, activate, or validate.
- 1 = very hard to reach, activate, or validate.

Formula:

```text
score = demand_quantity*0.25 + customer_quality*0.20 + decision_influence*0.20 + trust_transfer*0.20 + activation_difficulty*0.15
```

### Content Channel Score

Use this for content and self-media platforms:

- Traffic potential: 25%
- User precision: 20%
- Trust-building ability: 20%
- Conversion efficiency: 20%
- Execution cost: 15%

Execution cost uses an inverted score:

- 5 = low cost, easy to sustain, easy to validate.
- 1 = high cost, hard to sustain, slow to validate.

Formula:

```text
content_score = traffic_potential*0.25 + user_precision*0.20 + trust_building*0.20 + conversion_efficiency*0.20 + execution_cost*0.15
```

### Priority Levels

Classify channels into:

- S-Level: high ROI, strong trust transfer, realistic activation, and strategic importance.
- A-Level: useful and worth testing, but with one clear limitation.
- B-Level: possible but lower priority, slow to activate, or weakly connected to demand/trust.

Always identify:

- Top 3 growth channels.
- Top 3 quick wins.
- Top 3 long-term assets.

For each priority channel, explain:

- Why it matters.
- Why now.
- Expected ROI logic.
- Validation method.
- First action.

## Dynamic Focus Engine

Automatically identify the most important growth drivers based on the business model and allocate more analysis depth to high-leverage channels.

Examples:

- Interior design: designer referrals, high-net-worth acquisition, Xiaohongshu, WeChat Channels, referral systems.
- Commercial lighting: design firms, brand owners, retail expansion projects, industry relationships.
- High-end dining: repeat customers, membership systems, business banquet channels, high-net-worth communities.
- AI consulting: founder communities, industry associations, thought leadership content, referral networks.
- Luxury car sales: old-customer referrals, private circles, finance/insurance partners, short-video trust content, local platform presence.
- Insurance sales: professional referrals, old-customer referrals, family lifecycle triggers, community education, private-domain follow-up.

## Mandatory Report Structure

Every report must use the following 20 sections in this exact order and with these section meanings:

```markdown
# 商业渠道地图分析报告：[对象]

## 01. 行业概览
## 02. 最终客户分析
## 03. 客户来源分析
## 04. 决策链分析
## 05. 信任链分析
## 06. 关系渠道分析
## 07. 内容渠道分析
## 08. 社群渠道分析
## 09. 平台渠道分析
## 10. 渠道评分表
## 11. S级渠道
## 12. A级渠道
## 13. B级渠道
## 14. 关键资源人分析
## 15. 渠道合作策略
## 16. 内容策略
## 17. 私域策略
## 18. 30天行动计划
## 19. 90天行动计划
## 20. 核心增长路径
```

Section requirements:

- `01. 行业概览`: define the business model, target market, price band, demand context, and key assumptions.
- `02. 最终客户分析`: include who pays, who uses, who decides, who recommends, who influences, and who can veto.
- `03. 客户来源分析`: include where customers come from, who controls demand, early demand signals, and referral/strategic demand sources.
- `04. 决策链分析`: map the full purchase decision chain.
- `05. 信任链分析`: identify who controls trust, how trust transfers, and which proof assets reduce risk.
- `06. 关系渠道分析`: analyze direct relationship channels and relationship-based amplification paths.
- `07. 内容渠道分析`: analyze content/self-media lead generation, platform fit, topics, conversion paths, and proof assets.
- `08. 社群渠道分析`: analyze communities, groups, associations, circles, and community-based demand discovery.
- `09. 平台渠道分析`: analyze search, local listings, review platforms, vertical directories, marketplaces, and service/procurement platforms.
- `10. 渠道评分表`: score all relevant channels, including relationship, referral, content, community, platform, and strategic channels.
- `11. S级渠道`: list the highest-priority channels and why they matter now.
- `12. A级渠道`: list useful channels worth testing and their limitations.
- `13. B级渠道`: list lower-priority or longer-cycle channels and why they are not immediate priorities.
- `14. 关键资源人分析`: identify who to meet, why they matter, what they control, and what to ask them.
- `15. 渠道合作策略`: recommend cooperation models, activation methods, incentives, and risk boundaries.
- `16. 内容策略`: provide platform selection, content pillars, topic ideas, proof assets, publishing rhythm, and validation metrics.
- `17. 私域策略`: define lead capture, qualification, follow-up, conversion, ownership, and timing.
- `18. 30天行动计划`: provide concrete weekly actions for fast validation.
- `19. 90天行动计划`: provide a staged roadmap for compounding assets and channel expansion.
- `20. 核心增长路径`: summarize the acquisition path, conversion path, referral path, retention path, and growth flywheel.

Every report must also include:

- Top 3 growth channels.
- Top 3 quick wins.
- Top 3 long-term assets.
- One-sentence growth strategy.
- Six-channel analysis covering relationship, referral, content, community, platform, and strategic channels.
- Comprehensive channel scoring table.
- Content channel scoring table when content is relevant.
- Whom to find in each channel.
- Why they matter.
- What they control.
- How to approach them.
- What questions to ask.
- How to cooperate.
- Private-domain handoff path.
- Risks and red flags.
- Validation metrics.
- 30-day action plan.
- 90-day roadmap.

## Local Resources

For detailed templates, read:

- `templates/channel_map_report_template.md`
- `templates/channel_comparison_table.md`
- `templates/resource_interview_questions.md`
- `templates/30_day_action_plan.md`

For task-specific prompting, read:

- `prompts/channel_mapper_prompt.md` for full channel mapping.
- `prompts/decision_chain_prompt.md` for decision-chain analysis.
- `prompts/trust_chain_prompt.md` for trust transfer.
- `prompts/scoring_prompt.md` for scoring.

For internet/content channel mapping, read:

- `references/internet_channels.md` when the user asks about online channels, content channels, self-media, SEO, ads, private domain, platform leads, or when a report would otherwise over-focus on relationship channels.

For examples, read only the relevant file:

- `examples/high_end_residential_design_with_media.md` for high-end residential design with relationship + self-media acquisition.
- `examples/luxury_retail_lighting.md` for luxury retail lighting consultants.
- `examples/interior_design.md` for interior design services.
- `examples/luxury_car_sales.md` for luxury car sales.
- `examples/insurance_sales.md` for insurance sales.
- `examples/ai_consulting.md` for AI consulting.

## Local Script

Use `scripts/generate_channel_report.py` only when the user wants a local Markdown report generated from command-line inputs. The script reads local templates only and must not call external services.

## Quality Standards

- Separate final customer, user, payer, decision maker, recommender, influencer, and gatekeeper.
- Prioritize channels by access to demand and trust, not generic popularity.
- Explain why each channel matters in the customer's decision process.
- Include all six channel types unless the business model clearly excludes one.
- Include practical contact paths, interview questions, cooperation models, and first actions.
- For content channels, include platform fit, user profile, topics, conversion path, private-domain handoff, scoring, and a 30-day publishing plan.
- State assumptions when information is missing.
- Use weighted scoring tables.
- Identify risks, false channels, validation metrics, success signals, and failure signals.
- Make action plans concrete enough to execute.

## Prohibited Actions

- Do not connect to Feishu/Lark unless the user explicitly asks to save, import, upload, or share the report through Feishu/Lark.
- Do not call external APIs.
- Do not create a database or CRM system.
- Do not invent fake market statistics, named partners, or unverifiable case data.
- Do not treat traffic, likes, views, or followers as business results unless they lead to qualified conversations.
- Do not recommend illegal rebates, undisclosed kickbacks, deceptive cooperation, fake reviews, fake comments, fake case studies, or undisclosed paid endorsements.
- Do not output vague advice such as "do content marketing", "run ads", "build private domain", or "post on Xiaohongshu" without specifying target user, topic, trust path, conversion path, private-domain handoff, validation metric, and action.
