---
description: The full list of 20 tools your coding agent can use through the Hamster MCP server, across accounts, briefs, tasks, subtasks, documents, and plans.
title: Available Tools | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Available Tools

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
   * [Getting Started](https://tryhamster.com/docs/hamster-studio/mcp/getting-started "Getting Started")  
   * [Available Tools](https://tryhamster.com/docs/hamster-studio/mcp/available-tools "Available Tools")

* [Taskmaster](https://tryhamster.com/docs/taskmaster "Taskmaster")
* Workspace

* Teams

* Collaboration

* Account Settings

# Available Tools

_The full list of 20 tools your coding agent can use through the Hamster MCP server._

## Overview

When your agent connects to the Hamster [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp), it gains access to 20 tools organized across six areas: accounts, [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), subtasks, documents, and plans. These tools let the agent read your project context, create and update work items, and navigate between accounts — all scoped to your permissions.

Every tool runs as the signed-in user. A Reviewer can list [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), threads, and [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) but cannot mutate them; a Creator can create and update; an Admin and Owner can do everything their role allows in the browser. There is no admin override at the MCP layer — your role is your role.

## Accounts

| Tool            | What it does                               |
| --------------- | ------------------------------------------ |
| list\_accounts  | Show all your accounts (personal and team) |
| switch\_account | Switch to a different account              |

## Briefs

| Tool          | What it does                                                                                        |
| ------------- | --------------------------------------------------------------------------------------------------- |
| list\_briefs  | List [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) in the current account             |
| get\_brief    | Get a [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s full content and metadata        |
| create\_brief | Create a new [Brief](https://tryhamster.com/docs/hamster-studio/briefs)                             |
| update\_brief | Update a [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s title, description, or status |
| delete\_brief | Delete a [Brief](https://tryhamster.com/docs/hamster-studio/briefs)                                 |

## Tasks

| Tool                 | What it does                                                                                                                                                                              |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| list\_tasks          | List [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) for a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), with optional filters for status, priority, and assignee |
| get\_task            | Get a [Task](https://tryhamster.com/docs/hamster-studio/tasks)'s full details including subtasks and dependencies                                                                         |
| create\_task         | Create a new [Task](https://tryhamster.com/docs/hamster-studio/tasks) under a [Brief](https://tryhamster.com/docs/hamster-studio/briefs)                                                  |
| update\_task         | Update a [Task](https://tryhamster.com/docs/hamster-studio/tasks)'s title, description, priority, assignee, or other fields                                                               |
| update\_task\_status | Move a [Task](https://tryhamster.com/docs/hamster-studio/tasks) to a new status (to do, in progress, done)                                                                                |
| get\_next\_task      | Get the next [Task](https://tryhamster.com/docs/hamster-studio/tasks) to work on based on priority and dependencies                                                                       |

## Subtasks

| Tool            | What it does                                                                 |
| --------------- | ---------------------------------------------------------------------------- |
| list\_subtasks  | List subtasks for a [Task](https://tryhamster.com/docs/hamster-studio/tasks) |
| create\_subtask | Add a subtask to a [Task](https://tryhamster.com/docs/hamster-studio/tasks)  |
| update\_subtask | Update a subtask's content or status                                         |
| delete\_subtask | Remove a subtask                                                             |

## Documents

| Tool            | What it does                                                                            |
| --------------- | --------------------------------------------------------------------------------------- |
| list\_documents | List documents attached to a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) |
| get\_document   | Get a document's full content                                                           |

## Plans

| Tool      | What it does                                                                                                                                                                                                              |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| get\_plan | Get the full [Plan](https://tryhamster.com/docs/hamster-studio/plans) for a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), including all generated [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) |

## How Tools Are Discovered

Your AI tool calls `tools/list` once per session and gets back the full list of 20 tools, each with its input schema and description. The schema is rich enough that the AI can infer when to use a tool without you spelling it out — "what's my next [Task](https://tryhamster.com/docs/hamster-studio/tasks)?" maps to `get_next_task`, "what [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) do I have open?" maps to `list_briefs`, and so on.

Hamster's [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) is stateless — each call carries your auth token and the active account context, and the server resolves the right team-account scope per request. That makes it safe for AI tools that open and close [Connections](https://tryhamster.com/docs/hamster-studio/connections) frequently or run multiple sessions in parallel.

## Tips

* The `get_next_task` tool is particularly useful for agentic workflows. It returns the highest-priority [Task](https://tryhamster.com/docs/hamster-studio/tasks) that has no unfinished dependencies — so the agent always picks up the right thing next.
* `get_task` and `update_task_status` accept both UUIDs and display IDs (like `HAM-123`), so your agent can reference [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) the same way you do.
* `list_tasks` supports filters for status, priority, and assignee — useful when you want the agent to focus on a specific slice of work.
* `update_task_status` handles reordering automatically. When the AI moves a [Task](https://tryhamster.com/docs/hamster-studio/tasks) to "done", the [Task](https://tryhamster.com/docs/hamster-studio/tasks) list stays correctly sorted.
* Tool [Results](https://tryhamster.com/docs/hamster-studio/results) respect your role. If an action is blocked by your permissions, the response carries a clear error rather than a silent failure.
* The [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) and the [CLI](https://tryhamster.com/docs/hamster-studio/cli) complement each other: MCP gives the agent live read/write access; [CLI](https://tryhamster.com/docs/hamster-studio/cli) sync keeps the same content on disk as markdown your agent can grep, read, and reference without an API call.

## Related

* [Getting Started](https://tryhamster.com/docs/hamster-studio/mcp/getting-started)
* [MCP Server Overview](https://tryhamster.com/docs/hamster-studio/mcp)
* [Task Overview](https://tryhamster.com/docs/hamster-studio/tasks/task-overview)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Mcp","item":"https://tryhamster.com/docs/hamster-studio/mcp"},{"@type":"ListItem","position":5,"name":"Available Tools","item":"https://tryhamster.com/docs/hamster-studio/mcp/available-tools"}]}
```
