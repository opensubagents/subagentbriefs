---
description: Everything in the Plan tab — how tasks are structured, how to read and organize them, and how to hand the plan off for delivery.
title: Understanding Plans | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Understanding Plans

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
   * [Generating Plans](https://tryhamster.com/docs/hamster-studio/plans/generating-plans "Generating Plans")  
   * [Guided Research](https://tryhamster.com/docs/hamster-studio/plans/guided-research "Guided Research")  
   * [Understanding Plans](https://tryhamster.com/docs/hamster-studio/plans/understanding-plans "Understanding Plans")

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

# Understanding Plans

Everything in the [Plan](https://tryhamster.com/docs/hamster-studio/plans) tab — how [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are structured, how to read and organize them, and how to hand the [Plan](https://tryhamster.com/docs/hamster-studio/plans) off for delivery.

## Overview

A [Plan](https://tryhamster.com/docs/hamster-studio/plans) is a two-level hierarchy of [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) attached to a brief. The top level contains parent [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) that represent the major areas of work. Each parent [Task](https://tryhamster.com/docs/hamster-studio/tasks) contains subtasks — the individual units of work with detailed descriptions and acceptance criteria. [Plans](https://tryhamster.com/docs/hamster-studio/plans) are designed to be reviewed, adjusted, and then delivered to your team or AI agent via the Hamster CLI.

![Plan tab showing a two-level task hierarchy with parent tasks and subtasks](https://tryhamster.com/_site/images/features/plans/understanding-plans/plan-detail-view-desktop-light.webp?v=6)![Plan tab showing a two-level task hierarchy with parent tasks and subtasks](https://tryhamster.com/_site/images/features/plans/understanding-plans/plan-detail-view-desktop-dark.webp?v=6) 

## Task Hierarchy

**Parent [Tasks](https://tryhamster.com/docs/hamster-studio/tasks)** represent distinct areas of work within the scope of the brief. Each parent [Task](https://tryhamster.com/docs/hamster-studio/tasks) has a title, description, and a set of subtasks. Parent [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are created first during [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation and appear in the [Plan](https://tryhamster.com/docs/hamster-studio/plans) view as soon as they are ready.

**Subtasks** are the detailed steps inside each parent task. Each subtask is generated with:

* A title and description scoped tightly to the parent [Task](https://tryhamster.com/docs/hamster-studio/tasks)
* Acceptance criteria that define when the work is complete
* A complexity score that indicates how much effort the [Task](https://tryhamster.com/docs/hamster-studio/tasks) requires

Subtasks are elaborated in parallel — each parent [Task](https://tryhamster.com/docs/hamster-studio/tasks) is expanded at the same time. They appear progressively as each elaboration thread finishes.

## Reading the Plan

### Task status

Every [Task](https://tryhamster.com/docs/hamster-studio/tasks) and subtask can be in one of three states:

* Todo — Work has not started
* In Progress — Work is underway
* Done — Work is complete

You can move [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) between states from the [Plan](https://tryhamster.com/docs/hamster-studio/plans) view. When grouped by status, the [Task](https://tryhamster.com/docs/hamster-studio/tasks) list is organized into sections by state so you can see what is in progress at a glance.

### Complexity badge

[Tasks](https://tryhamster.com/docs/hamster-studio/tasks) show a complexity badge based on the AI's assessment during generation. The badge gives a rough indication of effort — useful for spotting which [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are likely to take the most time and for planning assignments.

### Next best task

One [Task](https://tryhamster.com/docs/hamster-studio/tasks) in the [Plan](https://tryhamster.com/docs/hamster-studio/plans) is marked as the next best [Task](https://tryhamster.com/docs/hamster-studio/tasks) to work on. This is the highest-priority in-progress [Task](https://tryhamster.com/docs/hamster-studio/tasks) if one exists, otherwise the first to-do task. It is marked with a small indicator in the [Task](https://tryhamster.com/docs/hamster-studio/tasks) row to help you and your team quickly orient when picking up work.

### Task detail view

Clicking a [Task](https://tryhamster.com/docs/hamster-studio/tasks) opens the full detail view. Here you can read the complete [Task](https://tryhamster.com/docs/hamster-studio/tasks) description and acceptance criteria, see all subtasks, and interact with the [Task](https://tryhamster.com/docs/hamster-studio/tasks)'s AI conversation thread for deeper context on what was generated and why.

## View Options

The Display button in the top-right corner of the [Plan](https://tryhamster.com/docs/hamster-studio/plans) tab gives you control over how [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are shown.

**View mode**:

* List — A vertical list of tasks. Parent [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) show an expand/collapse control to show or hide their subtasks inline.
* Kanban — A board view with columns for Todo, In Progress, and Done. Parent [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) appear as cards you can drag between columns.

**Group by**:

* None — [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are shown in a single flat list ordered by position
* Status — [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are grouped into sections by their current state

## Organizing Tasks

You can reorder parent [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) by dragging them within the list view. The order you set is preserved and reflected when the [Plan](https://tryhamster.com/docs/hamster-studio/plans) is delivered to the Hamster CLI. Moving a [Task](https://tryhamster.com/docs/hamster-studio/tasks) to a different status group (when grouped by status) updates its status automatically.

## Refining the Plan with Chat

The [Plan](https://tryhamster.com/docs/hamster-studio/plans) view includes an AI chat panel scoped to your plan. Use it to make targeted adjustments after generation without regenerating from scratch:

* Ask the AI to split a parent [Task](https://tryhamster.com/docs/hamster-studio/tasks) that covers too much ground
* Request a missing subtask for a concern the [Plan](https://tryhamster.com/docs/hamster-studio/plans) overlooked
* Ask it to rewrite acceptance criteria for a specific [Task](https://tryhamster.com/docs/hamster-studio/tasks)
* Request a scope change to a [Task](https://tryhamster.com/docs/hamster-studio/tasks) description

The AI reads the current [Plan](https://tryhamster.com/docs/hamster-studio/plans) state — all existing [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) and their content — before making any changes. It updates [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) directly rather than producing suggestions for you to apply manually.

## Expanding Tasks with AI

If a parent [Task](https://tryhamster.com/docs/hamster-studio/tasks) does not have subtasks, or you want to generate additional subtasks after the initial [Plan](https://tryhamster.com/docs/hamster-studio/plans), you can expand it using the sparkle icon that appears when you hover the [Task](https://tryhamster.com/docs/hamster-studio/tasks) title. The AI elaborates the [Task](https://tryhamster.com/docs/hamster-studio/tasks) into subtasks using the same context from the [Brief](https://tryhamster.com/docs/hamster-studio/briefs), the parent [Task](https://tryhamster.com/docs/hamster-studio/tasks) description, and the sibling [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) to avoid overlap.

## Assigning Tasks

You can assign any [Task](https://tryhamster.com/docs/hamster-studio/tasks) or subtask to a team member using the assignee control in the [Task](https://tryhamster.com/docs/hamster-studio/tasks) row. If your workspace has background AI agents configured, you can also assign [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) directly to an agent.

## Delivering the Plan

There are two ways to deliver a [Plan](https://tryhamster.com/docs/hamster-studio/plans) once you're happy with it.

### Deliver with Cloud Agents

Click **Deliver** in the [Plan](https://tryhamster.com/docs/hamster-studio/plans) tab header, and Hamster runs an AI agent through your [Plan](https://tryhamster.com/docs/hamster-studio/plans) in a [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents), then opens a pull request on GitHub. Your machine doesn't need to be running — just click and come back to a PR.

The button shows a spinner and stays disabled while a run is active. The state persists across page refreshes and browser tabs so you always know whether a [Delivery](https://tryhamster.com/docs/concepts/delivery) is in progress.

See [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) for the full guide.

### Open in CLI

For hands-on [Delivery](https://tryhamster.com/docs/concepts/delivery) — working task-by-task, pausing between steps, or handing off to your own agent setup — use the Hamster CLI. The **Open in [CLI](https://tryhamster.com/docs/hamster-studio/cli)** button in the top-right of the [Plan](https://tryhamster.com/docs/hamster-studio/plans) tab gives you a one-line command to run in your terminal. This command:

1. Installs the Hamster [CLI](https://tryhamster.com/docs/hamster-studio/cli) if it is not already present
2. Authenticates your account automatically
3. Sets the [CLI](https://tryhamster.com/docs/hamster-studio/cli) context to the current [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and lists your [Tasks](https://tryhamster.com/docs/hamster-studio/tasks)

From there, you can use [CLI](https://tryhamster.com/docs/hamster-studio/cli) commands to work through the [Plan](https://tryhamster.com/docs/hamster-studio/plans) [Task](https://tryhamster.com/docs/hamster-studio/tasks) by [Task](https://tryhamster.com/docs/hamster-studio/tasks), track progress, and hand off individual [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) to AI coding agents.

Common commands once set up:

```
hamster list                              # View all tasks in the plan
hamster next                              # Get the next task to work on
hamster show [id]                         # View full details for a task
hamster set-status --id=[id] --status=done  # Mark a task complete

```

The command shown in the panel is single-use and time-limited. A fresh command is generated each time you open the panel.

## Tips

* Review the parent [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) first before drilling into subtasks. If a parent [Task](https://tryhamster.com/docs/hamster-studio/tasks)'s scope seems off, edit the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) to clarify the intent and regenerate rather than manually reworking many subtasks.
* Use the list view grouped by status when running a standup or checking team progress — it gives a clear picture of what is moving and what is blocked.
* The kanban view works well for individual workflow management. Dragging cards between columns updates [Task](https://tryhamster.com/docs/hamster-studio/tasks) status in real time.
* Complexity scores are relative within a [Plan](https://tryhamster.com/docs/hamster-studio/plans), not absolute estimates. Use them to identify [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) that may need to be broken down further or assigned to more experienced team members.

## Related

* [Generating Plans](https://tryhamster.com/docs/hamster-studio/plans/generating-plans)
* [Guided Research](https://tryhamster.com/docs/hamster-studio/plans/guided-research)
* [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents)
* [Task Overview](https://tryhamster.com/docs/hamster-studio/tasks/task-overview)
* [CLI Authentication](https://tryhamster.com/docs/hamster-studio/cli/cli-authentication)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Plans","item":"https://tryhamster.com/docs/hamster-studio/plans"},{"@type":"ListItem","position":5,"name":"Understanding Plans","item":"https://tryhamster.com/docs/hamster-studio/plans/understanding-plans"}]}
```
