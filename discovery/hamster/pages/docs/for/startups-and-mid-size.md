---
description: Run Hamster across multiple product teams. Connect a richer Context Graph, build blueprints per product surface, and ship change through aligned briefs.
title: How to use Hamster: Startups and mid-size companies | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Startups & mid-size

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

# How to use Hamster: Startups and mid-size companies

A guide for admins setting up Hamster at a 10–50 person product org. Post-PMF, multiple product teams, engineers all using AI coding tools. Covers connecting a richer [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph) across multiple repos and tools, building [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) per product surface, setting [Direction](https://tryhamster.com/docs/concepts/direction) with Goals, codifying [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) that hold up across engineers, and shipping change through [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) grouped into Initiatives.

> Under 10 people? [How to use Hamster: Small teams](https://tryhamster.com/docs/for/small-teams) is the right starting point. Want to try Hamster on a single [Brief](https://tryhamster.com/docs/hamster-studio/briefs) first without the setup? See [Just ship](https://tryhamster.com/docs/concepts#what-this-means-in-practice).

Running Hamster across multiple teams

\~3 minutes

Video coming soon

## Setting up your workspace

### Organise your teams

At this stage you typically have one Hamster workspace with multiple teams underneath — for example, "Growth", "Core Platform", "Mobile", "Marketing". Each team has its own [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Plans](https://tryhamster.com/docs/hamster-studio/plans), and deliveries; integrations and [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) live at the workspace level.

Walk through onboarding once with the founding admin, then invite the rest of the org. Default new invites to Reviewer and promote to Creator as people start writing briefs. The Reviewer role is read-only on [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) and [Plans](https://tryhamster.com/docs/hamster-studio/plans) but can comment, vote alignment, and use Slack — a good default for non-builders and stakeholders. See [Roles & permissions](https://tryhamster.com/docs/hamster-studio/teams/roles-permissions) for the full role model.

Top tip: Send the [Joining a team on Hamster](https://tryhamster.com/docs/joining-a-team) guide to everyone you invite. It gets ICs (engineers, designers, stakeholders) oriented in 10 minutes.

### Connect your full Context Graph

A richer [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph) is the single biggest difference between this stage and the small-team setup. The more your team has accumulated in real systems — Linear tickets, Figma frames, customer-call recordings — the more grounded the [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) Hamster generates and the better every [Brief](https://tryhamster.com/docs/hamster-studio/briefs) gets refined.

[Connections](https://tryhamster.com/docs/hamster-studio/connections) worth investing in here:

* [GitHub](https://tryhamster.com/docs/hamster-studio/connections/github) — at this scale, configure at the GitHub-org level. Hamster reads code and PR history across all your repos.
* [Linear](https://tryhamster.com/docs/hamster-studio/connections/linear) (or Jira) — bidirectional sync of [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), and initiatives. [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) in Hamster, task-level state visible in Linear, so existing rituals (stand-ups, sprint review) stay intact.
* [Figma](https://tryhamster.com/docs/hamster-studio/connections/figma) — designers attach `.fig` files and Figma URLs to [Briefs](https://tryhamster.com/docs/hamster-studio/briefs); the AI agent uses them as grounding context for the [Plan](https://tryhamster.com/docs/hamster-studio/plans) and delivery.
* [Notion](https://tryhamster.com/docs/hamster-studio/connections/notion) and [Google Drive](https://tryhamster.com/docs/hamster-studio/connections/google-drive) — turn existing wiki pages and shared docs into context the AI agent reads.
* [Slack](https://tryhamster.com/docs/hamster-studio/connections/slack) — the bot, the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) side panel, slash commands. Where most non-builders interact with Hamster.
* [Meeting Agent](https://tryhamster.com/docs/hamster-studio/connections/meeting-agent) — capture customer calls and design reviews; transcripts auto-link to the relevant brief.

See [Connections overview](https://tryhamster.com/docs/hamster-studio/connections/overview) for the full list.

### Wire up the IDE flow for engineers (the most-used path)

At this scale, most of your engineers already use Claude Code, Cursor, Codex, or similar. The biggest unlock for adoption is exposing your [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph), [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), and [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) inside the tool they already use.

Two pieces, installed by each engineer:

* The [Hamster CLI](https://tryhamster.com/docs/hamster-studio/cli) — handles auth, skills sync, slash commands, scoped context. Lives in the terminal next to git and gh.
* The [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) — once connected to Claude Code or Cursor, an engineer can say "ship the \[Brief title\] Brief" or "show me what's in \[Initiative\]" and their AI assistant has every piece of context Hamster's seen. No copy-paste, no tab-switching.

This is the path that makes engineers happy. They stay in control, ship from where they live, and get the team's accumulated context for free. Make sure the MCP setup is documented in your engineering onboarding.

### Cloud Agents per repo (for delivery without an engineer at the keyboard)

A [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) is the configured environment Hamster runs deliveries in when nobody's hands are on a keyboard — repo URL, env vars, build and test commands, runtime.

[Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) complement the IDE flow rather than replacing it. They're how:

* A PM kicks off a [Delivery](https://tryhamster.com/docs/concepts/delivery) on a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) without an engineer in the loop.
* [Routines](https://tryhamster.com/docs/hamster-studio/routines) run scheduled or event-driven deliveries.
* Multiple deliveries happen in parallel without queuing on engineer time.

If your team has multiple repos shared across product teams, configure one [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) per repo. If you have multiple environments (e.g. `staging-api` and `production-api`), configure a [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) per environment.

Top tip: Lock production-deploying [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) to senior engineers using the [permissions model](https://tryhamster.com/docs/hamster-studio/teams/roles-permissions). Reviewers can read configurations but can't trigger deliveries.

## Building blueprints per product surface

At small-team scale, one [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) covers most of the product. At 10–50 people, you'll typically have multiple product surfaces — a web app, a mobile app, a public API, an internal admin tool — and each deserves its own [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints).

Hamster generates first drafts from your Context Graph. Spend a sprint reviewing and editing them. The pattern that works: each product team owns the [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) for the surface they ship into, edits it as the surface evolves, and treats the [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) as the canonical answer to "what is this surface today?"

[Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) are bidirectional. If your team migrates from one architecture to another, the [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) updates as the new code lands. If you author a new architecture doc in Notion, the [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) absorbs it on the next sync.

## Set Direction with Goals

At 10–50 people, "what are we optimising for this quarter?" stops being obvious. [Goals](https://tryhamster.com/docs/hamster-studio/goals) is where the answer lives, in a framework your team already speaks.

Pick a framework that matches how your team runs reviews — OKR, OGSM, V2MOM, AARRR, HEART, or North Star. Most product orgs at this scale run OKR at the team level and either OGSM or a North Star at the company level; pick one and use it. Run two frameworks in parallel only if your leadership team really is already operating that way.

Attach a [Metric](https://tryhamster.com/docs/hamster-studio/metrics) to each measurable Goal — unit, [Direction](https://tryhamster.com/docs/concepts/direction), target, optional baseline. Log [Results](https://tryhamster.com/docs/hamster-studio/results) per period; status (On Track, At Risk, Off Track) makes "off track" visible without anyone curating a deck.

## Initiatives are the planning surface at this scale

At 10–50 people, raw [Brief](https://tryhamster.com/docs/hamster-studio/briefs) lists get noisy across multiple teams. [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) are how Hamster groups related [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) under an outcome — a quarterly bet, a launch, a discrete strategic project. Each [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) links to one or more Goals (with optional weights), so the work ladders cleanly back to Direction.

We recommend [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) at this scale because:

* PMs talk to your CEO about outcomes, not tickets.
* Cross-team dependencies are easier to express ("this [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) depends on that [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives)") than at the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) level.
* Status roll-ups happen at the right level of detail for execs.

Examples of [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives):

* "Mobile app launch — Q3" → Mobile adoption Goal
* "Self-serve checkout" → Activation Goal
* "Sales-led onboarding for top 100 accounts" → Enterprise revenue Goal

The pattern: PMs write [Briefs](https://tryhamster.com/docs/hamster-studio/briefs); an EM or PM lead groups [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) into [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives); [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) link to Goals; execs see Goal- and Initiative-level roll-ups rather than every Brief. If you have Linear or Jira connected, [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) sync to your existing exec dashboards.

## Shipping change

The [Discovery](https://tryhamster.com/docs/concepts/discovery) → refinement → [Plan](https://tryhamster.com/docs/hamster-studio/plans) → [Delivery](https://tryhamster.com/docs/concepts/delivery) loop is the same as it is for small teams, and it doesn't have to start in a Brief. Spike code, ideate in Figma, run a [Research Agent](https://tryhamster.com/docs/hamster-studio/research-agents) pass, or whiteboard with your team; converge into a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) when the shape is clear. The [Brief](https://tryhamster.com/docs/hamster-studio/briefs) is the artefact that aligns the team and feeds the [Plan](https://tryhamster.com/docs/hamster-studio/plans).

What changes at this scale:

* Run [Delivery](https://tryhamster.com/docs/concepts/delivery) from [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), not terminals. Engineers might still kick off the occasional [CLI](https://tryhamster.com/docs/hamster-studio/cli) [Delivery](https://tryhamster.com/docs/concepts/delivery), but the primary surface is the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) — every [Delivery](https://tryhamster.com/docs/concepts/delivery) is attributed, observable in the [delivery thread](https://tryhamster.com/docs/hamster-studio/cloud-agents), and reviewable by anyone in the org.
* Alignment becomes asynchronous. At small scale, alignment happens in the room. At 30 people it happens in the [activity timeline](https://tryhamster.com/docs/hamster-studio/briefs/activity-timeline) and [Slack alignment unfurls](https://tryhamster.com/docs/hamster-studio/connections/slack). Make sure every [Brief](https://tryhamster.com/docs/hamster-studio/briefs) has a clear set of alignment voters.
* Multiple teams ship in parallel. [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) per repo means deliveries don't queue behind each other.

## Codifying your team's methods

The [Methods Library](https://tryhamster.com/docs/hamster-studio/skills-methods) is your team's AI playbook — the [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) the AI reads from when it builds. The Hamster [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) default is well-tuned for most patterns; at this scale, you'll want to fork it once at the workspace level and add the conventions specific to your team.

We recommend forking the Hamster [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) once at the workspace level rather than per-team. Per-team forks multiply maintenance and the drift compounds across deliveries.

Common additions teams make at this scale:

* Testing patterns — how the team expects unit, integration, and E2E tests for different kinds of change.
* Deploy procedures — pre-merge checks, snapshot environments, manual approval gates.
* Design-system compliance — when a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) touches design-critical surfaces, what checks are required before the PR is reviewed.
* Domain-specific patterns — anything specific to your product that the AI shouldn't have to re-figure-out per brief.

Top tip: Add a "How we test" and "How we deploy" [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) to your Library fork early. These are the conventions AI agents trip over most often when shipping for a team.

## Understanding progress

### Initiative roll-ups, not brief lists

Once you have multiple teams writing [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) list view is too noisy for status. The [Initiatives view](https://tryhamster.com/docs/hamster-studio/initiatives) and the per-initiative timeline are the right surfaces for execs and stakeholders.

### Activity timelines on briefs

Every [Brief](https://tryhamster.com/docs/hamster-studio/briefs) has an [activity timeline](https://tryhamster.com/docs/hamster-studio/briefs/activity-timeline) — every change to the [Brief](https://tryhamster.com/docs/hamster-studio/briefs), every alignment vote, every [Plan](https://tryhamster.com/docs/hamster-studio/plans) revision (including AI-driven revisions), every [Delivery](https://tryhamster.com/docs/concepts/delivery) run. It's the audit log for one piece of work.

### Slack for stakeholders

For non-builder stakeholders (sales, CS, ops, designers who aren't in Hamster every day), the [Slack brief side panel](https://tryhamster.com/docs/hamster-studio/connections/slack) renders the live [Brief](https://tryhamster.com/docs/hamster-studio/briefs) inline. They don't need to log into Hamster to stay in the loop.

## Going deeper

* [Routines](https://tryhamster.com/docs/hamster-studio/routines) — automate "every time X happens, do Y" patterns.
* [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) — expose Hamster's [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph) to Cursor, Claude Code, and other tools your engineers use.
* [Meeting Agent](https://tryhamster.com/docs/hamster-studio/connections/meeting-agent) — auto-capture customer calls into briefs.

When you cross 50 people or start running multiple product orgs, see [How to use Hamster: Enterprise and scaling](https://tryhamster.com/docs/for/enterprise-and-scaling).

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Solutions","item":"https://tryhamster.com/docs/for"},{"@type":"ListItem","position":4,"name":"Startups And Mid Size","item":"https://tryhamster.com/docs/for/startups-and-mid-size"}]}
```
