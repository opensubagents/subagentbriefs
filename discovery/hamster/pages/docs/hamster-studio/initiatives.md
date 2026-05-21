---
description: Initiatives turn goals into work in flight — what we&#x27;re going to do to move an outcome, broken down into briefs that ship.
title: Initiatives | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Initiatives

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

# Initiatives

_[Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) turn goals into work in flight. Each one names the outcome it's going to move, the [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) that will deliver it, and how it's tracking — so the line from a goal to a shipped PR is visible at every altitude._

## Overview

An **[Initiative](https://tryhamster.com/docs/hamster-studio/initiatives)** is your team's commitment to deliver a goal. Goals say _what we want_ with [Metrics](https://tryhamster.com/docs/hamster-studio/metrics), baselines, targets, and per-period [Results](https://tryhamster.com/docs/hamster-studio/results) attached. [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) say _what we're going to do about it_ — concretely enough that [Delivery](https://tryhamster.com/docs/concepts/delivery) can start.

Each [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) carries:

* The goals it delivers — one or more, with their [Metrics](https://tryhamster.com/docs/hamster-studio/metrics) and [Results](https://tryhamster.com/docs/hamster-studio/results) inherited up. An optional weight (0–1) per link captures partial contribution when an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) only partly serves a goal.
* An owner — accountable for whether this commitment lands.
* A description in plain English — what we're going to do, written so humans and AI can both read it.
* State — where the work is in its lifecycle (Planning, Active, Completed, …).
* Health — how the work is tracking right now (On Track, At Risk, Off Track, In Planning), independent of state.
* Optional dates — start and end if the [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) is time-bound.
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) — the deliverable chunks the [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) breaks down into.

[Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) sit at the top of Hamster's [Delivery](https://tryhamster.com/docs/concepts/delivery) layer. Above an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) is the goal it serves (with its [Metric](https://tryhamster.com/docs/hamster-studio/metrics), target, and per-period [Results](https://tryhamster.com/docs/hamster-studio/results)); below it are the [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) the [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) breaks into, and the [Plans](https://tryhamster.com/docs/hamster-studio/plans), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), and PRs they generate.

You manage [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) in three places: the dedicated [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) surface in the sidebar, inline from any [Brief](https://tryhamster.com/docs/hamster-studio/briefs), and from [Hamster Chat](https://tryhamster.com/docs/hamster-studio/chat) in natural language. If you have Linear or Jira connected, your [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) also stay in sync with the matching projects or goals on those platforms.

## How It Works

1. Open the [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) tab — Find [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) in the sidebar. The page opens in tree view, with a card grid available as an alternative layout.
2. Create an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) — Click **New [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives)**. Give it a title and an optional description, pick an icon, and assign an owner. [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) can be created at the top level or as a child of an existing one.
3. Link the goals it delivers — From the [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives), link one or more goals. The [Metrics](https://tryhamster.com/docs/hamster-studio/metrics) and per-period [Results](https://tryhamster.com/docs/hamster-studio/results) on those goals propagate up so you can see at a glance which outcomes this commitment is meant to move. Add a weight (0–1) when the contribution is partial.
4. Build the hierarchy — Drag any [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) onto another to nest it as a child. There is no depth limit, and Hamster prevents drags that would create a cycle. Two levels usually beats five.
5. Break it down into [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) — Use **Add [Brief](https://tryhamster.com/docs/hamster-studio/briefs)** to multi-select existing [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), or create new ones from chat. Each [Brief](https://tryhamster.com/docs/hamster-studio/briefs) is one deliverable chunk of the [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives); together they're how the commitment gets executed.
6. Link sub-initiatives in bulk — Use **Add sub-initiative** the same way to attach existing [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) as children, in a single multi-select pass.
7. Track state and health — Set the **state** (Planning, Active, Completed, …) for lifecycle, and the **health** (On Track, At Risk, Off Track, In Planning) as your weekly pulse. They're independent — an Active [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) can be At Risk; a Planning [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) can be On Track if planning is going well.
8. Filter the list — Use the status filter at the top of the list to scope the view. Your filter, expanded tree state, and visible columns persist per user.
9. Ask in chat — Type "what's the status of growth and adoption?" or "are any active [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) at risk?" in any [Hamster Chat](https://tryhamster.com/docs/hamster-studio/chat) thread. The [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) Manager agent answers inline with rich reference cards.

## Briefs are the deliverable chunks

A [Brief](https://tryhamster.com/docs/hamster-studio/briefs) is the smallest unit of _change that ships_. One [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) breaks down into many [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) over its lifetime; each [Brief](https://tryhamster.com/docs/hamster-studio/briefs) is small enough to refine in chat, align on, and ship as a PR. The [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) says what we're going to ship; [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) are the actual things we ship to do it.

A [Brief](https://tryhamster.com/docs/hamster-studio/briefs) belongs to one [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) at a time. Linking a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) that's already attached to a _different_ [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) moves it; the picker hides [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) already linked to _this_ [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) so you can't accidentally double-link.

## Multi-Select Linking

Linking [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) and sub-initiatives is a multi-select action, not one-at-a-time. Open the link dialog from an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) detail page, tick every [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) you want to attach, and submit once. Hamster fans the request out across all selections at the same time.

The dialog handles the noise for you:

* Already-linked items are hidden — A [Brief](https://tryhamster.com/docs/hamster-studio/briefs) that is already linked to this [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) will not appear in the picker, so you cannot accidentally double-link it. A [Brief](https://tryhamster.com/docs/hamster-studio/briefs) linked to a _different_ [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) still shows up; one [Brief](https://tryhamster.com/docs/hamster-studio/briefs) can only belong to one [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives), so picking it moves it.
* Archived [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) are excluded — The [Brief](https://tryhamster.com/docs/hamster-studio/briefs) picker filters out archived [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) by default to keep the list focused on live work.
* Counter and Clear all — A small counter shows how many items you have selected, with a Clear button to reset.

## Status Filters and Display Preferences

The [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) list supports filtered views without leaving the page:

* State filter — A multi-select dropdown at the top of the list. Pick any combination of states (Planning, Active, Completed, etc.) to scope the visible initiatives.
* Visible properties — Choose which columns to show in the list view (owner, dates, state, health). Hidden columns persist across sessions.
* Tree expand state — Branches you collapse stay collapsed. Branches you expand stay expanded. Hamster remembers your view between sessions.
* Card vs tree — Toggle the layout from the page header. Both views read the same data; pick the one that suits the moment.

All of these preferences are stored per user, so your view is yours alone. Switching workspaces or accounts does not affect them.

## Initiatives in Hamster Chat

Hamster's AI assistant has a dedicated [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) Manager. It is always available in the Getting Started, [Brief](https://tryhamster.com/docs/hamster-studio/briefs), Goal, and [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) chat surfaces — no setup required.

Ask things like:

* _"What [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) are delivering the Activation goal?"_
* _"What's the health of our active [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) right now?"_
* _"Create a new [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) called Q3 Onboarding Polish under the Refine workstream, linked to the Activation goal."_
* _"Move HAM-1234 from Onboarding to Activation."_
* _"Suggest an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) to move our North Star metric."_

The agent resolves names — you do not need to copy IDs around. When it cites an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives), the link renders as a rich inline card with the title, description, status badge, and [Brief](https://tryhamster.com/docs/hamster-studio/briefs) count. Click the card to open the [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) directly.

If a chat thread is scoped to a specific [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) (because you opened the chat from an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) page), the agent picks that up as context automatically.

## Two-Way Sync with Linear and Jira

If your workspace has Linear or Jira connected with two-way sync enabled, [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) stay in sync with the matching projects (Linear) or goals (Jira):

* Creating an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) creates the matching project or goal on the other side.
* Renaming, restating, or restoring an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) pushes the same change across.
* Hamster preserves any links that exist only in Hamster — so syncing with Linear will not strip out [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) you only track here.
* Sync badges appear on [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) and [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) so you can tell at a glance which ones are mirrored externally.

Hamster's hierarchy is deeper than Linear's, so deeply nested [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) map to a Linear project plus a label fallback. Jira goals map onto [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) one-to-one.

## Tips

* **Lead with the goal.** Every [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) should link to at least one goal. An [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) without linked goals is unanchored work; create the goal first, then commit the [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) to it.
* **Use weights when the contribution is partial.** If an Onboarding Polish [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) serves Activation 70% and Retention 30%, set the weights — it's how the [Metric](https://tryhamster.com/docs/hamster-studio/metrics) ladder stays honest.
* **Start with two levels and add depth only when you actually need it.** A flat list of ten [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) is easier to track than a five-deep tree.
* **Use state for lifecycle, health for pulse.** They tell different stories. State says where it _is_; health says how it's _going_.
* **The chat surface is the fastest way to triage.** "What's at risk and which goals does it threaten?" answers in one prompt.
* **Owners show up in the list view, so set one early.** [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) without an owner tend to drift.
* **Linking [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) in bulk on the way in is much faster than fixing the hierarchy retroactively.**
* The [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) tree is realtime — when a teammate moves an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) or links a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), you see it without a refresh.

## Related

* [Goals](https://tryhamster.com/docs/hamster-studio/goals) — the outcomes [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) deliver, with [Metrics](https://tryhamster.com/docs/hamster-studio/metrics) and [Results](https://tryhamster.com/docs/hamster-studio/results) attached
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) — the deliverable chunks an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) breaks down into
* [Plans](https://tryhamster.com/docs/hamster-studio/plans) — what each [Brief](https://tryhamster.com/docs/hamster-studio/briefs) generates for [Delivery](https://tryhamster.com/docs/concepts/delivery)
* [Linear Connection](https://tryhamster.com/docs/hamster-studio/connections/linear)
* [Hamster Chat](https://tryhamster.com/docs/hamster-studio/chat)
* [Roles and Permissions](https://tryhamster.com/docs/hamster-studio/teams/roles-permissions)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Initiatives","item":"https://tryhamster.com/docs/hamster-studio/initiatives"}]}
```
