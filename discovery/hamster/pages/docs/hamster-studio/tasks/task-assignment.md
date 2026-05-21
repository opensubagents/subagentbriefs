---
description: Assign a Task to a teammate or AI agent from the Task list or detail page.
title: Task Assignment | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Task Assignment

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
   * [Overview](https://tryhamster.com/docs/hamster-studio/tasks "Overview")  
   * [Task Overview](https://tryhamster.com/docs/hamster-studio/tasks/task-overview "Task Overview")  
   * [Task Details](https://tryhamster.com/docs/hamster-studio/tasks/task-details "Task Details")  
   * [Task Assignment](https://tryhamster.com/docs/hamster-studio/tasks/task-assignment "Task Assignment")  
   * [Task Editing](https://tryhamster.com/docs/hamster-studio/tasks/task-editing "Task Editing")

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

# Task Assignment

Assign any [Task](https://tryhamster.com/docs/hamster-studio/tasks) to a team member or an AI agent directly from the [Task](https://tryhamster.com/docs/hamster-studio/tasks) list or [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page.

## Overview

[Task](https://tryhamster.com/docs/hamster-studio/tasks) assignment connects a piece of work to the person or agent responsible for delivering it. Assignments are visible throughout the [Task](https://tryhamster.com/docs/hamster-studio/tasks) list and inside the [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page, making it clear at a glance who owns what. Any team member with access to the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) can assign or reassign a [Task](https://tryhamster.com/docs/hamster-studio/tasks) at any time. If your workspace has an AI coding agent configured and connected to a code repository, you can also assign [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) to that agent to have it work on the implementation automatically.

![Task list showing the assignee picker dropdown with team members and AI agents](https://tryhamster.com/_site/images/features/tasks/task-assignment/task-assignment-desktop-light.webp?v=6)![Task list showing the assignee picker dropdown with team members and AI agents](https://tryhamster.com/_site/images/features/tasks/task-assignment/task-assignment-desktop-dark.webp?v=6) 

## How It Works

1. Find the [Task](https://tryhamster.com/docs/hamster-studio/tasks) — Navigate to the [Plan](https://tryhamster.com/docs/hamster-studio/plans) tab of the brief. Each [Task](https://tryhamster.com/docs/hamster-studio/tasks) row shows an assignee avatar on the right side. A grey placeholder means the [Task](https://tryhamster.com/docs/hamster-studio/tasks) is unassigned.
2. Open the assignee picker — Click the avatar or the chevron beside it. A dropdown appears showing "Agents" (if configured) and "Team Members". The current assignee is marked with a "Current" badge.
3. Select an assignee — Click any name. The assignment saves immediately and the avatar on the [Task](https://tryhamster.com/docs/hamster-studio/tasks) row updates. Select "Unassigned" at the top to remove the assignment.
4. Assign from the [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page — Open the [Task](https://tryhamster.com/docs/hamster-studio/tasks) and click the Assignee field in the metadata grid. The same picker appears and saves the same way.

## Assigning to a Team Member

Team members appear under "Team Members" in the picker. Selecting one saves the assignment immediately — the member's name and avatar appear on the [Task](https://tryhamster.com/docs/hamster-studio/tasks) row, giving the rest of the team visibility into ownership. You can assign to yourself or to any other team member. There is no approval step.

## Assigning to an AI Agent

If your workspace has a coding agent configured, an "Agents" section appears at the top of the picker. Agents are only available for top-level [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) — the section does not appear when working with a subtask.

When you assign a [Task](https://tryhamster.com/docs/hamster-studio/tasks) to an agent:

1. A [Delivery](https://tryhamster.com/docs/concepts/delivery) dialog opens where you confirm the repository, branch, and any additional context.
2. The [Task](https://tryhamster.com/docs/hamster-studio/tasks) status moves to "In Progress".
3. The agent starts working on the [Task](https://tryhamster.com/docs/hamster-studio/tasks) in the connected code repository.
4. The [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page shows a status strip with the run status and a progress percentage.
5. When the agent finishes, a link to the pull request appears in the status strip.

You can also use the [Delivery](https://tryhamster.com/docs/concepts/delivery) button on the [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page to launch with your saved preferences in one click. [Delivery](https://tryhamster.com/docs/concepts/delivery) preferences (which agent to use, default branch) are saved at the account level so you don't need to configure them each time.

## Unassigning a Task

Open the assignee picker and select "Unassigned" at the top. Unassigning a [Task](https://tryhamster.com/docs/hamster-studio/tasks) that was previously assigned to an agent does not cancel any in-progress agent run — agent runs continue independently once started.

## Key Capabilities

* **Assign from list or detail view**: Both surfaces use the same picker and save immediately.
* **Visual ownership in the [Task](https://tryhamster.com/docs/hamster-studio/tasks) list**: [Task](https://tryhamster.com/docs/hamster-studio/tasks) rows show the assignee's avatar. Unassigned [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) show a placeholder for easy scanning.
* **Agent assignment**: Assigning to an AI agent triggers automated work on the [Task](https://tryhamster.com/docs/hamster-studio/tasks) in the connected code repository.
* **Agent run visibility**: The [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page shows a live status strip for any agent working on the [Task](https://tryhamster.com/docs/hamster-studio/tasks), with a link to the pull request.
* **Subtask assignment**: Subtasks can be assigned to team members using the same picker, minus the Agents section.

## Tips

* Assign [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) as soon as the [Plan](https://tryhamster.com/docs/hamster-studio/plans) is generated. Even a tentative assignment helps the team understand who is expected to pick up each item.
* If a [Task](https://tryhamster.com/docs/hamster-studio/tasks) is blocked or handed off, reassign it at any point — no history or notes are lost.
* Agents require a code repository [Connection](https://tryhamster.com/docs/hamster-studio/connections) before assignment triggers automated work. See [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview) for setup instructions.

## Related

* [Task Overview](https://tryhamster.com/docs/hamster-studio/tasks/task-overview)
* [Task Details](https://tryhamster.com/docs/hamster-studio/tasks/task-details)
* [Task Editing](https://tryhamster.com/docs/hamster-studio/tasks/task-editing)
* [Inviting Members](https://tryhamster.com/docs/hamster-studio/teams/inviting-members)
* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Tasks","item":"https://tryhamster.com/docs/hamster-studio/tasks"},{"@type":"ListItem","position":5,"name":"Task Assignment","item":"https://tryhamster.com/docs/hamster-studio/tasks/task-assignment"}]}
```
