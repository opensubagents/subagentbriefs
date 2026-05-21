---
description: Roll Hamster out across 50+ people, multiple teams, and multiple repos. Workspace topology, audit, methods governance, and bridging your engineering platform.
title: How to use Hamster: Enterprise and scaling | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Enterprise & scaling

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

# How to use Hamster: Enterprise and scaling

A guide for admins setting up Hamster at a 50+ person product org. Multiple teams, multiple repos, often multiple business units. Existing engineering platform in place. Engineers already deeply embedded with Cursor, Claude Code, or other coding agents. Covers workspace topology decisions, integrating with your existing platform, setting [Direction](https://tryhamster.com/docs/concepts/direction) across the org, governing [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) at scale, and the audit and attribution model.

> Under 50 people? [How to use Hamster: Startups and mid-size companies](https://tryhamster.com/docs/for/startups-and-mid-size) is the right starting point. Want to try Hamster on a single [Brief](https://tryhamster.com/docs/hamster-studio/briefs) first without the setup? See [Just ship](https://tryhamster.com/docs/concepts#what-this-means-in-practice).

Running Hamster at scale

\~4 minutes

Video coming soon

## Setting up your workspace

### Workspace topology

At scale, the first decision is workspace boundary. Hamster doesn't currently support cross-workspace nesting, so pick the boundary that matches how your [Delivery](https://tryhamster.com/docs/concepts/delivery) org actually runs.

The three common patterns:

* One workspace, many teams. Works well up to \~150 people on a single product. [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives), [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods), and [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) all live in one place. This is the default and the one we recommend unless something forces you off it.
* One workspace per product line. When product lines have separate codebases, separate roadmaps, and minimal shared review. [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) don't move between product lines.
* One workspace per business unit. When business units are operationally independent — separate finance, separate go-to-market, separate engineering leadership.

You can move [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) between workspaces if you pick wrong, but it's not zero-cost. We recommend talking to us before locking topology — see [Get in touch](#procurement-security-and-sso) at the bottom of this page.

### Connect your Context Graph at the org level

At this scale, configure [Connections](https://tryhamster.com/docs/hamster-studio/connections) at the organisation level rather than per-team where possible. Your [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph) is what makes [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), and [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) work — and at scale, you want the graph reading consistently across your whole org, not stitched together per team.

* [GitHub](https://tryhamster.com/docs/hamster-studio/connections/github) at the GitHub-org level. Hamster respects per-repo permissions; the org-level [Connection](https://tryhamster.com/docs/hamster-studio/connections) just removes per-repo install friction. PRs are attributed to the engineer who triggered the delivery.
* [Linear](https://tryhamster.com/docs/hamster-studio/connections/linear) or Jira mapped [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) → epics. Decide team-by-team whether brief-level state lives in Hamster or in your existing tracker.
* [Slack](https://tryhamster.com/docs/hamster-studio/connections/slack) in your primary workspace. The [Brief](https://tryhamster.com/docs/hamster-studio/briefs) side panel and slash commands work consistently across teams.
* [Meeting Agent](https://tryhamster.com/docs/hamster-studio/connections/meeting-agent) — at this scale, common pattern is enabling for product, sales, and CS teams; transcripts auto-link to relevant briefs.
* [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) — expose Hamster context to Cursor, Claude Code, Codex, and your own internal tools at the org level. This is how individual engineers get the same [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph) reach inside their existing IDE.

See [Connections overview](https://tryhamster.com/docs/hamster-studio/connections/overview) for the full list.

### IDE flow for engineers (the path most engineers use)

At your scale, your engineers are deeply embedded with Claude Code, Cursor, Codex, or other coding agents. The [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) plus the Hamster [CLI](https://tryhamster.com/docs/hamster-studio/cli) give them your [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph), [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), and [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) inside their existing tool. Engineers ship from their IDE, with your team's accumulated context already loaded.

Two pieces every engineer installs:

* The [Hamster CLI](https://tryhamster.com/docs/hamster-studio/cli) — auth, skills sync, slash commands, scoped context.
* The [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) — exposes Hamster context to Claude Code, Cursor, Codex, and your own internal tools at the org level.

We strongly recommend making MCP setup a step in your engineering onboarding. The IDE flow is what most of your engineers will use day-to-day, and it scales without forcing engineers into a new surface they didn't ask for.

### Cloud Agents at scale (for non-engineer-driven deliveries)

A [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) is the configured environment Hamster runs deliveries in when nobody's hands are on a keyboard. At scale, configure one [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) per active repo per environment.

[Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) complement the IDE flow rather than replacing it. They're how PMs kick off deliveries from [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) without an engineer in the loop, how [Routines](https://tryhamster.com/docs/hamster-studio/routines) run automated deliveries, and how parallel deliveries run across the team without queuing on engineer time.

Common patterns:

* Per-team [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) for team-specific repos (e.g. `mobile-ios`, `mobile-android` each get their own).
* Shared [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) for monorepo or platform repos that multiple teams ship into.
* Production-restricted [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) that only senior engineers can trigger deliveries from.

[Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) respect Hamster's permission model. Only Creators can configure [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents); Reviewers can read configurations but not trigger deliveries. For sensitive environments, use the Admin role to gate configuration changes. See [Roles & permissions](https://tryhamster.com/docs/hamster-studio/teams/roles-permissions) for the full model.

## Building blueprints across the org

At this scale, you typically have many product surfaces. Each one deserves its own [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) — generated from your [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph), edited by the team that owns the surface, and used as the source of truth every [Brief](https://tryhamster.com/docs/hamster-studio/briefs) on that surface gets refined against.

Treat [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) as part of your platform documentation. Owners, review cadence, change control, the works. The benefit at scale is that [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) are connected to your real systems through your [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph), not lying in a wiki — they update in both directions as code changes and as new docs are authored.

For organisations with central architecture, security, or platform teams: have those teams own the cross-cutting [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) (security posture, infrastructure topology, compliance policies). Each product team's [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) inherits from the cross-cutting ones rather than restating them.

## Direction at scale

At enterprise scale, [Direction](https://tryhamster.com/docs/concepts/direction) usually runs at multiple altitudes — a company-level framework that boards and execs read against, plus team-level frameworks that product groups operate against quarter to quarter.

Common patterns:

* Company-level OGSM or North Star at the workspace root, owned by leadership.
* Team-level OKRs per product team, linked up to the company-level Goals.
* Cross-cutting Goals (security posture, infrastructure SLOs, compliance) owned by central teams and surfaced as Goals on the workspace.

Each [Goal](https://tryhamster.com/docs/hamster-studio/goals) takes a [Metric](https://tryhamster.com/docs/hamster-studio/metrics) and [Results](https://tryhamster.com/docs/hamster-studio/results) per period. [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) link many-to-many to Goals (with optional weights), so a "Mobile launch" [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) can roll up to both "Q3 launches" and "Mobile platform investment" Goals without forking work. Frameworks are versioned and switching them doesn't disturb the [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives), [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Plans](https://tryhamster.com/docs/hamster-studio/plans), or [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) below.

## Methods governance

The [Methods Library](https://tryhamster.com/docs/hamster-studio/skills-methods) is your team's AI playbook — the [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) the AI reads from when it builds. At scale this is load-bearing: drift in your library means drift in every [Delivery](https://tryhamster.com/docs/concepts/delivery), multiplied by your team count.

We recommend:

1. Start with the Hamster [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) default.
2. Fork it once, at the workspace level, to add your engineering conventions (preferred testing patterns, code-style enforcement, deploy procedures, security review gates).
3. Avoid per-team forks unless absolutely necessary. They multiply maintenance and the drift compounds across teams.

A platform team typically owns the workspace-level [Methods Library](https://tryhamster.com/docs/hamster-studio/skills-methods) fork at this scale, in the same way an internal-tooling team would own a CI configuration or a build system. Product teams contribute [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) up to the central fork rather than maintaining their own.

Top tip: Add an "Internal compliance and review gates" [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) to your Library fork early. This is where security review requirements, audit logging, and PII-handling rules live; AI agents need them in the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) context, not pasted in by an engineer at [Delivery](https://tryhamster.com/docs/concepts/delivery) time.

## Bridging your existing engineering platform

Hamster doesn't replace your engineering platform. It sits on the spec layer above it.

| Surface                                                                       | Hamster         | Your platform                        |
| ----------------------------------------------------------------------------- | --------------- | ------------------------------------ |
| [Brief](https://tryhamster.com/docs/hamster-studio/briefs) / spec             | Hamster         | —                                    |
| [Plan](https://tryhamster.com/docs/hamster-studio/plans)                      | Hamster         | (synced)                             |
| [Tasks](https://tryhamster.com/docs/hamster-studio/tasks)                     | (synced)        | Linear / Jira                        |
| Code review                                                                   | —               | GitHub                               |
| CI/CD                                                                         | —               | GitHub Actions / Buildkite / Jenkins |
| [Delivery](https://tryhamster.com/docs/concepts/delivery) agent observability | Hamster         | —                                    |
| Production observability                                                      | —               | Datadog / Sentry / your stack        |
| Customer signal                                                               | Hamster + Slack | Gong / Zendesk / your stack          |

The pattern: keep your existing platform; let Hamster own the goals, [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives), [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), and [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods), plus AI delivery. The [Connections](https://tryhamster.com/docs/hamster-studio/connections) do the gluing. Most rollouts at this scale don't change anything in the existing platform — they add Hamster to it.

## Shipping change at scale

The loop — [Discovery](https://tryhamster.com/docs/concepts/discovery), refine, align, deliver — doesn't change at scale. What changes is the surface area each loop touches. [Discovery](https://tryhamster.com/docs/concepts/discovery) at this scale still doesn't have to start in a [Brief](https://tryhamster.com/docs/hamster-studio/briefs): spike code in a feature branch, ideate in Figma, run a [Research Agent](https://tryhamster.com/docs/hamster-studio/research-agents) pass, hold an architecture review. Converge into a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) when the shape is clear and alignment voters are ready.

### Initiatives are mandatory

[Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) become the primary planning surface. Brief-level visibility doesn't scale past \~5 teams; Initiative-level does. Each [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) links to one or more [Goals](https://tryhamster.com/docs/hamster-studio/goals), so company- and team-level [Direction](https://tryhamster.com/docs/concepts/direction) stays connected to the work in flight.

The pattern at scale:

* Each team groups its [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) into Initiatives.
* [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) link to Goals (many-to-many, optional weights) so outcome roll-ups stay accurate.
* [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) sync to Linear or Jira so existing exec dashboards still work without parallel reporting.
* Cross-team dependencies are expressed via Initiative-to-Initiative links.
* Multi-select linking lets [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) belong to multiple parents (a "Mobile launch" [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) might roll up to both "Q3 launches" and "Mobile platform investment").

### Alignment becomes asynchronous

At small scale, alignment happens in the room. At scale, it happens in the [activity timeline](https://tryhamster.com/docs/hamster-studio/briefs/activity-timeline) and [Slack alignment unfurls](https://tryhamster.com/docs/hamster-studio/connections/slack). Make sure every [Brief](https://tryhamster.com/docs/hamster-studio/briefs) has a clear set of required alignment voters before it moves to [Delivery](https://tryhamster.com/docs/concepts/delivery); the brief-status flow gates this.

### Routines for repeating work

[Routines](https://tryhamster.com/docs/hamster-studio/routines) automate "every time X happens, do Y" patterns. At scale, common [Routines](https://tryhamster.com/docs/hamster-studio/routines) include:

* Post-delivery summary posted to a Slack channel for non-builders.
* Scope-change alert when a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) grows past a threshold during alignment.
* Plan-review reminder for [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) that have been in alignment for more than three days.
* Audit-trail mirror that mirrors Brief-level events to your internal audit log.

## Audit, attribution, and observability

At scale, who triggered what and when matters. Hamster provides:

* PR attribution via the [GitHub connection](https://tryhamster.com/docs/hamster-studio/connections/github). Every [Delivery](https://tryhamster.com/docs/concepts/delivery) PR is attributed to the engineer who triggered it, not to a generic "Hamster bot".
* Brief-level audit in the [activity timeline](https://tryhamster.com/docs/hamster-studio/briefs/activity-timeline). Every [Brief](https://tryhamster.com/docs/hamster-studio/briefs) edit, alignment vote, [Plan](https://tryhamster.com/docs/hamster-studio/plans) revision, and [Delivery](https://tryhamster.com/docs/concepts/delivery) run is recorded.
* Per-delivery observability in the [delivery thread](https://tryhamster.com/docs/hamster-studio/cloud-agents). Every tool call, every flow step, every PR push is logged.
* Per-account isolation. [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Plans](https://tryhamster.com/docs/hamster-studio/plans), and deliveries are scoped to the workspace. Cross-workspace access is not possible without explicit invitation.

If your security or compliance team needs more (audit log exports, retention policies, SOC 2 attestation), see below.

## Procurement, security, and SSO

Hamster supports SSO via the major IdPs (Okta, Google Workspace, Microsoft Entra) on the Business [Plan](https://tryhamster.com/docs/hamster-studio/plans) and above. SOC 2 Type II attestation is available; reach out for the report.

For procurement processes, custom DPAs, security questionnaires, or VPC-isolated deployments: email [hello@tryhamster.com](mailto:hello@tryhamster.com) before procurement starts. We'll work it through case-by-case.

## Going deeper

* [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) — expose Hamster's context to Cursor, Claude Code, Codex, and your internal tools at the org level.
* [CLI](https://tryhamster.com/docs/hamster-studio/cli) — scripted deliveries in CI, skill sync, slash commands.
* [Routines](https://tryhamster.com/docs/hamster-studio/routines) — automation patterns for repeated org-wide work.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Solutions","item":"https://tryhamster.com/docs/for"},{"@type":"ListItem","position":4,"name":"Enterprise And Scaling","item":"https://tryhamster.com/docs/for/enterprise-and-scaling"}]}
```
