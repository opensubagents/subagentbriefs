---
description: Learn to decompose your North Star Metric into actionable input metrics your data analytics product teams can directly influence.
title: Identifying Input Metrics for Your Data Analytics Product
image: https://tryhamster.com/skills/identifying-input-metrics/opengraph-image-1tdarl?74b99121c50772fb
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

# Identifying and Mapping Input Metrics to Your Data Analytics Product's North Star

This skill teaches you how to break down your North Star Metric into a set of actionable, team-level input metrics that collectively drive your core product outcome — turning a single guiding number into a practical system of levers your organization can pull every day.

To identify input metrics, decompose your North Star Metric into the 3-6 leading indicators that directly drive it. For each candidate metric, verify that teams can influence it through daily work, it moves predictably before the North Star changes, and it's measurable at a weekly or daily cadence. Map each input metric to a specific team or squad to create clear ownership and accountability.

Outcome: You'll have a clear, validated map of 3-6 input metrics tied to your North Star, each owned by a specific team, enabling every squad to see exactly how their work moves the company's most important number.

[Add to Hamster](https://tryhamster.com/auth/sign-up?utm%5Fsource=website&utm%5Fmedium=pseo&utm%5Fcampaign=skill-identifying-input-metrics&utm%5Fcontent=hero)[or download skill pack](https://tryhamster.com/%5Fsite/api/download/skill/north-star-metric/identifying-input-metrics)

Apr 19, 2026

Synthesized from public framework references and reviewed for accuracy.

ProductIntermediate2-4 hours

## Prerequisites

* A defined North Star Metric (see Selecting the Right North Star Metric for Your Product)
* Basic understanding of product analytics and funnel thinking
* Familiarity with your product's user journey and key touchpoints
* Access to your product's data or analytics platform

## Overview

Your North Star Metric captures the core value your product delivers, but it's typically a lagging indicator — it tells you where you've been, not what to do next. Input metrics are the leading indicators that decompose your North Star into components teams can actually move through their daily work. For any data analytics product, this decomposition is the bridge between high-level strategy and ground-level execution.

Without well-defined input metrics, teams default to vanity metrics or siloed KPIs that don't connect back to product-wide outcomes. The result is misalignment: the growth team optimizes signups while the engagement team optimizes session length, and nobody knows whether either effort actually drives the metric that matters. Input metric mapping solves this by creating a shared, mathematically grounded model of how your North Star Metric is produced.

This skill is central to the [North Star Metric](https://tryhamster.com/methods/north-star-metric) framework. Once you've selected your North Star, identifying input metrics is the essential next step before you can align cross-functional teams, build meaningful dashboards, or connect the metric to roadmap decisions.

## How It Works

Input metrics work because your North Star Metric is never truly atomic — it's always a composite of upstream behaviors, actions, and conditions. A data analytics product whose North Star is "Weekly Active Analysts" can decompose that into new analyst activation rate, returning analyst retention rate, and the number of analyses completed per session. Each of these is a lever that a specific team can own and improve.

The conceptual model is a tree: your North Star sits at the top, and input metrics branch below it. Some inputs are additive (new users + retained users = total active users), some are multiplicative (users × frequency × depth = engagement score), and some are sequential (activation feeds into retention which feeds into expansion). The shape of your tree depends on your product's value creation model.

The key insight is that good input metrics are **leading** indicators — they change before your North Star does, giving teams a fast feedback loop. If your North Star moves on a monthly cadence, your input metrics should move weekly or even daily. This speed difference is what makes input metrics actionable: teams can run experiments, see results in days, and course-correct without waiting for the lagging North Star to budge.

Finally, the mapping must be exhaustive but not excessive. You want 3-6 input metrics that collectively explain the majority of variance in your North Star. Too few and you're missing critical levers; too many and you've recreated the dashboard sprawl you were trying to escape.

## Step-by-Step

1. ### Step 1: Write Out the Mathematical Relationship Behind Your North Star  
Start by expressing your North Star Metric as a formula or equation. This forces you to think structurally about what produces it rather than treating it as an abstract goal.  
For example, if your North Star for a data analytics product is "Weekly Reports Consumed," you might write: `Weekly Reports Consumed = Active Users × Reports per User per Week`. You can further decompose Active Users into `New Activated Users + Returning Users`. Reports per User can decompose into `Sessions per User × Reports per Session`.  
Write multiple candidate formulations. There's rarely one "correct" decomposition — the right one depends on where your product's biggest growth levers are and how your teams are organized. Test each formulation by asking: does this equation actually hold when I plug in real numbers from last quarter?  
Tip: Use a whiteboard or diagramming tool (Miro, FigJam) for this step. Invite your data analyst to validate the math against actual product data before moving forward.
2. ### Step 2: Generate Candidate Input Metrics from Each Branch  
For every term in your formula, generate 2-3 possible metrics that could represent it. Don't filter yet — this is a divergent step.  
For the "New Activated Users" branch, candidates might include: signups that complete onboarding, users who create their first dashboard, or users who invite a teammate within 48 hours. Each captures a slightly different definition of "activated." List them all.  
Pull in perspectives from different teams. Engineering might suggest infrastructure-related metrics (query response time affecting activation). Marketing might propose channel-specific acquisition metrics. Product might focus on feature adoption rates. The goal is a comprehensive long list before you narrow down.  
Tip: A common trap is only generating metrics your current analytics stack already tracks. Think about what \*should\* be measured, not just what's easy to measure.
3. ### Step 3: Apply the Input Metric Quality Filter  
Now filter your candidates through four criteria. A strong input metric must pass all four:  
   1. **Influenceable**: Can a team directly move this metric through their work within a sprint cycle? If nobody can design an experiment to improve it, it's not actionable.  
   2. **Predictive**: Does this metric change _before_ the North Star changes? Check historical data — when this metric moved last quarter, did the North Star follow?  
   3. **Measurable**: Can you track this metric at a weekly (ideally daily) cadence with your current or near-term data infrastructure?  
   4. **Non-redundant**: Does this metric capture something the other input metrics don't? If two candidates are highly correlated (r > 0.85), pick the one that's more actionable and drop the other.  
Score each candidate metric against these four criteria. Be honest — a metric that scores 4/4 is rare and valuable. Most of your final input metrics will score 3/4 with a plan to close the gap on the fourth.  
Tip: Run a quick correlation analysis between candidate metrics and your North Star using the last 6-12 months of data. If the correlation is weak or absent, the candidate isn't truly an input metric — it's a distraction.
4. ### Step 4: Select 3-6 Final Input Metrics and Assign Ownership  
From your filtered list, select the 3-6 metrics that collectively cover the most important levers for your North Star. Aim for a mix: at least one acquisition-oriented metric, one engagement or activation metric, and one retention or depth metric.  
For each selected input metric, assign a clear owner — typically a squad, pod, or cross-functional team. Ownership means that team is responsible for monitoring the metric, diagnosing changes, and running experiments to improve it. Without ownership, input metrics become spectator metrics that everyone watches but nobody moves.  
Document the ownership map explicitly. A simple table works: Input Metric | Definition | Owner | Target | Cadence. Share this as a living document, not a slide that gets filed away.  
Tip: If a single input metric requires two teams to collaborate to move it, that's a sign it needs to be decomposed further or that your team structure needs a closer look.
5. ### Step 5: Validate the Map with Historical Data  
Before committing to your input metric map, backtest it. Pull 6-12 months of historical data and check whether your input metrics, in combination, actually explain movements in your North Star.  
Run a simple regression or even a visual analysis: during weeks when Input Metric A improved and B held steady, did the North Star move as your model predicts? Look for periods where the North Star moved but none of your input metrics changed — these gaps reveal missing inputs you haven't captured.  
This step is especially critical for a data analytics product where teams have access to rich behavioral data. Use your own product's analytics capabilities to validate the model. If you can't explain at least 70-80% of historical North Star variance through your input metrics, your map is incomplete.  
Tip: Don't expect perfection. External factors (seasonality, market shifts) will always introduce noise. The goal is a model that's directionally right and practically useful, not statistically perfect.
6. ### Step 6: Define Targets and Review Cadence  
For each input metric, set a specific, time-bound target. These targets should be ambitious enough to move the North Star but realistic enough that teams don't burn out or game the metric.  
Derive targets by working backward from your North Star goal. If your North Star target is "10,000 Weekly Active Analysts by Q3" and your decomposition shows that requires a 15% improvement in activation rate and a 10% improvement in retention, set those as your input metric targets.  
Establish a regular review cadence — typically weekly for input metrics, monthly for the North Star. In each review, teams present their input metric trajectory, diagnose any unexpected movements, and share learnings from experiments. This cadence is what transforms a static metric map into a living operational system.  
Tip: Build automated alerts for when input metrics deviate significantly from their expected trajectory. Early detection of a dropping activation rate is far more valuable than discovering it in a monthly review.

## Examples

### Example: Input Metric Map for a B2B Data Analytics Product

A B2B data analytics product has selected 'Weekly Active Analysts' as its North Star Metric. The company has teams responsible for growth, activation, core product experience, and enterprise expansion. They need to decompose the North Star into input metrics that align with their team structure.

The product team starts by writing the formula: `Weekly Active Analysts = New Activated Analysts (this week) + Returning Analysts (from previous weeks)`. They further decompose:

* **New Activated Analysts** \= Signups × Onboarding Completion Rate × First-Value-Moment Rate (defined as creating their first saved query within 48 hours)
* **Returning Analysts** \= Previous Active Analysts × Week-over-Week Retention Rate
* **Engagement Depth** \= Queries Run per Analyst per Week (a quality signal — more queries means more value extracted)

After filtering for influenceability, predictiveness, and measurability, they select four input metrics:

1. **Onboarding Completion Rate** (Growth team owns) — % of signups who connect a data source and run their first query
2. **First-Value-Moment Rate** (Activation team owns) — % of onboarded users who save their first query or dashboard within 48 hours
3. **Week-1 Retention Rate** (Core Product team owns) — % of activated users who return in the second week
4. **Queries per Analyst per Week** (Core Product team co-owns with Enterprise team) — average depth of engagement

They validate with 9 months of data and find these four metrics explain \~78% of weekly variance in the North Star. The missing \~22% is attributed to seasonality and enterprise contract cycles. They set quarterly targets: improve onboarding completion from 45% to 55%, first-value-moment from 30% to 40%, week-1 retention from 60% to 65%, and maintain queries per analyst above 12.

### Example: Discovering a Missing Input Metric Through Backtesting

A self-service analytics platform initially identified three input metrics for its North Star ('Monthly Insights Shared'): new user activation, dashboard creation rate, and sharing feature adoption. During quarterly review, they noticed a 3-week period where all three input metrics were stable but the North Star dropped 18%.

The team investigated the anomaly and discovered that a cohort of power users — the top 10% who generated 40% of shared insights — had churned simultaneously. Their three input metrics didn't capture power-user health because they averaged across all users equally.

They added a fourth input metric: **Power User Retention Rate** (% of users sharing 5+ insights/month who remain active). This metric was assigned to a newly formed 'customer success' squad focused on high-value accounts. Backtesting with this fourth metric included, the model's explanatory power jumped from 65% to 82%. The lesson: input metric maps need to account for user segments, not just aggregate behaviors. For any data analytics product with a heavy-user concentration, segment-specific retention metrics are often the most predictive input.

## Best Practices

* Always derive input metrics from a mathematical or logical decomposition of your North Star — never brainstorm metrics in isolation and retroactively try to connect them upward.
* Limit yourself to 3-6 input metrics. Research on organizational focus consistently shows that teams perform better with fewer, clearer priorities. If you have more than 6, you're probably tracking sub-inputs that should roll up.
* Ensure every input metric has exactly one owning team. Shared ownership is no ownership. If two teams must collaborate on an outcome, give one team the metric and the other a supporting SLA.
* Review and recalibrate your input metric map quarterly. As your data analytics product matures, the bottleneck shifts — what was once an activation problem may become a retention problem, and your input metrics should evolve accordingly. See also: [Evolving Your North Star Metric Across Product Growth Stages](https://tryhamster.com/skills/evolving-north-star-across-growth-stages).
* Use your input metrics as the primary language in sprint planning and roadmap discussions. If a proposed feature doesn't connect to an input metric, it needs a stronger justification for inclusion.
* Document the causal hypothesis behind each input metric explicitly (e.g., 'We believe improving onboarding completion rate will increase weekly active analysts because users who complete onboarding are 3x more likely to return in week 2'). This makes the assumption testable.

## Common Mistakes

Choosing output metrics disguised as input metrics — for example, selecting 'revenue' as an input to 'monthly active users.'

Correction

Input metrics must be upstream of and causally prior to your North Star. Test directionality: does changing the candidate metric _cause_ the North Star to move, or is it the other way around? If you can't articulate the causal mechanism, it's likely a correlated output, not a true input.

Selecting metrics that no team can actually influence — like 'market size' or 'competitor pricing.'

Correction

Apply the influenceability test rigorously. For every candidate, ask: 'What specific experiment could a team run this month to move this number by 5%?' If nobody can answer, discard it and look for a more proximate lever within your product experience.

Creating too many input metrics (8+) because every team wants 'their' metric represented.

Correction

More metrics doesn't mean more alignment — it means more noise. Use a tiered system: 3-6 company-level input metrics that map to the North Star, and allow teams to define sub-metrics beneath their owned input metric. This preserves focus at the top while giving teams room to operate.

Mapping input metrics once and never revisiting the model as the product evolves.

Correction

Your input metric map is a hypothesis about how value is created in your product. Like any hypothesis, it should be tested and updated. Schedule quarterly reviews where you re-validate the statistical relationship between input metrics and your North Star, and retire or replace metrics that no longer predict movement.

Ignoring metric interactions and trade-offs — optimizing one input metric at the expense of another.

Correction

Monitor input metrics as a system, not in isolation. If improving activation rate is degrading retention (e.g., by lowering the onboarding quality bar), you've created a local optimization that hurts the North Star. Flag these trade-offs in weekly reviews and adjust experiment designs to account for cross-metric effects.

## Other Skills in This Method

[Connecting Your North Star Metric to Product Roadmap DecisionsHow to use your North Star Metric and its input metrics to prioritize roadmap initiatives and justify strategic trade-offs.](https://tryhamster.com/skills/connecting-north-star-to-product-roadmap)[Building Dashboards to Track Your North Star and Input MetricsHow to set up real-time dashboards and reporting cadences that make your North Star Metric and its supporting inputs visible and actionable across the organization.](https://tryhamster.com/skills/building-north-star-dashboards)[Validating Your North Star Metric with User ResearchHow to use qualitative user research and customer insights to confirm that your chosen North Star Metric truly reflects the value customers experience.](https://tryhamster.com/skills/validating-north-star-with-user-research)[Selecting the Right North Star Metric for Your ProductHow to evaluate candidate metrics and choose the single metric that best captures the core value customers get from your product.](https://tryhamster.com/skills/selecting-your-north-star-metric)[Evolving Your North Star Metric Across Product Growth StagesWhen and how to revisit, refine, or replace your North Star Metric as your product matures from MVP through scaling and beyond.](https://tryhamster.com/skills/evolving-north-star-across-growth-stages)[Aligning Cross-Functional Teams Around a Shared North StarTechniques for communicating, cascading, and embedding the North Star Metric across engineering, design, marketing, and other cross-functional teams to drive shared accountability.](https://tryhamster.com/skills/aligning-cross-functional-teams-around-north-star)

## Frequently Asked Questions

How many input metrics should I have for my North Star Metric?+

Aim for 3-6 input metrics. Fewer than 3 usually means your decomposition is too shallow and you're missing critical levers. More than 6 typically introduces noise and dilutes team focus. If you have more candidates, organize them into a hierarchy where 3-6 top-level inputs map to the North Star and sub-metrics roll up beneath each one.

What's the difference between an input metric and a KPI?+

A KPI is any metric a team tracks to measure performance. An input metric is specifically a leading indicator that causally drives your North Star Metric. All input metrics are KPIs, but not all KPIs are input metrics. The distinction matters because input metrics have a validated, directional relationship to your company's most important outcome.

How do I know if my input metrics are actually driving the North Star?+

Validate with historical data. Check whether past improvements in your input metrics preceded improvements in your North Star. Run correlation and basic regression analyses over 6-12 months of data. If an input metric frequently moves without any corresponding North Star movement, it may not be a true driver. See our guide on \[building dashboards\](/skills/building-north-star-dashboards) for tracking these relationships.

Can input metrics change over time as my data analytics product matures?+

Absolutely — and they should. Early-stage products often focus on acquisition and activation inputs, while mature products shift toward retention and expansion inputs. Review your input metric map quarterly and update it as your product's growth bottleneck evolves. The sibling skill on \[evolving your North Star across growth stages\](/skills/evolving-north-star-across-growth-stages) covers this in depth.

What if two teams need to collaborate to move a single input metric?+

Assign primary ownership to one team and create an explicit SLA or collaboration agreement with the supporting team. If the metric genuinely requires equal contribution from both teams, that's often a sign it should be decomposed into two more specific metrics — one per team — that roll up into the shared outcome.

Should input metrics for a data analytics product focus on usage or business outcomes?+

Input metrics should focus on user behaviors and product interactions — the actions that lead to business outcomes, not the outcomes themselves. For a data analytics product, metrics like 'queries run per user' or 'dashboards shared per week' are better inputs than 'revenue per account' because teams can directly influence product usage through design and feature work.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Skills","item":"https://tryhamster.com/skills"},{"@type":"ListItem","position":3,"name":"Identifying Input Metrics","item":"https://tryhamster.com/skills/identifying-input-metrics"}]}
[{"@context":"https://schema.org","@type":"TechArticle","headline":"Identifying Input Metrics for Your Data Analytics Product","name":"Identifying Input Metrics for Your Data Analytics Product","description":"Learn to decompose your North Star Metric into actionable input metrics your data analytics product teams can directly influence.","image":"https://tryhamster.com/opengraph-image","url":"https://tryhamster.com/skills/identifying-input-metrics","author":{"@type":"Organization","name":"Hamster","url":"https://tryhamster.com"},"publisher":{"@type":"Organization","name":"Hamster","url":"https://tryhamster.com"},"reviewedBy":{"@type":"Organization","name":"Hamster editorial team"},"datePublished":"2026-04-19","dateModified":"2026-04-19","isPartOf":{"@type":"Article","headline":"North Star Metric","url":"https://tryhamster.com/methods/north-star-metric"},"about":"data analytics product, input metrics, north star metric decomposition, product input metrics, north star input metrics mapping","proficiencyLevel":"Intermediate"},{"@context":"https://schema.org","@type":"FAQPage","mainEntity":[{"@type":"Question","name":"How many input metrics should I have for my North Star Metric?","acceptedAnswer":{"@type":"Answer","text":"Aim for 3-6 input metrics. Fewer than 3 usually means your decomposition is too shallow and you're missing critical levers. More than 6 typically introduces noise and dilutes team focus. If you have more candidates, organize them into a hierarchy where 3-6 top-level inputs map to the North Star and sub-metrics roll up beneath each one."}},{"@type":"Question","name":"What's the difference between an input metric and a KPI?","acceptedAnswer":{"@type":"Answer","text":"A KPI is any metric a team tracks to measure performance. An input metric is specifically a leading indicator that causally drives your North Star Metric. All input metrics are KPIs, but not all KPIs are input metrics. The distinction matters because input metrics have a validated, directional relationship to your company's most important outcome."}},{"@type":"Question","name":"How do I know if my input metrics are actually driving the North Star?","acceptedAnswer":{"@type":"Answer","text":"Validate with historical data. Check whether past improvements in your input metrics preceded improvements in your North Star. Run correlation and basic regression analyses over 6-12 months of data. If an input metric frequently moves without any corresponding North Star movement, it may not be a true driver. See our guide on [building dashboards](/skills/building-north-star-dashboards) for tracking these relationships."}},{"@type":"Question","name":"Can input metrics change over time as my data analytics product matures?","acceptedAnswer":{"@type":"Answer","text":"Absolutely — and they should. Early-stage products often focus on acquisition and activation inputs, while mature products shift toward retention and expansion inputs. Review your input metric map quarterly and update it as your product's growth bottleneck evolves. The sibling skill on [evolving your North Star across growth stages](/skills/evolving-north-star-across-growth-stages) covers this in depth."}},{"@type":"Question","name":"What if two teams need to collaborate to move a single input metric?","acceptedAnswer":{"@type":"Answer","text":"Assign primary ownership to one team and create an explicit SLA or collaboration agreement with the supporting team. If the metric genuinely requires equal contribution from both teams, that's often a sign it should be decomposed into two more specific metrics — one per team — that roll up into the shared outcome."}},{"@type":"Question","name":"Should input metrics for a data analytics product focus on usage or business outcomes?","acceptedAnswer":{"@type":"Answer","text":"Input metrics should focus on user behaviors and product interactions — the actions that lead to business outcomes, not the outcomes themselves. For a data analytics product, metrics like 'queries run per user' or 'dashboards shared per week' are better inputs than 'revenue per account' because teams can directly influence product usage through design and feature work."}}]},{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Methods","item":"https://tryhamster.com/methods"},{"@type":"ListItem","position":2,"name":"North Star Metric","item":"https://tryhamster.com/methods/north-star-metric"},{"@type":"ListItem","position":3,"name":"Identifying Input Metrics for Your Data Analytics Product","item":"https://tryhamster.com/skills/identifying-input-metrics"}]}]
```
