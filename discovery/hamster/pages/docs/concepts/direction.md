---
description: Direction turns speed into velocity by connecting Goals, Metrics, Results, and the work your team ships.
title: Direction | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Direction

* [Documentation](https://tryhamster.com/docs "Documentation")
* [Getting Started](https://tryhamster.com/docs/hamster-studio/getting-started "Getting Started")
* [Common Challenges](https://tryhamster.com/docs/solutions "Common Challenges")
* Concepts
* [Overview](https://tryhamster.com/docs/concepts "Overview")
* [Direction](https://tryhamster.com/docs/concepts/direction "Direction")
* [Discovery](https://tryhamster.com/docs/concepts/discovery "Discovery")
* [Delivery](https://tryhamster.com/docs/concepts/delivery "Delivery")
* [Knowledge](https://tryhamster.com/docs/concepts/knowledge "Knowledge")
* By stage
* [Small teams](https://tryhamster.com/docs/for/small-teams "Small teams")
* [Startups & mid-size](https://tryhamster.com/docs/for/startups-and-mid-size "Startups & mid-size")
* [Enterprise & scaling](https://tryhamster.com/docs/for/enterprise-and-scaling "Enterprise & scaling")
* [Joining a team](https://tryhamster.com/docs/joining-a-team "Joining a team")
* Direction
* [Goals](https://tryhamster.com/docs/hamster-studio/goals "Goals")
* [Metrics](https://tryhamster.com/docs/hamster-studio/metrics "Metrics")
* [Results](https://tryhamster.com/docs/hamster-studio/results "Results")
* Discovery

* Hamster Chat

* [Research Agents](https://tryhamster.com/docs/hamster-studio/research-agents "Research Agents")
* Delivery
* [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives "Initiatives")

* Briefs

* Plans

* Tasks

* [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents "Cloud Agents")
* [Routines](https://tryhamster.com/docs/hamster-studio/routines "Routines")
* Knowledge

* Blueprints

* Methods

* [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph "Context Graph")

* Connections

* Surfaces

* CLI

* MCP Server

* [Taskmaster](https://tryhamster.com/docs/taskmaster "Taskmaster")
* Workspace

* Teams

* Collaboration

* Account Settings

# Direction — where you're heading

[Direction](https://tryhamster.com/docs/concepts/direction) is how Hamster turns speed into velocity: movement toward outcomes your team actually cares about. It connects [Goals](https://tryhamster.com/docs/hamster-studio/goals), [Metrics](https://tryhamster.com/docs/hamster-studio/metrics), targets, and per-period [Results](https://tryhamster.com/docs/hamster-studio/results) so people and AI can reason from the same orientation before work moves into [Discovery](https://tryhamster.com/docs/concepts/discovery) and [Delivery](https://tryhamster.com/docs/concepts/delivery).

Here, strategy becomes operational context. You pick the frameworks your company already speaks, such as OKR or North Star, and define how progress should be understood over time. Hamster then gives the rest of the product a shared model to read from in [Goals](https://tryhamster.com/docs/hamster-studio/goals), [Hamster Chat](https://tryhamster.com/docs/hamster-studio/chat), [Plans](https://tryhamster.com/docs/hamster-studio/plans), and [Delivery](https://tryhamster.com/docs/concepts/delivery).

## Goals — durable direction

A [Goal](https://tryhamster.com/docs/hamster-studio/goals) is an outcome with a measurement story: what you're trying to move, how you'll know whether movement is happening, and how each period rolls up. Good [Goals](https://tryhamster.com/docs/hamster-studio/goals) keep the team oriented across many loops of [Discovery](https://tryhamster.com/docs/concepts/discovery) and [Delivery](https://tryhamster.com/docs/concepts/delivery), not just toward a single finish line.

[Goals](https://tryhamster.com/docs/hamster-studio/goals) give [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) their reason to exist. [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) collect the work aimed at moving a [Goal](https://tryhamster.com/docs/hamster-studio/goals); [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) define the shippable units inside each [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives). The flow goes [Goals](https://tryhamster.com/docs/hamster-studio/goals) → [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) → [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) → [Plans](https://tryhamster.com/docs/hamster-studio/plans) → [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) → PRs. Without [Goals](https://tryhamster.com/docs/hamster-studio/goals), [Delivery](https://tryhamster.com/docs/concepts/delivery) can look busy without creating velocity; with [Goals](https://tryhamster.com/docs/hamster-studio/goals), every [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) can be understood against the outcome it is meant to move.

Hamster ships with six measurement frameworks built in — OKR, OGSM, V2MOM, AARRR, HEART, and North Star. You pick the one that matches how your team already runs reviews; Hamster enforces the shape (a Key [Result](https://tryhamster.com/docs/hamster-studio/results) lives under an Objective in OKR, not under a Strategy) and you fill in the substance. You can run more than one framework at a time — a company-level OGSM alongside team-level OKRs — and switch later without disturbing downstream work.

## Metrics — how you count it

A [Metric](https://tryhamster.com/docs/hamster-studio/metrics) is the quantitative shape attached to a measurable [Goal](https://tryhamster.com/docs/hamster-studio/goals): what unit you use, which way is good, how numbers roll up, and what you're aiming at. Set it once per [Goal](https://tryhamster.com/docs/hamster-studio/goals) so every period's [Results](https://tryhamster.com/docs/hamster-studio/results) land against the same definition.

A [Metric](https://tryhamster.com/docs/hamster-studio/metrics) pins down five things:

* Unit — what you're counting (users, dollars, NPS points, conversion rate).
* [Direction](https://tryhamster.com/docs/concepts/direction) — whether increase, decrease, or maintain is "good" for that Goal.
* Aggregation — how raw inputs roll up across time (`sum`, `avg`, `last`, `max`, `min`).
* Baseline — an optional starting reference when you're establishing a new line.
* Target — the number the team is trying to reach.

OGSM Measures can additionally be tagged as _leading_ (an early signal) or _lagging_ (an outcome). Mixing them is how strategies stay honest — you can see whether early indicators are moving before the lagging numbers prove the strategy worked.

[Metrics](https://tryhamster.com/docs/hamster-studio/metrics) inherit their measurable eligibility from the framework template — Key [Results](https://tryhamster.com/docs/hamster-studio/results), OGSM Measures, AARRR/HEART [Metrics](https://tryhamster.com/docs/hamster-studio/metrics), North Star and Input Metrics. You don't attach a [Metric](https://tryhamster.com/docs/hamster-studio/metrics) to a non-measurable [Goal](https://tryhamster.com/docs/hamster-studio/goals) type; the hierarchy enforces that for you.

## Results — measurement over time

A [Result](https://tryhamster.com/docs/hamster-studio/results) is the per-period row for a measurable [Goal](https://tryhamster.com/docs/hamster-studio/goals): the target you intended, the actual you achieved, a status (On Track, At Risk, Off Track, Achieved, Missed), and optional confidence (0–1) when the team is still forecasting.

Your active [Goals](https://tryhamster.com/docs/hamster-studio/goals) framework has a cadence — quarterly, half-yearly, monthly, or continuous for always-on growth frameworks. Hamster generates periods from it (Q1 2026, H1 2026, April 2026) and gives each measurable [Goal](https://tryhamster.com/docs/hamster-studio/goals) one [Result](https://tryhamster.com/docs/hamster-studio/results) row per period. Targets and actuals can be logged as you go, so when review time comes, history is already there — no parallel spreadsheet.

[Results](https://tryhamster.com/docs/hamster-studio/results) always read against the [Metric](https://tryhamster.com/docs/hamster-studio/metrics) defined on the [Goal](https://tryhamster.com/docs/hamster-studio/goals), so "35% vs 40%" means the same thing in stand-ups, in the [Goals](https://tryhamster.com/docs/hamster-studio/goals) view, and in [Hamster Chat](https://tryhamster.com/docs/hamster-studio/chat). When an actual lands outside the band you care about, status makes "off track" visible without anyone curating a deck.

## Direction connects to Delivery through Initiatives

An [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) is how a [Goal](https://tryhamster.com/docs/hamster-studio/goals) becomes committed work — owned, tracked, and broken down into [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) that ship. Link one or more [Goals](https://tryhamster.com/docs/hamster-studio/goals) to each [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) so [Delivery](https://tryhamster.com/docs/concepts/delivery) ladders clearly to outcomes; the link is many-to-many with optional weights, so an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) that serves Activation 70% and Retention 30% can read honestly.

As [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) ship, the [Goals](https://tryhamster.com/docs/hamster-studio/goals) they serve move. The [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) view is where you see what work is driving each outcome.

## Direction stays current as work ships

Set a [Goal](https://tryhamster.com/docs/hamster-studio/goals) and attach a [Metric](https://tryhamster.com/docs/hamster-studio/metrics), and the AI assistant can suggest [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) to move it; new [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) can be created from it. As [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) ship and [Metrics](https://tryhamster.com/docs/hamster-studio/metrics) update, [Goal](https://tryhamster.com/docs/hamster-studio/goals) [Results](https://tryhamster.com/docs/hamster-studio/results) roll forward and statuses stay in sync with [Delivery](https://tryhamster.com/docs/concepts/delivery) — reviews start from live data tied to the work in flight.

## Where to go next

* [Discovery](https://tryhamster.com/docs/concepts/discovery)
* [Delivery](https://tryhamster.com/docs/concepts/delivery)
* [Knowledge](https://tryhamster.com/docs/concepts/knowledge)
* [Goals](https://tryhamster.com/docs/hamster-studio/goals)
* [Metrics](https://tryhamster.com/docs/hamster-studio/metrics)
* [Results](https://tryhamster.com/docs/hamster-studio/results)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Concepts","item":"https://tryhamster.com/docs/concepts"},{"@type":"ListItem","position":4,"name":"Direction","item":"https://tryhamster.com/docs/concepts/direction"}]}
```
