---
description: Configured cloud sandboxes that ship Briefs and Tasks for your Team — set up once, deliver in parallel without anyone&#x27;s laptop in the loop.
title: Cloud Agents | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Cloud Agents

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

# Cloud Agents

_Configure one [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents), point it at a repo, paste your `.env`, hit Save. A minute later it shows "Active" — and from then on any teammate can deliver a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or [Task](https://tryhamster.com/docs/hamster-studio/tasks) from the cloud, in parallel, without anyone's laptop in the loop._

## Overview

A [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) is a configured cloud sandbox plus the AI agent that runs inside it. The sandbox knows your repo URL, your env vars, and your build and test commands. The AI agent knows the [Brief](https://tryhamster.com/docs/hamster-studio/briefs), the relevant [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), and the [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods). When a teammate clicks **Deliver** on a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), launches from a [Task](https://tryhamster.com/docs/hamster-studio/tasks), triggers a [Routine](https://tryhamster.com/docs/hamster-studio/routines), or uses `/ship` from Slack, the [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) boots, the AI executes the work, and a pull request lands in your repository.

[Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) complement the IDE flow rather than replacing it. Most engineers ship from their IDE using [CLI](https://tryhamster.com/docs/hamster-studio/cli) and [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) — they want control. [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) are the path for deliveries that don't need an engineer at the keyboard: a PM clicking **Deliver** on a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), [Routines](https://tryhamster.com/docs/hamster-studio/routines) running scheduled work, parallel deliveries across the [Team](https://tryhamster.com/docs/hamster-studio/teams), or Slack slash flows that should not queue on engineer time.

## How it works

1. Configure once. Open **Settings > [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents)** and create a new Cloud Agent. Name it, attach one or more GitHub repositories, paste your `.env`, set the install/build/test/run commands per repo. Save.
2. Hamster builds and snapshots automatically. Status moves through **Pending → In progress → Active**. Once Active, the sandbox snapshot is ready and any [Brief](https://tryhamster.com/docs/hamster-studio/briefs) on a connected repo can deliver into this [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents).
3. Deliver from a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), [Task](https://tryhamster.com/docs/hamster-studio/tasks), [Routine](https://tryhamster.com/docs/hamster-studio/routines), or Slack. Click **Deliver** on a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), hand a [Task](https://tryhamster.com/docs/hamster-studio/tasks) to the [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) from the [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page, let a [Routine](https://tryhamster.com/docs/hamster-studio/routines) trigger [Delivery](https://tryhamster.com/docs/concepts/delivery), or use the Slack slash flow for a specific [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents).
4. Watch the [Delivery](https://tryhamster.com/docs/concepts/delivery) thread. The agent's narrative streams live in the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or [Task](https://tryhamster.com/docs/hamster-studio/tasks) thread — every tool call, every flow step, the PR push. You can interrupt it at any time by typing into the thread.

## Status

Each [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) shows a status pill that mirrors the sandbox lifecycle:

* Pending — Configuration saved, sandbox build hasn't started yet.
* In progress — Building, restarting, or stopping.
* Active — Sandbox snapshot is ready. [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) and [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) can deliver into this Agent.
* Needs action — The build hit an error. Open the Agent to see what happened and try again.

The list updates live, so you can save a config and watch the pill change without refreshing.

## Env vars

Env vars are encrypted at rest and never exposed in the UI after they're saved. You can paste:

* A full `.env` blob — comments, blank lines, and `export` prefixes are tolerated.
* Individual key/value pairs — single and double quotes are stripped.
* Multiple paste operations — last-write-wins per key, so re-pasting an updated `.env` overrides the prior value cleanly.

Vars are scoped to the [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) and made available to the sandbox at [Delivery](https://tryhamster.com/docs/concepts/delivery) time.

## Multiple Cloud Agents

You can run as many [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) as your team needs. Common patterns:

* **One Agent per repo** for single-repo teams.
* **One Agent per app inside a monorepo**, each with the right command set baked in.
* **Separate Agents for staging vs. production** deploys, with different env vars on each.

Two [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) targeting different Agents deliver in parallel without contention. Two [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) targeting the same Agent each get their own sandbox, also in parallel, booted from the shared snapshot.

## What the agent receives

When a [Delivery](https://tryhamster.com/docs/concepts/delivery) launches, the AI agent inside the [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) receives:

* The [Brief](https://tryhamster.com/docs/hamster-studio/briefs) — title, description, scope, acceptance criteria, attached context (Figma frames, customer-call clips, screenshots, URLs).
* Relevant [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) from your [Team](https://tryhamster.com/docs/hamster-studio/teams)'s [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph) — what the product is today, what the relevant systems are.
* [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) from your [Team](https://tryhamster.com/docs/hamster-studio/teams)'s [Methods Library](https://tryhamster.com/docs/hamster-studio/skills-methods/methods-library) — how your [Team](https://tryhamster.com/docs/hamster-studio/teams) works, testing patterns, deploy procedures.
* The repository, branch, and any additional instructions you provide at launch time.

The agent uses all of this to understand not just what to build, but why and how — which leads to more contextually appropriate implementation than a generic AI coding tool would produce in isolation.

## Run states

Each [Delivery](https://tryhamster.com/docs/concepts/delivery) moves through a set of states Hamster tracks and displays:

* Pending — The run has been created and the agent is starting up.
* Running — The agent is actively working in the sandbox.
* Completed — The agent finished and opened a pull request.
* Failed — The agent encountered an error. The run record includes details.
* Cancelled — The run was cancelled before completion.

Only one [Delivery](https://tryhamster.com/docs/concepts/delivery) can be active for a given [Brief](https://tryhamster.com/docs/hamster-studio/briefs) at a time. If you try to launch a second run while one is in progress, you'll wait for it to finish or cancel it first.

## Reset

If a [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) stops booting cleanly — bad commit, broken dependency, stale snapshot — open the Agent's overflow menu and click **Reset**. Hamster clears the live sandbox handles, flips the Agent back to Pending, and re-runs the build. When it lands on Active again, it has a fresh snapshot.

Reset is the right move when:

* A [Delivery](https://tryhamster.com/docs/concepts/delivery) has failed repeatedly and you suspect the snapshot is stale.
* You've changed env vars or commands and want a clean rebuild.
* You've upgraded the underlying repo's toolchain and want the Agent to pick it up.

## Permissions

Workspace **Admins** and **Creators** can configure [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) — create, edit, reset, and delete. Other roles can deliver [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) into any Active [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) but cannot change the configuration. For sensitive environments (e.g. production deploys), use the Admin role to gate configuration changes.

## Cloud Agents vs the IDE flow

[Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) and the [IDE flow](https://tryhamster.com/docs/hamster-studio/cli) ([CLI](https://tryhamster.com/docs/hamster-studio/cli) \+ [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp)) are two paths to the same destination — a PR in your repo from a [Brief](https://tryhamster.com/docs/hamster-studio/briefs). Use whichever fits the situation:

* IDE flow — engineers stay in Claude Code, Cursor, or Codex. They keep control. Best for engineer-driven work where someone wants to be in the loop on the agent's choices in real time.
* [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) — deliver without an engineer at the keyboard. Best for PM-driven deliveries, [Routines](https://tryhamster.com/docs/hamster-studio/routines), parallel work across the [Team](https://tryhamster.com/docs/hamster-studio/teams), or anything kicked off from Slack via slash commands.

Most teams use both. The CLI/MCP path for individual engineers; [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) for everything else.

## Tips

* Keep your `.env` source of truth somewhere stable (1Password, a secrets manager). Re-paste into the [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) any time the source changes; the parser handles re-paste cleanly.
* Use a descriptive Agent name that includes the repo or app — "API", "Web app", "Marketing site" — so teammates know which Agent to pick when delivering.
* If you have multiple repos that share a build pipeline, attach them all to one Agent. [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) that touch any of them can use the same snapshot.
* [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) and the [Slack bot](https://tryhamster.com/docs/hamster-studio/connections/slack) work together: each Agent gets its own slash command flow, so a teammate can deliver a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) into a specific Agent directly from a Slack channel.
* Write clear, specific [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) and [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) before launching. The more precisely the acceptance criteria are written, the better the agent's output will be.
* Check the pull request carefully before merging. [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) are capable, but code review remains important — especially for changes with security implications or complex integration points.
* If a run fails, check the run details for an error description. Common causes include repository access issues or ambiguous instructions the agent couldn't resolve.

## Related

* [Hamster CLI](https://tryhamster.com/docs/hamster-studio/cli) — the IDE/terminal path, for engineers who want control.
* [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) — exposes Hamster context to Claude Code, Cursor, and Codex.
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) — the artefact a [Delivery](https://tryhamster.com/docs/concepts/delivery) ships.
* [Routines](https://tryhamster.com/docs/hamster-studio/routines) — automated, event-driven deliveries.
* [GitHub](https://tryhamster.com/docs/hamster-studio/connections/github) — required for [Delivery](https://tryhamster.com/docs/concepts/delivery) PRs.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Cloud Agents","item":"https://tryhamster.com/docs/hamster-studio/cloud-agents"}]}
```
