---
description: Learn customer journey analytics techniques for tracking how consumers add and remove brands during active evaluation. Learn how Hamster helps teams...
title: Analyzing Active Evaluation Behavior | Journey Analytics
image: https://tryhamster.com/skills/analyzing-active-evaluation-behavior/opengraph-image-1tdarl?74b99121c50772fb
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

# Analyzing Active Evaluation Behavior with Customer Journey Analytics

This skill teaches you how to track and interpret consumer behavior during the active evaluation phase of the McKinsey Consumer Decision Journey—specifically how people research, compare, and progressively narrow or expand their brand consideration set before buying.

To analyze active evaluation behavior, track how consumers add and remove brands from their consideration set during digital research, review reading, and peer consultation. Map touchpoint sequences using customer journey analytics tools, tag evaluation-stage interactions (comparison pages, review sites, social mentions), and measure which content causes brands to be added or eliminated. This reveals where you win or lose against competitors before purchase.

Outcome: You gain the ability to identify exactly where and why consumers add or drop your brand during evaluation, enabling you to intervene at the moments that actually determine purchase decisions.

[Add to Hamster](https://tryhamster.com/auth/sign-up?utm%5Fsource=website&utm%5Fmedium=pseo&utm%5Fcampaign=skill-analyzing-active-evaluation-behavior&utm%5Fcontent=hero)[or download skill pack](https://tryhamster.com/%5Fsite/api/download/skill/mckinsey-consumer-decision-journey/analyzing-active-evaluation-behavior)

Apr 29, 2026

MarketingIntermediate2-4 hours for initial setup; ongoing monitoring

## Prerequisites

* Understanding of the McKinsey Consumer Decision Journey framework
* Familiarity with web analytics tools (GA4 or similar)
* Basic knowledge of mapping initial consideration sets
* Access to brand mention or social listening tools

## Overview

The active evaluation phase is where purchase decisions are truly won or lost. Unlike the old funnel model—where brands assumed a steady narrowing from awareness to purchase—McKinsey's research showed that consumers actively add brands during this phase just as often as they eliminate them. A consumer might start with three brands in mind, discover two more through Google searches and Reddit threads, and ultimately drop four of the five after reading reviews. Understanding this dynamic reshuffling is the core of customer journey analytics applied to the decision journey.

Analyzing active evaluation behavior means building a systematic practice of tracking which touchpoints cause consumers to include or exclude your brand. This goes beyond pageview-level analytics. It requires stitching together signals from comparison site visits, review platform engagement, social media research patterns, peer conversations, and direct brand interactions to reconstruct the evaluative arc each consumer travels.

This skill is essential because most marketing teams over-invest in awareness (top of funnel) and conversion (bottom of funnel) while neglecting the messy middle where brand preference actually forms. When you understand active evaluation behavior, you can allocate budget and content to the touchpoints that genuinely shift consideration—not just the ones that are easiest to measure.

## How It Works

Active evaluation behavior analysis works by treating the evaluation phase as a series of discrete events where a consumer's consideration set changes. Each event has a trigger (what prompted the research), a touchpoint (where the research happened), and an outcome (brand added, brand reinforced, or brand eliminated).

The conceptual model borrows from customer journey analytics by mapping these events across time and channels. Unlike linear funnel analytics that measure progression through stages, active evaluation analysis measures lateral movement—how the consideration set expands and contracts simultaneously. A consumer reading a 'best project management tools' article might add two new brands while mentally eliminating one they previously considered, all in a single session.

The mechanism relies on three data layers. The first is behavioral data: what pages, searches, and content a consumer engages with during evaluation. The second is competitive data: where your brand appears alongside competitors in comparison contexts. The third is qualitative data: what consumers say about their evaluation process in surveys, reviews, and social discussions. By triangulating these three layers, you build a picture of evaluation dynamics that no single data source can provide.

This approach aligns with the broader McKinsey Consumer Decision Journey framework by acknowledging that the path from initial consideration to purchase is non-linear and heavily influenced by consumer-driven research rather than brand-pushed messaging.

## Step-by-Step

1. ### Step 1: Define Your Evaluation Touchpoint Inventory  
Before you can analyze behavior, you need a comprehensive map of every touchpoint where active evaluation happens in your category. This includes your own properties (comparison pages, pricing pages, feature pages, case studies) and third-party properties (review sites like G2 or Capterra, comparison articles from publishers, Reddit threads, YouTube reviews, social media discussions).  
Create a spreadsheet with columns for: touchpoint name, platform/channel, type (brand-owned vs. third-party), whether you can track behavior directly, and estimated influence level. For B2B SaaS, your inventory might include G2 comparison pages, Capterra reviews, competitor blog comparisons, your own pricing page, product demo videos, and industry analyst reports.  
Don't limit this to digital touchpoints. If your category involves in-store evaluation, peer recommendations, or sales conversations, include those too. The goal is completeness—you'll prioritize later.  
Tip: Interview 5-10 recent customers and ask them to walk you through their evaluation process step by step. You'll discover touchpoints you never considered, like niche Slack communities or specific influencers.
2. ### Step 2: Instrument Evaluation-Stage Tracking  
Set up analytics to capture evaluation-specific behaviors. In GA4 or your analytics tool, create event tracking for signals that indicate active evaluation rather than casual browsing. Key evaluation signals include: visiting a pricing or comparison page, viewing three or more product feature pages in a session, returning to the site after visiting a competitor's site (detectable via referral data), downloading comparison guides, and engaging with review content.  
Create a custom audience segment in your analytics platform for 'active evaluators'—visitors whose behavior pattern matches evaluation rather than awareness or post-purchase activity. This typically means multi-page sessions focused on product details, pricing, and differentiation content, often with return visits over days or weeks.  
For third-party touchpoints you can't directly instrument, use brand monitoring tools (Mention, Brandwatch, or even Google Alerts) to track when your brand appears in evaluative contexts—comparison articles, review discussions, 'vs' searches, and recommendation threads.  
Tip: Set up UTM parameters specifically for evaluation-stage content. Use utm\_medium=evaluation or a similar convention so you can easily filter for evaluation touchpoints in your customer journey analytics reports.
3. ### Step 3: Map Consideration Set Dynamics  
This is the core analytical step. You need to understand how your brand enters and exits consumer consideration sets. There are two complementary approaches.  
Quantitative approach: Analyze search query data (via Google Search Console and paid search reports) for evaluation-intent keywords. Track queries containing 'vs,' 'alternative to,' 'compared to,' 'best \[category\],' and 'review.' Monitor which competitor brands appear alongside yours in these queries and how that changes over time. Use tools like Semrush or Ahrefs to track your share of voice in comparison and evaluation keywords.  
Qualitative approach: Conduct win/loss interviews with recent customers and lost prospects. Ask specifically: 'Which brands did you consider? When did you add or remove each brand? What caused each addition or removal?' Document the trigger events that caused consideration set changes. Common triggers include a compelling review, a peer recommendation, a negative experience with a competitor's demo, or discovering a price discrepancy.  
Combine both approaches into a consideration set flow diagram showing typical patterns: which brands consumers start with, which they add during evaluation, and which survive to the purchase decision.  
Tip: Pay special attention to brands that get added late in evaluation—these are often the ones that win. McKinsey's original research found that brands added during active evaluation have disproportionately high conversion rates.
4. ### Step 4: Identify Brand Addition and Elimination Triggers  
With your data from Step 3, categorize the specific triggers that cause brands to be added to or eliminated from consideration sets. Create two lists: addition triggers (what causes consumers to discover and add your brand during evaluation) and elimination triggers (what causes consumers to drop your brand).  
Common addition triggers include: appearing in a 'best of' article, strong G2/Capterra rating, recommendation from a peer or community, compelling comparison content that highlights unique strengths, and retargeting ads that surface at the right evaluation moment.  
Common elimination triggers include: negative reviews mentioning specific pain points, pricing that's significantly above expectations, poor demo experience, missing a must-have feature discovered during comparison, slow or unhelpful sales response, and outdated content that suggests the product is stagnant.  
Quantify these triggers where possible. If 40% of lost prospects mention pricing as the elimination trigger, that's a different strategic problem than if 40% mention missing a specific feature. This analysis directly informs where to invest in content, product, and experience improvements.  
Tip: Elimination triggers are often more actionable than addition triggers. Fixing a common reason people drop you can have a bigger impact than trying to get added to more consideration sets.
5. ### Step 5: Analyze Competitive Overlap in Evaluation Contexts  
Map exactly where and how your brand co-appears with competitors during the evaluation phase. This competitive overlap analysis reveals your true competitive set (which may differ from who you think your competitors are) and shows where evaluation battles are happening.  
Use customer journey analytics tools and search data to identify: which competitors appear in the same 'vs' searches as your brand, which competitors share review site categories with you, which brands consumers mention together in social discussions, and which competitors' content ranks for the same evaluation-intent keywords.  
Create a competitive co-occurrence matrix showing how frequently each competitor appears alongside your brand in evaluation contexts. High co-occurrence with a specific competitor means you need differentiation content targeting that pairing specifically. Low co-occurrence with a brand you consider a competitor might mean consumers don't actually compare you—you're in different mental categories.  
Audit the comparison and review content that exists for each competitive pairing. Is the existing content accurate? Is it favorable to you? Are there gaps where no comparison content exists, leaving consumers to guess?  
Tip: Check who's creating the comparison content consumers find. If a competitor controls the 'Brand A vs Your Brand' narrative by publishing their own comparison pages, you need to create balanced comparison content that consumers will trust more.
6. ### Step 6: Build Evaluation-Phase Intervention Points  
Based on your analysis, identify the specific moments where intervention can change evaluation outcomes. An intervention point is a combination of a touchpoint, a consumer need at that touchpoint, and content or experience you can provide.  
For each major evaluation touchpoint from your inventory, define: what consumers need at this point (information, reassurance, social proof, a direct comparison), what you currently provide, and what you should provide. Map these to your addition and elimination triggers.  
For example, if your analysis shows that consumers who visit your pricing page and then visit a competitor's pricing page tend to eliminate you (detectable via exit page + competitor referral on return visits), the intervention might be: add a comparison pricing table directly on your pricing page, include an ROI calculator, or add testimonials from customers who evaluated competitors.  
Prioritize interventions by: volume of consumers at that touchpoint × likelihood that the intervention changes the evaluation outcome × feasibility of implementation. This gives you a ranked action plan.  
Tip: Don't just create more content—improve existing evaluation touchpoints first. A better pricing page, a more honest comparison page, or faster demo booking often outperforms new blog posts.
7. ### Step 7: Establish Ongoing Monitoring and Iteration  
Active evaluation behavior shifts as markets evolve, competitors change tactics, and consumer preferences develop. Set up recurring monitoring to keep your analysis current.  
Create a monthly dashboard that tracks: evaluation-intent search volume and your share of voice, review site ratings and sentiment trends, consideration set composition from win/loss interviews (quarterly), conversion rates from evaluation-stage touchpoints, and competitive content changes in your category.  
Review this dashboard monthly with both marketing and product teams. Many elimination triggers are product issues masquerading as marketing problems—a feature gap that competitors highlight in comparisons isn't solved with better ad copy.  
Iterate your intervention points quarterly. Test different approaches to the same evaluation moment (e.g., A/B test comparison page formats) and retire interventions that aren't changing evaluation outcomes. Feed your findings back into the broader McKinsey Consumer Decision Journey analysis to understand how evaluation dynamics connect to the initial consideration set and moment of purchase.  
Tip: Track the time consumers spend in active evaluation. If your category's average evaluation period is shortening, it often means one competitor is making the decision easier—study what they're doing differently.

## Examples

### Example: B2B SaaS Project Management Tool

A mid-market project management SaaS company notices they appear in many initial consideration sets (based on brand awareness surveys) but their win rate against two key competitors has dropped 15% over six months. They need to understand what's happening during active evaluation.

The team begins by inventorying evaluation touchpoints: G2 comparison pages, Capterra reviews, five major 'best project management tools' articles ranking on page one, their own comparison pages, the pricing page, and product demo flow.

They instrument evaluation-stage tracking in GA4, creating a custom segment for visitors who view the pricing page AND at least two feature pages in a session. They set up Mention alerts for their brand appearing alongside competitor names.

Win/loss interviews with 20 recent deals reveal the pattern: prospects add their brand to the shortlist from 'best of' articles, evaluate features on their site, then check G2 head-to-head comparisons. The elimination trigger for 8 of 12 lost deals was a specific integration gap that competitors highlighted in G2 comparisons and their own comparison pages.

The team creates three interventions: (1) an honest comparison page addressing the integration gap with a workaround and roadmap commitment, (2) outreach to G2 reviewers who mentioned the integration positively to encourage updates, and (3) an FAQ section on their pricing page addressing the three most common evaluation-stage objections from interview data. Within one quarter, win rate against the two competitors improves by 9%.

### Example: Direct-to-Consumer Skincare Brand

A DTC skincare brand selling through their own website and Amazon sees that branded search volume is growing but conversion rate is declining. Customer journey analytics shows visitors are spending more time on the site before purchasing or leaving—suggesting a longer, more complex active evaluation phase.

The brand maps evaluation touchpoints for their category: Instagram ingredient review accounts, Reddit's r/SkincareAddiction, Dermstore comparison articles, Amazon review pages, TikTok dermatologist reviews, and beauty publication roundups.

Using search query data, they discover a spike in '\[brand name\] vs \[competitor\]' searches over the past quarter, driven by a competitor's aggressive influencer campaign. Social listening reveals that the competitor's campaign introduced a specific ingredient claim that consumers now use as an evaluation criterion.

The brand analyzes Amazon review data and finds their product has a 4.3 rating but the competitor has a 4.6—and the rating gap is driven entirely by reviews mentioning the specific ingredient in question. Their product actually contains a superior version of the same ingredient but doesn't communicate this clearly.

Interventions: (1) update product descriptions on all channels to explicitly address the ingredient comparison, (2) partner with three dermatologists to create evaluation-stage content explaining ingredient differences, (3) add a comparison section to their product pages showing clinical data for their ingredient formulation vs. alternatives. They also create structured content optimized for customer journey analytics targeting 'ingredient A vs ingredient B' searches, capturing consumers in active evaluation who are comparing the underlying science.

## Best Practices

* Track both additions and eliminations separately—they have different triggers and require different responses. Most teams only analyze why they won; analyzing why you were eliminated is often more valuable.
* Use win/loss interview data as the qualitative backbone and analytics as the quantitative validation. Neither source alone gives you the full picture of active evaluation behavior.
* Segment your evaluation analysis by buyer persona. A technical evaluator and an executive sponsor evaluate completely differently—different touchpoints, different triggers, different timelines.
* Monitor third-party review sites and comparison content as actively as your own analytics. For many categories, the evaluation battle is won or lost on sites you don't control.
* Connect evaluation behavior data to revenue outcomes, not just traffic metrics. A touchpoint that influences 50 high-value purchases matters more than one that drives 5,000 pageviews from casual browsers.
* Update your evaluation touchpoint inventory quarterly. New review platforms, communities, and content formats emerge constantly—if you're not tracking the latest places consumers evaluate, your analysis has blind spots.

## Common Mistakes

Treating evaluation as a linear narrowing process instead of a dynamic reshuffling

Correction

The core McKinsey insight is that consumers add brands during evaluation, not just eliminate them. Your customer journey analytics must track additions and expansions of the consideration set, not just attrition. Build your tracking to capture both directions of consideration set change.

Only analyzing owned touchpoints and ignoring third-party evaluation contexts

Correction

Most active evaluation happens on sites you don't own—review platforms, Reddit, comparison blogs, YouTube. Set up brand monitoring and competitive intelligence for these third-party touchpoints. If you only analyze your own website data, you're seeing a fraction of the evaluation journey.

Conflating awareness-stage metrics with evaluation-stage behavior

Correction

A consumer visiting your homepage from a display ad is an awareness touchpoint. A consumer visiting your pricing page after reading a G2 comparison is an evaluation touchpoint. Separate these in your analytics by creating evaluation-specific segments based on behavioral patterns (multi-page product sessions, comparison content engagement, return visits).

Treating all competitor comparisons as equal threats

Correction

Build a competitive co-occurrence matrix to understand which competitors consumers actually compare you against. Invest differentiation content and resources against high-co-occurrence competitors, not the competitors your leadership team worries about. Your perceived competitive set and your actual evaluation competitive set are often different.

Collecting evaluation data but not connecting it to actionable intervention points

Correction

Every piece of evaluation analysis should answer: 'What should we change or create to influence this evaluation moment?' If your analysis produces interesting dashboards but no action items, restructure it around the intervention framework—touchpoint × consumer need × content or experience response.

## Other Skills in This Method

[Mapping the Initial Consideration SetHow to identify and analyze the brands and options consumers include in their initial consideration set before active research begins.](https://tryhamster.com/skills/mapping-initial-consideration-sets)[Optimizing Moment-of-Purchase TriggersHow to identify and influence the critical decision-stage touchpoints that convert active evaluators into buyers at the point of purchase.](https://tryhamster.com/skills/optimizing-moment-of-purchase-triggers)[Building Post-Purchase Loyalty LoopsDesigning post-purchase experiences that create ongoing loyalty loops so customers skip re-evaluation and repurchase directly.](https://tryhamster.com/skills/building-post-purchase-loyalty-loops)[Identifying Touchpoints Across CDJ StagesHow to audit and catalog every brand touchpoint across the four CDJ phases to find gaps and high-impact interaction opportunities.](https://tryhamster.com/skills/identifying-touchpoints-across-cdj-stages)[Creating Circular Consumer Journey MapsStep-by-step process for building a circular customer journey map based on the CDJ model instead of a traditional linear funnel.](https://tryhamster.com/skills/creating-circular-journey-maps)[Replacing Funnel Thinking with the Decision JourneyHow to transition your marketing strategy from a linear customer journey funnel to the non-linear CDJ model with practical examples.](https://tryhamster.com/skills/replacing-funnel-thinking-with-cdj)

## Frequently Asked Questions

What is active evaluation in the McKinsey Consumer Decision Journey?+

Active evaluation is the phase where consumers actively research, compare, and reshape their consideration set by adding and removing brands. Unlike the traditional funnel where options only narrow, McKinsey found consumers frequently add new brands during this phase through digital research, reviews, peer input, and comparison shopping.

How does customer journey analytics help track active evaluation behavior?+

Customer journey analytics tracks evaluation-stage signals like comparison page visits, review site engagement, competitor-related search queries, and multi-session research patterns. By stitching these touchpoints together, you can see how consumers move through evaluation, which content influences their consideration set changes, and where brands get added or eliminated.

What tools do I need to analyze active evaluation behavior?+

At minimum, you need web analytics (GA4), search console data, and a brand monitoring tool. For deeper analysis, add a social listening platform, competitive SEO tool (Ahrefs or Semrush), and review monitoring for platforms like G2 or Capterra. Supplement with qualitative data from win/loss customer interviews.

How do I know if consumers are adding or removing my brand during evaluation?+

Track branded search volume trends alongside evaluation-intent queries like 'best \[category\]' and '\[brand\] vs \[competitor\].' Win/loss interviews reveal specific addition and elimination triggers. Rising 'vs' search volume suggests you're being evaluated more; declining win rates despite stable consideration suggest elimination problems.

How often should I update my active evaluation analysis?+

Review quantitative evaluation metrics monthly (search data, review ratings, evaluation-stage conversion rates). Conduct qualitative win/loss interviews quarterly. Do a full touchpoint inventory refresh and competitive co-occurrence analysis every six months, or whenever a major competitor launches a new campaign or product.

What's the difference between analyzing evaluation behavior and running a traditional competitive analysis?+

Traditional competitive analysis compares features, pricing, and positioning statically. Evaluation behavior analysis tracks the dynamic process consumers go through when comparing brands—which touchpoints they use, what triggers add or eliminate brands, and how consideration sets change over time. It's consumer-centric rather than company-centric.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Skills","item":"https://tryhamster.com/skills"},{"@type":"ListItem","position":3,"name":"Analyzing Active Evaluation Behavior","item":"https://tryhamster.com/skills/analyzing-active-evaluation-behavior"}]}
[{"@context":"https://schema.org","@type":"TechArticle","headline":"Analyzing Active Evaluation Behavior | Journey Analytics","name":"Analyzing Active Evaluation Behavior | Journey Analytics","description":"Learn customer journey analytics techniques for tracking how consumers add and remove brands during active evaluation.","image":"https://tryhamster.com/opengraph-image","url":"https://tryhamster.com/skills/analyzing-active-evaluation-behavior","author":{"@type":"Organization","name":"Hamster","url":"https://tryhamster.com"},"publisher":{"@type":"Organization","name":"Hamster","url":"https://tryhamster.com"},"datePublished":"2026-04-29","dateModified":"2026-04-29","isPartOf":{"@type":"Article","headline":"McKinsey Consumer Decision Journey","url":"https://tryhamster.com/methods/mckinsey-consumer-decision-journey"},"about":"customer journey analytics, active evaluation phase, consumer decision journey analysis, brand consideration set tracking, evaluation behavior analytics","proficiencyLevel":"Intermediate"},{"@context":"https://schema.org","@type":"FAQPage","mainEntity":[{"@type":"Question","name":"What is active evaluation in the McKinsey Consumer Decision Journey?","acceptedAnswer":{"@type":"Answer","text":"Active evaluation is the phase where consumers actively research, compare, and reshape their consideration set by adding and removing brands. Unlike the traditional funnel where options only narrow, McKinsey found consumers frequently add new brands during this phase through digital research, reviews, peer input, and comparison shopping."}},{"@type":"Question","name":"How does customer journey analytics help track active evaluation behavior?","acceptedAnswer":{"@type":"Answer","text":"Customer journey analytics tracks evaluation-stage signals like comparison page visits, review site engagement, competitor-related search queries, and multi-session research patterns. By stitching these touchpoints together, you can see how consumers move through evaluation, which content influences their consideration set changes, and where brands get added or eliminated."}},{"@type":"Question","name":"What tools do I need to analyze active evaluation behavior?","acceptedAnswer":{"@type":"Answer","text":"At minimum, you need web analytics (GA4), search console data, and a brand monitoring tool. For deeper analysis, add a social listening platform, competitive SEO tool (Ahrefs or Semrush), and review monitoring for platforms like G2 or Capterra. Supplement with qualitative data from win/loss customer interviews."}},{"@type":"Question","name":"How do I know if consumers are adding or removing my brand during evaluation?","acceptedAnswer":{"@type":"Answer","text":"Track branded search volume trends alongside evaluation-intent queries like 'best [category]' and '[brand] vs [competitor].' Win/loss interviews reveal specific addition and elimination triggers. Rising 'vs' search volume suggests you're being evaluated more; declining win rates despite stable consideration suggest elimination problems."}},{"@type":"Question","name":"How often should I update my active evaluation analysis?","acceptedAnswer":{"@type":"Answer","text":"Review quantitative evaluation metrics monthly (search data, review ratings, evaluation-stage conversion rates). Conduct qualitative win/loss interviews quarterly. Do a full touchpoint inventory refresh and competitive co-occurrence analysis every six months, or whenever a major competitor launches a new campaign or product."}},{"@type":"Question","name":"What's the difference between analyzing evaluation behavior and running a traditional competitive analysis?","acceptedAnswer":{"@type":"Answer","text":"Traditional competitive analysis compares features, pricing, and positioning statically. Evaluation behavior analysis tracks the dynamic process consumers go through when comparing brands—which touchpoints they use, what triggers add or eliminate brands, and how consideration sets change over time. It's consumer-centric rather than company-centric."}}]},{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Methods","item":"https://tryhamster.com/methods"},{"@type":"ListItem","position":2,"name":"McKinsey Consumer Decision Journey","item":"https://tryhamster.com/methods/mckinsey-consumer-decision-journey"},{"@type":"ListItem","position":3,"name":"Analyzing Active Evaluation Behavior | Journey Analytics","item":"https://tryhamster.com/skills/analyzing-active-evaluation-behavior"}]}]
```
