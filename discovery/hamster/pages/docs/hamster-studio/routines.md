---
description: Write instructions once, attach them to workspace events, and Hamster runs them automatically. Automate recurring AI tasks for your team.
title: Routines | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Routines

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

# Routines

Write an instruction once, and Hamster runs it automatically whenever the right thing happens in your workspace.

## The job routines do

Every product team has work that should happen every single time — summarise a new [Brief](https://tryhamster.com/docs/hamster-studio/briefs) so the team has shared context, check a completed [Task](https://tryhamster.com/docs/hamster-studio/tasks) against the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s acceptance criteria, flag when a [Plan](https://tryhamster.com/docs/hamster-studio/plans) changes scope. Without automation, this relies on someone remembering to do it. Sometimes they do. Often they don't.

[Routines](https://tryhamster.com/docs/hamster-studio/routines) take those recurring jobs off your team's plate. You write the instruction once, attach it to the events that should trigger it, and it runs without anyone thinking about it.

A [Routine](https://tryhamster.com/docs/hamster-studio/routines) has two parts:

* Instructions — what you want Hamster to do, written in plain English or markdown
* Triggers — the workspace events that cause it to run

When a trigger fires, Hamster reads your instructions, gathers the full context of the triggering event, and executes. The output lands in the run history, and any changes it makes to [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), or documents appear in the normal activity feed.

## Creating a routine

Open **[Routines](https://tryhamster.com/docs/hamster-studio/routines)** from the workspace sidebar and select **New [Routine](https://tryhamster.com/docs/hamster-studio/routines)**.

The editor has three tabs:

* Instructions — write what Hamster should do. Be specific. Reference the thing that triggered the [Routine](https://tryhamster.com/docs/hamster-studio/routines) directly — "the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) that was just created", "the [Task](https://tryhamster.com/docs/hamster-studio/tasks) that was just completed".
* Triggers — choose one or more workspace events that cause the [Routine](https://tryhamster.com/docs/hamster-studio/routines) to run. Triggers are optional at save time — you can write and test your instructions before attaching any.
* Runs — see every execution for this [Routine](https://tryhamster.com/docs/hamster-studio/routines), with the input it received and the output it produced.

## Writing instructions

Instructions are plain-language prompts. Hamster receives the full context of the triggering event — the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) content, the [Task](https://tryhamster.com/docs/hamster-studio/tasks) details, the [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) it belongs to — so you can reference entities directly rather than describing them abstractly.

A few patterns that work:

```
When this brief is created, write a two-paragraph research summary based on
the description and add it to the brief as a context document.

```

```
When a task is marked complete, check that the task title and description
match the acceptance criteria in the parent brief. If they don't align,
post a note in the task thread with the specific discrepancy.

```

```
When this blueprint is updated, compare the new version against the previous
version and summarise what changed in three bullet points.

```

```
When an initiative status changes to "delivering", scan the attached briefs
for any tasks that are still in draft state and flag them in a comment on
the initiative.

```

```
When a brief is approved, write a one-paragraph summary of what was agreed
and the key decisions made, and attach it to the brief as a handover note.

```

```
When an initiative is marked at risk, review the attached briefs and list
the specific blockers or open questions that could be contributing.

```

Instructions can be as long as you need. [Routines](https://tryhamster.com/docs/hamster-studio/routines) support full markdown, so you can include examples, formatting rules, or multi-step logic.

## Testing your instructions before going live

Use **Test Run** to check that your instructions produce the right output before attaching any triggers.

Select **Test Run** from the [Routine](https://tryhamster.com/docs/hamster-studio/routines) modal, and Hamster executes what you've written in the editor right now — including any edits you haven't saved yet. You don't need to save before testing. Write a draft, run it, see what Hamster produces, adjust, and run again. Only save when you're happy.

The [Result](https://tryhamster.com/docs/hamster-studio/results) appears in the **Runs** tab. Each test-run entry shows the exact instructions that ran, so you can compare iterations side by side. Test runs are marked **Test run** in the run history and don't count toward the **Last run** column on the [Routines](https://tryhamster.com/docs/hamster-studio/routines) list — your tests don't displace the record of the last real execution.

You can test at any point, with or without triggers configured.

The test-run button is disabled when:

* Your instructions are empty — a tooltip explains why
* A run is pending or in progress
* A 30-second cooldown is active after the last run completes

## What happens when a routine runs

When a trigger fires, Hamster executes your instructions using the same AI that runs your conversations. It has access to the full workspace context — [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), documents, [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) — and can use the same tools available in chat: reading and writing [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), adding context documents, posting notes, and more.

[Routine](https://tryhamster.com/docs/hamster-studio/routines) executions run in the background and don't appear in your Conversations. Each run gets its own isolated thread, so your chat history stays focused on your actual conversations.

## Triggers

Triggers are workspace lifecycle events. Add one or more from the **Triggers** tab. A single [Routine](https://tryhamster.com/docs/hamster-studio/routines) can respond to multiple events — for example, both `brief.created` and `brief.status_changed`.

| Group                                                                    | Events                                                                                                                                                                                                                                                                                                                             |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **[Brief](https://tryhamster.com/docs/hamster-studio/briefs)**           | Created, status changed, [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation started/completed/failed, review requested, alignment vote submitted, approved, updated, deleted, document added/removed, [Task](https://tryhamster.com/docs/hamster-studio/tasks) added/removed, member added/removed, comment added |
| **[Initiative](https://tryhamster.com/docs/hamster-studio/initiatives)** | Created, state changed (shipped, blocked, archived), health changed (at risk, off track), updated, deleted, [Brief](https://tryhamster.com/docs/hamster-studio/briefs) added/removed, member added/removed, comment added                                                                                                          |
| **[Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints)**   | Created, updated, deleted, published, section added/removed                                                                                                                                                                                                                                                                        |
| **[Task](https://tryhamster.com/docs/hamster-studio/tasks)**             | Created, updated, status changed, assigned/unassigned, completed, deleted                                                                                                                                                                                                                                                          |
| **[Plan](https://tryhamster.com/docs/hamster-studio/plans)**             | Generated, updated                                                                                                                                                                                                                                                                                                                 |

Each trigger can be enabled or disabled individually — toggle the switch next to a trigger to pause it without removing the configuration.

## Posting to brief and blueprint chats

A [Routine](https://tryhamster.com/docs/hamster-studio/routines)'s instructions can tell Hamster to post a message directly into a [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s or [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints)'s chat thread — not just record output in the run history, but make it visible to your team in context.

This is useful when a [Routine](https://tryhamster.com/docs/hamster-studio/routines) is watching one thing but its output belongs somewhere else. For example, a [Routine](https://tryhamster.com/docs/hamster-studio/routines) that monitors [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) status changes can post a summary of what changed directly into the [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives)'s attached [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) so the people working on them see it without going to the [Routines](https://tryhamster.com/docs/hamster-studio/routines) page.

To use this in your instructions, describe what you want posted and where:

```
When the initiative status changes to "delivering", post a message to the
initiative's primary brief chat summarising what changed and listing any
tasks still in draft state.

```

Hamster finds the target thread, posts the message as an automated entry, and marks it so it's clear it came from a [Routine](https://tryhamster.com/docs/hamster-studio/routines) rather than a team member.

## When a routine is running

When a [Routine](https://tryhamster.com/docs/hamster-studio/routines) fires and is actively executing, a status indicator appears on the relevant thread entry point. This shows the [Routine](https://tryhamster.com/docs/hamster-studio/routines) is in progress — you do not need to refresh or check the Runs tab to know it's working. The indicator clears when the run completes.

## When routines fail

If a [Routine](https://tryhamster.com/docs/hamster-studio/routines) fails, the run is logged with the error. You can open the run from the **Runs** tab to see what went wrong — the full input the [Routine](https://tryhamster.com/docs/hamster-studio/routines) received and the error message are both visible.

If a [Routine](https://tryhamster.com/docs/hamster-studio/routines) fails five times in a row, Hamster disables it automatically and marks it as "Disabled by system" in the [Routines](https://tryhamster.com/docs/hamster-studio/routines) list. This prevents a misconfigured [Routine](https://tryhamster.com/docs/hamster-studio/routines) from continuing to fire against events it cannot handle. To re-enable it, fix the instructions and toggle it back on from the [Routine](https://tryhamster.com/docs/hamster-studio/routines) card.

Single failures do not disable a routine. The consecutive-failure threshold exists to catch [Routines](https://tryhamster.com/docs/hamster-studio/routines) that are broken in a way that will keep failing, not to disable [Routines](https://tryhamster.com/docs/hamster-studio/routines) that occasionally hit a transient error.

## Run history

Every execution is logged. Open the **Runs** tab inside a [Routine](https://tryhamster.com/docs/hamster-studio/routines) to see its history, or go to **[Routines](https://tryhamster.com/docs/hamster-studio/routines) → All Runs** to see every execution across your workspace in one feed.

The feed updates in real time as runs complete. Use the **Triggers** filter on the All Runs feed to narrow down to specific event types.

Each run shows:

* The trigger event that caused it (or "Test run" if manually triggered)
* The instructions that actually ran for that specific execution
* The output — what Hamster produced
* Status: queued, running, succeeded, or failed
* Start and completion timestamps

The instructions shown are what fired at that moment — not whatever the [Routine](https://tryhamster.com/docs/hamster-studio/routines) currently says. If you edited the [Routine](https://tryhamster.com/docs/hamster-studio/routines) after this run, the run history still reflects what actually executed. This matters when you're debugging: you can look at any run and know exactly what Hamster was working from.

Click any run to open the full thread view — the complete AI execution with tool calls, reasoning, and output, the same as any other Hamster conversation.

## Permissions

Creating, editing, and running [Routines](https://tryhamster.com/docs/hamster-studio/routines) requires the **Manage [Routines](https://tryhamster.com/docs/hamster-studio/routines)** permission. Members without this permission can view [Routines](https://tryhamster.com/docs/hamster-studio/routines) and their run history, but can't create, edit, or trigger them.

[Routines](https://tryhamster.com/docs/hamster-studio/routines) are account-level — they apply to your whole team workspace, not just the person who created them.

## Related

* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)
* [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives)
* [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints)
* [Tasks](https://tryhamster.com/docs/hamster-studio/tasks/task-overview)
* [Teams & Permissions](https://tryhamster.com/docs/hamster-studio/teams/roles-permissions)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Routines","item":"https://tryhamster.com/docs/hamster-studio/routines"}]}
```
