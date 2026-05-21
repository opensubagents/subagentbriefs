---
description: Learn to build dashboards tracking your North Star and input metrics for a data analytics product strategy. Learn how Hamster helps teams plan, build,...
title: Building North Star Dashboards | Data Analytics Product
image: https://tryhamster.com/skills/building-north-star-dashboards/opengraph-image-1tdarl?74b99121c50772fb
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

# Building Dashboards to Track Your North Star: A Data Analytics Product Guide

This skill teaches you how to design and implement real-time dashboards and reporting rhythms that keep your North Star Metric and its supporting input metrics visible, contextualized, and actionable across every team in your organization.

Start by placing your North Star Metric prominently at the top of a single, centralized dashboard. Below it, display each input metric that drives the North Star, with trend lines showing at least 4–8 weeks of data. Connect live data sources, set meaningful thresholds for alerts, and establish a weekly reporting cadence so every team sees how their work connects to the metric that matters most.

Outcome: Your organization has a single source of truth dashboard where anyone can see the North Star Metric, understand the input metrics driving it, identify problems early, and connect daily work to strategic outcomes.

[Add to Hamster](https://tryhamster.com/auth/sign-up?utm%5Fsource=website&utm%5Fmedium=pseo&utm%5Fcampaign=skill-building-north-star-dashboards&utm%5Fcontent=hero)[or download skill pack](https://tryhamster.com/%5Fsite/api/download/skill/north-star-metric/building-north-star-dashboards)

Apr 19, 2026

Synthesized from public framework references and reviewed for accuracy.

ProductIntermediate2-4 hours for initial build, plus ongoing iteration

## Prerequisites

* A defined North Star Metric (see: Selecting the Right North Star Metric for Your Product)
* Mapped input metrics that drive your North Star (see: Identifying and Mapping Input Metrics to Your North Star)
* Access to a BI or dashboard tool (e.g., Looker, Tableau, Amplitude, Metabase, or even Google Sheets)
* Basic understanding of data pipelines and how your product events are tracked

## Overview

A North Star Metric is only as useful as its visibility. If the metric lives in a spreadsheet that one analyst updates monthly, it cannot serve as the organizational compass it's meant to be. Building a dedicated dashboard transforms your North Star from an abstract strategic concept into a living, breathing data analytics product artifact that teams reference daily.

The goal isn't just to display a number. It's to create a hierarchy of understanding: the North Star at the top, the input metrics that compose it in the middle, and segmented or team-specific views at the bottom. This structure lets executives check overall trajectory, product managers diagnose what's changing, and individual teams see how their specific lever is moving. When paired with a consistent reporting cadence—weekly reviews, monthly deep-dives—the dashboard becomes the heartbeat of your product organization.

Done well, this skill bridges the gap between the [North Star Metric](https://tryhamster.com/methods/north-star-metric) framework's strategic elegance and the messy reality of cross-functional execution. It's where data infrastructure meets product culture.

## How It Works

The concept behind a North Star dashboard is the **information hierarchy**. Your North Star Metric is a composite outcome—it moves because specific input metrics move. Those input metrics move because teams ship features, run experiments, and solve problems. The dashboard encodes this causal chain visually.

At the conceptual level, you're building three layers:

1. **The North Star layer** — a single, unmissable number with its trend over time. This answers: "Are we winning?"
2. **The input metrics layer** — 3–6 metrics that mathematically or logically compose the North Star. This answers: "What's driving the change?"
3. **The diagnostic layer** — segments, cohorts, and team-specific breakdowns. This answers: "Where exactly is the change happening, and who can act on it?"

The dashboard works because it makes the abstract concrete. When a product manager on the activation team sees that their input metric (new user activation rate) dropped 4% last week, they don't need someone to tell them to investigate. The data analytics product surfaces the signal automatically. When the VP of Product sees the North Star trending down, they can drill into the input layer to understand which lever broke—without scheduling a meeting.

Reporting cadences create the ritual around the dashboard. A weekly async check-in ensures nobody goes more than 5 business days without confronting reality. A monthly deep-dive creates space for causal analysis and strategy adjustment. The cadence prevents both the panic of watching numbers tick by tick and the negligence of quarterly-only reviews.

## Step-by-Step

1. ### Step 1: Audit Your Data Readiness  
Before touching any dashboard tool, verify that your North Star Metric and each input metric can actually be computed from your existing data infrastructure. For each metric, document:  
   * **The exact definition** (e.g., "Weekly Active Users who complete at least one core action")  
   * **The source table or event** (e.g., `events.core_action_completed`)  
   * **The calculation logic** (e.g., `COUNT(DISTINCT user_id) WHERE event = 'core_action_completed' AND timestamp >= NOW() - INTERVAL 7 DAYS`)  
   * **Data freshness** — how often does this data update? Real-time, hourly, daily?  
   * **Known gaps** — are there platforms, user segments, or events not yet tracked?  
This audit often reveals that one or two input metrics lack reliable data sources. It's far better to discover this now than after you've built a dashboard with blank panels.  
Tip: Create a simple data dictionary spreadsheet with columns for metric name, definition, SQL/query logic, data source, owner, and freshness. Share it with your data team for validation before proceeding.
2. ### Step 2: Design the Dashboard Layout on Paper First  
Sketch the dashboard layout before opening your BI tool. Use pen and paper, a whiteboard, or a simple design tool like Figma or even Google Slides.  
Place the North Star Metric at the top center—it should be the first thing anyone sees. Show it as a large number with a trend line spanning at least 8 weeks. Below it, arrange input metrics in a logical grouping. If your North Star decomposes into a formula (e.g., `NSM = New Users × Activation Rate × Engagement Frequency × Monetization per User`), lay them out left-to-right in that order so the composition is visually obvious.  
For each input metric, plan to show: the current value, the previous period value, percent change, and a trend line. Below the input layer, plan diagnostic panels—segment breakdowns, geographic splits, platform comparisons, or experiment results that help teams diagnose changes.  
Keep the dashboard to a single scrollable page. If you need more than one page, you're probably including vanity metrics or diagnostics that belong in team-specific sub-dashboards.  
Tip: Apply the 'five-second test': if someone glances at the dashboard for five seconds, they should be able to answer 'Is the North Star going up, down, or flat?' If they can't, simplify.
3. ### Step 3: Build the Dashboard in Your BI Tool  
Now implement the design in your chosen tool. Common choices include Looker, Tableau, Amplitude, Mixpanel, Metabase, or Mode Analytics. The specific tool matters less than consistency—pick the one your organization already uses and trusts.  
Start with the North Star panel. Use a combination visualization: a large KPI number (current value) next to a line chart showing the weekly or daily trend. Add a comparison annotation—whether that's week-over-week change, a target line, or a historical benchmark.  
Next, build each input metric panel using the same visual pattern for consistency. Uniform formatting reduces cognitive load—viewers should never have to figure out how to read a panel.  
Finally, add the diagnostic layer. This might include a breakdown by user segment, geography, platform (iOS vs. Android vs. Web), acquisition channel, or user cohort. Keep these as expandable or lower-priority sections so they don't distract from the primary story.  
Connect to live data sources rather than manual uploads wherever possible. A dashboard that requires someone to paste in a CSV every Monday morning is a dashboard that will be stale by Tuesday.  
Tip: Set all date ranges to use the same default (e.g., 'last 8 weeks, ending yesterday'). Mismatched date ranges across panels are a common source of confusion and incorrect conclusions.
4. ### Step 4: Add Contextual Annotations and Alerts  
Raw numbers without context are dangerous. A 10% drop in your North Star Metric could be a crisis or it could be a known seasonal pattern. Annotations transform a data display into a data analytics product that actually informs decisions.  
Add annotations for:  
   * **Feature launches** — mark the date a major feature shipped so you can visually correlate impact  
   * **Incidents** — note outages, data pipeline breaks, or bugs that affected metrics  
   * **Seasonal events** — holidays, back-to-school, end-of-quarter patterns  
   * **Experiment start/end dates** — so viewers don't confuse experiment-driven changes with organic shifts  
Also configure threshold-based alerts. Set up automated notifications (via Slack, email, or PagerDuty) when the North Star or a critical input metric moves beyond a defined range. For example: 'Alert the #product-metrics Slack channel if weekly active users drop more than 5% week-over-week.'  
Alerts should be rare enough to be taken seriously. If you send an alert every week, people will ignore them all.  
Tip: Maintain an 'annotation log'—a simple shared document where anyone can add context about things that happened on specific dates. This becomes invaluable during monthly deep-dives when you're trying to explain a trend.
5. ### Step 5: Set Permissions and Make It Universally Accessible  
A dashboard that only the data team can access defeats the purpose. The entire point of this exercise within the [North Star Metric](https://tryhamster.com/methods/north-star-metric) framework is organizational alignment—which requires organizational visibility.  
Grant view access to every employee by default. If there are sensitivity concerns (e.g., revenue figures before earnings), create a public version with the sensitive data removed and a restricted version for leadership.  
Pin the dashboard link in key Slack channels, bookmark it in your team wiki, and add it to your all-hands meeting template. Consider setting it as the default landing page in your BI tool so it's the first thing people see when they log in.  
Also define edit permissions carefully. Too many editors leads to accidental changes. Designate 1-2 dashboard maintainers who own the source of truth, and let others create their own copies for exploration.  
Tip: Put the dashboard URL in your company's onboarding checklist. New hires should see the North Star on their first day.
6. ### Step 6: Establish Reporting Cadences  
The dashboard is the artifact; the cadence is the ritual that makes it work. Establish three rhythms:  
**Daily (passive):** The dashboard is always available and always current. Teams that own specific input metrics check it as part of their daily workflow. No meeting required—this is ambient awareness.  
**Weekly (active, async or sync):** Every Monday (or your preferred day), distribute a brief summary—either auto-generated from the dashboard or written by a rotating team member. The summary should cover: North Star trend, input metric highlights, any anomalies, and one sentence on planned actions. Many teams do this as a Slack post with a screenshot of the dashboard and a few bullet points.  
**Monthly (deep-dive, sync):** A 30–60 minute meeting where product leadership reviews the North Star trend in depth. This is the time for causal analysis: why did this input metric move? What experiments contributed? What external factors were at play? Use this session to update targets, revise the input metric model, or flag concerns for the [product roadmap](https://tryhamster.com/skills/connecting-north-star-to-product-roadmap).  
The cadence ensures that the dashboard doesn't become digital wallpaper. Consistent review creates accountability without micromanagement.  
Tip: Automate the weekly summary wherever possible. Many BI tools support scheduled email snapshots. Pair that with a templated Slack message to reduce the burden on whoever's writing it.
7. ### Step 7: Iterate Based on Usage and Feedback  
Your first dashboard will not be perfect, and that's fine. After 2–4 weeks of use, actively solicit feedback:  
   * Are people actually looking at it? (Check view counts in your BI tool)  
   * Which panels do people click on most?  
   * What questions are people asking that the dashboard can't answer?  
   * Are the alerts too noisy, too quiet, or just right?  
   * Is any metric consistently confusing or misinterpreted?  
Common first-iteration improvements include: simplifying the layout, adding a comparison metric (e.g., showing the same period last year), adding a 'predicted' trend line based on current trajectory, or breaking out a diagnostic panel that teams kept asking for.  
Treat the dashboard like a data analytics product itself—it has users, and those users have needs. Iterate on it the way you'd iterate on any product feature.

## Examples

### Example: SaaS Collaboration Tool — Weekly Active Collaborators Dashboard

A B2B SaaS company building a collaborative document editor has chosen 'Weekly Active Collaborators' (users who edit or comment on a shared document at least once per week) as their North Star Metric. Their input metrics are: (1) New Team Signups, (2) Activation Rate (% of new teams creating their first shared doc within 7 days), (3) Collaboration Frequency (average shared doc interactions per active user per week), and (4) Team Retention (% of teams with ≥1 active collaborator month over month).

The team builds a Looker dashboard structured as follows:

**Top section:** A large KPI tile showing 'Weekly Active Collaborators: 42,300' with a green arrow indicating +3.2% WoW. Next to it, an 8-week trend line with a dotted target line at 50,000 (their quarterly goal).

**Middle section:** Four equal-width panels, one per input metric. Each shows current value, WoW change, and a sparkline trend. New Team Signups shows 1,840 (+5.1%), Activation Rate shows 38% (-2pp), Collaboration Frequency shows 4.2 interactions/week (+0.1), and Team Retention shows 82% (flat).

**Bottom section:** A breakdown of Weekly Active Collaborators by company size segment (SMB, Mid-Market, Enterprise) and by geographic region. An annotation marks the date they launched a new real-time commenting feature.

The dashboard reveals that despite growing signups, the dip in Activation Rate is partially offsetting the North Star growth. The product team investigates and finds that the new onboarding flow for teams with 10+ members is confusing. They flag this for the next sprint. The weekly Slack summary reads: 'WAC up 3.2% WoW to 42.3K. Signups strong but Activation Rate down 2pp—investigating onboarding for larger teams. Collaboration Frequency stable. On track for Q3 target if activation recovers.'

This is a data analytics product approach in action: the dashboard didn't just display data—it surfaced a specific, actionable insight that connected to the product roadmap.

### Example: Consumer Fitness App — Daily Active Exercisers Dashboard

A consumer fitness app has defined 'Daily Active Exercisers' (users who log at least one workout per day) as their North Star Metric. Input metrics include: (1) Daily New Downloads, (2) Day-1 Workout Completion Rate, (3) Weekly Workout Frequency among retained users, and (4) 30-Day Retention Rate.

The team uses Amplitude to build their dashboard. Since this is a consumer product with high daily variance, they display the North Star as a 7-day rolling average to smooth out weekend vs. weekday fluctuations. A secondary small chart shows raw daily values for pattern recognition.

The input metrics are arranged in funnel order (Downloads → Day-1 Completion → Frequency → Retention) to visually represent the user journey. Each panel uses a consistent color scheme: green if WoW trend is positive, yellow if flat, red if declining.

They set up two alerts: one if the 7-day rolling average of Daily Active Exercisers drops below 85% of the prior week's average, and one if Day-1 Workout Completion Rate drops below 25% (their critical activation threshold). They configure these to post to a #metrics-alerts Slack channel monitored by product and growth leads.

During the first month, the Day-1 alert fires after a new app update introduces a bug in the workout player on Android. The team catches it within hours instead of days because the alert was triggered, rolls back the update, and avoids what would have been a week of suppressed activation. The monthly deep-dive reveals that 30-Day Retention is strongest among users who complete 3+ workouts in their first week, leading to a new product hypothesis that becomes a roadmap item—demonstrating the link to connecting the North Star to product roadmap decisions.

## Best Practices

* Keep the North Star Metric visually dominant—use a larger font, a prominent position, and distinct color. It should be impossible to miss when the dashboard loads.
* Use consistent time granularity across all panels. If the North Star is measured weekly, show input metrics on the same weekly cadence to avoid apples-to-oranges comparisons.
* Include a 'last updated' timestamp on the dashboard so viewers always know how fresh the data is. Stale data presented as current leads to bad decisions.
* Add target lines or goal ranges to each metric. Showing a number without a benchmark forces people to guess whether it's good or bad, which defeats the purpose of visibility.
* Create team-specific sub-dashboards that drill into each input metric in detail, but always link back to the master North Star dashboard to maintain the hierarchy.
* Review and prune the dashboard quarterly. Metrics that no one looks at, panels that haven't been useful, or diagnostic views that are outdated should be removed to keep the dashboard focused.

## Common Mistakes

Cramming too many metrics onto the dashboard, turning it into a 'metrics graveyard' that nobody reads.

Correction

Limit the main dashboard to the North Star + 3–6 input metrics. Everything else belongs in team-specific sub-dashboards or exploratory notebooks. If you can't explain why a metric is on the dashboard in one sentence, remove it.

Building the dashboard but never establishing a review cadence, so it becomes digital wallpaper.

Correction

Commit to a weekly async summary and a monthly deep-dive from day one. Put these on the calendar before you share the dashboard. The cadence is what creates the habit of data-informed decision-making.

Using different metric definitions across the dashboard and other team reports, creating conflicting numbers.

Correction

Define every metric in a shared data dictionary with exact SQL logic. The dashboard should pull from the same source tables and use the same calculation as every other report. If there's a discrepancy, fix it immediately—trust erodes fast when numbers don't match.

Setting up alerts for every metric with tight thresholds, flooding Slack with noise until everyone mutes the channel.

Correction

Only alert on the North Star and the most critical 1–2 input metrics. Use thresholds that represent genuinely unusual movements (e.g., >2 standard deviations from the rolling average), not normal weekly variance.

Making the dashboard accessible only to the data or product team, undermining cross-functional alignment.

Correction

Default to company-wide read access. The entire purpose of the North Star framework is shared alignment—as covered in the sibling skill on aligning cross-functional teams around a shared North Star. If people can't see the numbers, they can't align around them.

## Other Skills in This Method

[Connecting Your North Star Metric to Product Roadmap DecisionsHow to use your North Star Metric and its input metrics to prioritize roadmap initiatives and justify strategic trade-offs.](https://tryhamster.com/skills/connecting-north-star-to-product-roadmap)[Validating Your North Star Metric with User ResearchHow to use qualitative user research and customer insights to confirm that your chosen North Star Metric truly reflects the value customers experience.](https://tryhamster.com/skills/validating-north-star-with-user-research)[Selecting the Right North Star Metric for Your ProductHow to evaluate candidate metrics and choose the single metric that best captures the core value customers get from your product.](https://tryhamster.com/skills/selecting-your-north-star-metric)[Evolving Your North Star Metric Across Product Growth StagesWhen and how to revisit, refine, or replace your North Star Metric as your product matures from MVP through scaling and beyond.](https://tryhamster.com/skills/evolving-north-star-across-growth-stages)[Aligning Cross-Functional Teams Around a Shared North StarTechniques for communicating, cascading, and embedding the North Star Metric across engineering, design, marketing, and other cross-functional teams to drive shared accountability.](https://tryhamster.com/skills/aligning-cross-functional-teams-around-north-star)[Identifying and Mapping Input Metrics to Your North StarHow to decompose your North Star Metric into actionable input metrics that teams can directly influence through their day-to-day work.](https://tryhamster.com/skills/identifying-input-metrics)

## Frequently Asked Questions

What's the best dashboard tool for tracking a North Star Metric?+

There's no single best tool—use what your organization already has. Looker, Tableau, Amplitude, Mixpanel, Metabase, and Mode are all viable. The most important factor is data freshness and company-wide accessibility, not the specific platform. A well-built Metabase dashboard beats a neglected Tableau implementation every time.

How often should I update my North Star dashboard?+

Aim for daily data refreshes at minimum. If your data pipeline supports it, near-real-time updates are ideal for input metrics that teams act on quickly. The North Star itself is typically reviewed on a weekly cadence, but having fresh underlying data lets teams spot problems early.

How many metrics should be on a North Star dashboard?+

Limit the primary dashboard to 4–7 metrics total: one North Star Metric plus 3–6 input metrics. Diagnostic breakdowns can appear below the fold, but the core view should be scannable in under 30 seconds. More metrics create noise and dilute focus.

How do I get non-data teams to actually use the North Star dashboard?+

Make it unavoidable. Pin the link in Slack, reference it in every all-hands, include a screenshot in weekly updates, and start every product review meeting by pulling it up. Establishing a weekly reporting cadence—as described in step 6—creates the habit. When teams see leadership using the dashboard, they follow.

Should I include revenue metrics on my North Star dashboard?+

Only if revenue is one of your defined input metrics or your North Star itself. Avoid adding revenue as a 'just because' metric—it clutters the dashboard and implies that revenue is the primary goal rather than customer value delivery. If needed, create a separate finance dashboard and link to it.

How does a data analytics product approach differ from a simple reporting dashboard?+

A data analytics product approach means treating the dashboard as a product itself—designed for specific users (your teams), solving a specific problem (visibility into what drives your North Star), and iterated on based on feedback. Simple reporting dashboards display data; a data analytics product approach surfaces actionable insights and drives decisions.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Skills","item":"https://tryhamster.com/skills"},{"@type":"ListItem","position":3,"name":"Building North Star Dashboards","item":"https://tryhamster.com/skills/building-north-star-dashboards"}]}
[{"@context":"https://schema.org","@type":"TechArticle","headline":"Building North Star Dashboards | Data Analytics Product","name":"Building North Star Dashboards | Data Analytics Product","description":"Learn to build dashboards tracking your North Star and input metrics for a data analytics product strategy.","image":"https://tryhamster.com/opengraph-image","url":"https://tryhamster.com/skills/building-north-star-dashboards","author":{"@type":"Organization","name":"Hamster","url":"https://tryhamster.com"},"publisher":{"@type":"Organization","name":"Hamster","url":"https://tryhamster.com"},"reviewedBy":{"@type":"Organization","name":"Hamster editorial team"},"datePublished":"2026-04-19","dateModified":"2026-04-19","isPartOf":{"@type":"Article","headline":"North Star Metric","url":"https://tryhamster.com/methods/north-star-metric"},"about":"data analytics product, north star metric dashboard, product metrics dashboard, north star metric tracking, input metrics dashboard","proficiencyLevel":"Intermediate"},{"@context":"https://schema.org","@type":"FAQPage","mainEntity":[{"@type":"Question","name":"What's the best dashboard tool for tracking a North Star Metric?","acceptedAnswer":{"@type":"Answer","text":"There's no single best tool—use what your organization already has. Looker, Tableau, Amplitude, Mixpanel, Metabase, and Mode are all viable. The most important factor is data freshness and company-wide accessibility, not the specific platform. A well-built Metabase dashboard beats a neglected Tableau implementation every time."}},{"@type":"Question","name":"How often should I update my North Star dashboard?","acceptedAnswer":{"@type":"Answer","text":"Aim for daily data refreshes at minimum. If your data pipeline supports it, near-real-time updates are ideal for input metrics that teams act on quickly. The North Star itself is typically reviewed on a weekly cadence, but having fresh underlying data lets teams spot problems early."}},{"@type":"Question","name":"How many metrics should be on a North Star dashboard?","acceptedAnswer":{"@type":"Answer","text":"Limit the primary dashboard to 4–7 metrics total: one North Star Metric plus 3–6 input metrics. Diagnostic breakdowns can appear below the fold, but the core view should be scannable in under 30 seconds. More metrics create noise and dilute focus."}},{"@type":"Question","name":"How do I get non-data teams to actually use the North Star dashboard?","acceptedAnswer":{"@type":"Answer","text":"Make it unavoidable. Pin the link in Slack, reference it in every all-hands, include a screenshot in weekly updates, and start every product review meeting by pulling it up. Establishing a weekly reporting cadence—as described in step 6—creates the habit. When teams see leadership using the dashboard, they follow."}},{"@type":"Question","name":"Should I include revenue metrics on my North Star dashboard?","acceptedAnswer":{"@type":"Answer","text":"Only if revenue is one of your defined input metrics or your North Star itself. Avoid adding revenue as a 'just because' metric—it clutters the dashboard and implies that revenue is the primary goal rather than customer value delivery. If needed, create a separate finance dashboard and link to it."}},{"@type":"Question","name":"How does a data analytics product approach differ from a simple reporting dashboard?","acceptedAnswer":{"@type":"Answer","text":"A data analytics product approach means treating the dashboard as a product itself—designed for specific users (your teams), solving a specific problem (visibility into what drives your North Star), and iterated on based on feedback. Simple reporting dashboards display data; a data analytics product approach surfaces actionable insights and drives decisions."}}]},{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Methods","item":"https://tryhamster.com/methods"},{"@type":"ListItem","position":2,"name":"North Star Metric","item":"https://tryhamster.com/methods/north-star-metric"},{"@type":"ListItem","position":3,"name":"Building North Star Dashboards | Data Analytics Product","item":"https://tryhamster.com/skills/building-north-star-dashboards"}]}]
```
