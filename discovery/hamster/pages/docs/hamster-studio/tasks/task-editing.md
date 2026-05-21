---
description: Edit Task status, priority, descriptions, notes, and subtasks without leaving the Task.
title: Task Editing | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Task Editing

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

# Task Editing

Update status, adjust priority, edit descriptions, add notes, and manage subtasks — all without leaving the task.

## Overview

[Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are working documents. They start with AI-generated content from the [Plan](https://tryhamster.com/docs/hamster-studio/plans), but they are meant to be shaped as work progresses. You can update a [Task](https://tryhamster.com/docs/hamster-studio/tasks)'s status, change its priority, edit its description to add context or acceptance criteria, and add subtasks to break down work that turns out to be larger than expected. All edits save immediately and are reflected across the [Plan](https://tryhamster.com/docs/hamster-studio/plans) list in real time.

![Task detail page in edit mode showing rich-text description and status controls](https://tryhamster.com/_site/images/features/tasks/task-editing/task-editing-desktop-light.webp?v=6)![Task detail page in edit mode showing rich-text description and status controls](https://tryhamster.com/_site/images/features/tasks/task-editing/task-editing-desktop-dark.webp?v=6) 

## Updating Status

[Tasks](https://tryhamster.com/docs/hamster-studio/tasks) have three states: **Todo**, **In Progress**, and **Done**.

**From the [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page**: Click the Status field in the metadata grid. A dropdown appears with all three options. Click any status to apply it immediately.

**Drag-and-drop in grouped list view**: When [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are grouped by status, drag a [Task](https://tryhamster.com/docs/hamster-studio/tasks) row from one section to another. The status updates as it crosses the section boundary.

**Drag-and-drop in kanban view**: Switch to kanban mode using the Display button. [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) appear as cards in columns corresponding to their status. Drag a card to a different column to change its status, or within a column to reorder. Both operations save immediately.

## Updating Priority

Priority levels are **Low**, **Medium**, **High**, and **Urgent**. The [Plan](https://tryhamster.com/docs/hamster-studio/plans) generator sets an initial priority, which you can change at any time.

From the [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page, click the Priority field in the metadata grid. Select the level you want. The change saves immediately. Priority is not shown on [Task](https://tryhamster.com/docs/hamster-studio/tasks) rows in the list view, but is always visible on the [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page.

## Editing the Description

The [Task](https://tryhamster.com/docs/hamster-studio/tasks) description is a rich-text document in the main body of the [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page. It is editable by default — no separate edit mode is required.

Click anywhere in the content area and begin typing. You can edit the AI-generated text, add headings, bullet lists, numbered lists, and other formatting, write implementation notes or acceptance criteria, and record decisions or reference links. Content auto-saves as you type. Description edits do not affect the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or plan.

## Managing Subtasks

### Adding a subtask manually

From inside any [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page, scroll to the Subtasks section. Click "Add Subtask". An inline input appears — type the subtask title and press Enter to create it, or Escape to cancel.

### Generating subtasks with AI

When a [Task](https://tryhamster.com/docs/hamster-studio/tasks) has no subtasks, an "Expand Subtasks" button appears next to "Add Subtask". Clicking it sends the [Task](https://tryhamster.com/docs/hamster-studio/tasks) to the AI, which reads the [Task](https://tryhamster.com/docs/hamster-studio/tasks) description and broader [Brief](https://tryhamster.com/docs/hamster-studio/briefs) context and generates a structured set of subtasks. [Results](https://tryhamster.com/docs/hamster-studio/results) stream in as they are created — you will see them appear without needing to reload. Once generated, each subtask can be edited, reordered, or deleted independently.

The "Expand Subtasks" button only appears when the [Task](https://tryhamster.com/docs/hamster-studio/tasks) has no subtasks yet.

### Reordering subtasks

Drag any subtask row up or down within the Subtasks section to reorder it. The new order saves immediately.

### Opening a subtask

Click any subtask to open its own [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page. Subtask detail pages have the same layout as top-level [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) — you can view and edit the description, update status, assign it, and add further nested subtasks.

## Display Options

The [Plan](https://tryhamster.com/docs/hamster-studio/plans) tab includes a Display button that controls how [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) appear in the list without changing the [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) themselves:

* **View**: Switch between List and Kanban. List view shows [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) as rows. Kanban view shows [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) as cards in columns.
* **Group By**: Choose None for a flat ordered list, or Status to group [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) into Todo, In Progress, and Done sections. Grouping is available in both List and Kanban view.

## Key Capabilities

* **Inline status changes**: Status can be changed from the [Task](https://tryhamster.com/docs/hamster-studio/tasks) row in the list and from the metadata grid in the [Task](https://tryhamster.com/docs/hamster-studio/tasks) detail page.
* **Drag-to-reorder and drag-to-status**: [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) and subtasks can be reordered by dragging. In grouped and kanban views, dragging across sections changes status.
* **Live rich-text editing**: The description editor is always active. Edits save automatically and appear instantly for anyone viewing the task.
* **AI subtask generation**: "Expand Subtasks" generates a structured breakdown asynchronously, streaming [Results](https://tryhamster.com/docs/hamster-studio/results) in real time.
* **Manual subtask creation**: "Add Subtask" provides a fast inline form for creating subtasks without navigating away.

## Tips

* Use the description editor to capture the definition of done for each [Task](https://tryhamster.com/docs/hamster-studio/tasks) when it is first generated. Clear acceptance criteria reduce back-and-forth later.
* If you are planning work across a team, generate the [Plan](https://tryhamster.com/docs/hamster-studio/plans) and then use the kanban view grouped by status to drag [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) into priority order before assigning them.
* Moving a [Task](https://tryhamster.com/docs/hamster-studio/tasks) back from Done to In Progress is fully supported — rework is normal. The [Task](https://tryhamster.com/docs/hamster-studio/tasks) will reappear in the In Progress column for the team to see.

## Related

* [Task Overview](https://tryhamster.com/docs/hamster-studio/tasks/task-overview)
* [Task Details](https://tryhamster.com/docs/hamster-studio/tasks/task-details)
* [Task Assignment](https://tryhamster.com/docs/hamster-studio/tasks/task-assignment)
* [Generating Plans](https://tryhamster.com/docs/hamster-studio/plans/generating-plans)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Tasks","item":"https://tryhamster.com/docs/hamster-studio/tasks"},{"@type":"ListItem","position":5,"name":"Task Editing","item":"https://tryhamster.com/docs/hamster-studio/tasks/task-editing"}]}
```
