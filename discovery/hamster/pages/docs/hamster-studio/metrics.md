---
description: Define how measurable goals are quantified — unit, direction, aggregation, baselines, and targets — with one definition from Goals through to shipped work.
title: Metrics | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Metrics

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

# Metrics

_[Metrics](https://tryhamster.com/docs/hamster-studio/metrics) are the definition of “how we count it.” Every measurable [Goal](https://tryhamster.com/docs/hamster-studio/goals) type — Key [Result](https://tryhamster.com/docs/hamster-studio/results), Measure, AARRR/HEART [Metric](https://tryhamster.com/docs/hamster-studio/metrics), North Star input, and others — can carry a [Metric](https://tryhamster.com/docs/hamster-studio/metrics): what unit you use, which way is good, how numbers roll up, and what you’re aiming at._

## Overview

A **[Metric](https://tryhamster.com/docs/hamster-studio/metrics)** in Hamster is the quantitative shape attached to a measurable node in your framework. You set it once per goal (or inherited type) so [Results](https://tryhamster.com/docs/hamster-studio/results) have a clear place to land each period: targets, actuals, and status all read against the same definition.

Hamster supports:

* Unit — what you’re counting (users, dollars, NPS points, conversion rate, and so on).
* [Direction](https://tryhamster.com/docs/concepts/direction) — whether increase, decrease, or maintain is “good” for that goal.
* Aggregation — how raw inputs roll up across time or dimensions (`sum`, `avg`, `last`, `max`, `min`).
* Baseline — an optional starting reference when you’re establishing a new line.
* Target — the number the team is trying to reach (per period or as a standing target, depending on the framework).
* Leading vs lagging (OGSM) — tag a measure as **leading** when it’s an early signal, or **lagging** when it reports outcomes.

[Metrics](https://tryhamster.com/docs/hamster-studio/metrics) inherit their **measurable** eligibility from the framework template — Key [Results](https://tryhamster.com/docs/hamster-studio/results), OGSM Measures, AARRR/HEART [Metrics](https://tryhamster.com/docs/hamster-studio/metrics), North Star and Input [Metrics](https://tryhamster.com/docs/hamster-studio/metrics), and other types the template marks as measurable. You don’t attach a [Metric](https://tryhamster.com/docs/hamster-studio/metrics) to a non-measurable goal type; the hierarchy enforces that for you.

## How metrics connect to Goals and Results

1. Framework → measurable goal — From your [Goals](https://tryhamster.com/docs/hamster-studio/goals) hierarchy, open a goal type that supports measurement.
2. Define the [Metric](https://tryhamster.com/docs/hamster-studio/metrics) — Set unit, [Direction](https://tryhamster.com/docs/concepts/direction), aggregation, optional baseline, and target so everyone agrees how progress is computed.
3. [Results](https://tryhamster.com/docs/hamster-studio/results) — Each reporting period (from the framework’s cadence) logs a target and actual against the same [Metric](https://tryhamster.com/docs/hamster-studio/metrics) definition, plus status and optional confidence.

Changing a [Metric](https://tryhamster.com/docs/hamster-studio/metrics)’s definition is deliberate — historical [Results](https://tryhamster.com/docs/hamster-studio/results) stay tied to the definition they were recorded against where versioning applies, so reviews stay comparable.

## How initiatives and briefs use metrics

[Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) link to goals; the [Metrics](https://tryhamster.com/docs/hamster-studio/metrics) on those goals are what “moving the number” refers to in planning and in chat. When the AI assistant proposes work, it can reference the same [Metric](https://tryhamster.com/docs/hamster-studio/metrics) language your team used when defining the goal.

## Roles and permissions

Creating and editing [Metrics](https://tryhamster.com/docs/hamster-studio/metrics) on goals follows the same **`goals.manage`** permission as frameworks and results. [Roles & Permissions](https://tryhamster.com/docs/hamster-studio/teams/roles-permissions) cover who holds it.

## Related

* [Goals](https://tryhamster.com/docs/hamster-studio/goals)
* [Results](https://tryhamster.com/docs/hamster-studio/results)
* [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives)
* [Direction](https://tryhamster.com/docs/concepts/direction)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Metrics","item":"https://tryhamster.com/docs/hamster-studio/metrics"}]}
```
