---
description: Use the terminal dashboard, everyday commands, and scoped prompts for agent-assisted Delivery.
title: Using the CLI | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Using the CLI

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
   * [CLI Sync](https://tryhamster.com/docs/hamster-studio/cli/cli-sync "CLI Sync")  
   * [Getting Started](https://tryhamster.com/docs/hamster-studio/cli/cli-authentication "Getting Started")  
   * [Using the CLI](https://tryhamster.com/docs/hamster-studio/cli/cli-brief-creation "Using the CLI")  
   * [Slash Commands](https://tryhamster.com/docs/hamster-studio/cli/slash-commands "Slash Commands")

* MCP Server

* [Taskmaster](https://tryhamster.com/docs/taskmaster "Taskmaster")
* Workspace

* Teams

* Collaboration

* Account Settings

# Using the CLI

The terminal dashboard, everyday commands, and example prompts for working with your coding agent.

## The Dashboard

Run `hamster` with no arguments to open the terminal dashboard. It shows four tabs:

* Dashboard — [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and [Task](https://tryhamster.com/docs/hamster-studio/tasks) counts, a progress bar for [Task](https://tryhamster.com/docs/hamster-studio/tasks) completion, and recent activity across your project
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) — Browse [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) with a [Task](https://tryhamster.com/docs/hamster-studio/tasks) list for each one. Press Enter to open a kanban view with [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) grouped by status
* [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) — Read your architecture documents rendered as formatted markdown
* [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) — Read your team conventions and processes

The dashboard watches for changes in real time. If a teammate updates a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or moves a [Task](https://tryhamster.com/docs/hamster-studio/tasks) in the browser, the dashboard reflects it within seconds.

### Keyboard Shortcuts

| Key             | Action                                                                                                                                                                                                                       |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1 2 3 4         | Jump to Dashboard / [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) / [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) / [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) |
| j / k or arrows | Navigate lists                                                                                                                                                                                                               |
| Enter           | Open detail view or kanban                                                                                                                                                                                                   |
| e               | Open the selected file in your editor                                                                                                                                                                                        |
| Space           | Cycle a [Task](https://tryhamster.com/docs/hamster-studio/tasks)'s status (pending, in progress, done)                                                                                                                       |
| s               | Trigger a manual sync                                                                                                                                                                                                        |
| ?               | Toggle help                                                                                                                                                                                                                  |
| q               | Quit                                                                                                                                                                                                                         |

## Commands

| Command                          | What it does                                                                     |
| -------------------------------- | -------------------------------------------------------------------------------- |
| hamster                          | Open the terminal dashboard                                                      |
| hamster sync                     | Pull the latest project context once                                             |
| hamster sync --watch             | Keep local files updated continuously                                            |
| hamster sync --force             | Ignore cache and pull everything fresh                                           |
| hamster brief create "Title"     | Create a new [Brief](https://tryhamster.com/docs/hamster-studio/briefs)          |
| hamster blueprint create "Title" | Create a new [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints)  |
| hamster method create "Title"    | Create a new [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) |
| hamster brief get                | View a [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s full content |
| hamster task get HAM-123         | View a [Task](https://tryhamster.com/docs/hamster-studio/tasks)'s full details   |
| hamster team                     | Switch between team accounts                                                     |
| hamster status                   | Show sync statistics, entity counts, and auth state                              |
| hamster auth login               | Authenticate or switch accounts                                                  |
| hamster auth logout              | Clear your local session                                                         |
| hamster init                     | Set up a new project (first-time only)                                           |

## Example Agent Prompts

Once `hamster sync --watch` is running and your agent has the project context loaded, these kinds of prompts work naturally:

**Starting work**

* "Read the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) for my-project and summarize what needs to be built"
* "What's the next [Task](https://tryhamster.com/docs/hamster-studio/tasks) I should work on?"
* "Show me the acceptance criteria for HAM-042"

**Building with context**

* "Implement HAM-015 following the patterns in the engineering-context [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints)"
* "Work on the next [Task](https://tryhamster.com/docs/hamster-studio/tasks), using the [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) in code-review-process"
* "Check the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) requirements before starting HAM-023 — make sure nothing has changed"

**Tracking progress**

* "Which [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are still in progress?"
* "How many [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are done on the auth [Brief](https://tryhamster.com/docs/hamster-studio/briefs)?"
* "Mark HAM-015 as done and pick up the next one"

These prompts work because the agent reads the synced `.hamster/` files directly. The [Brief](https://tryhamster.com/docs/hamster-studio/briefs) requirements, [Task](https://tryhamster.com/docs/hamster-studio/tasks) instructions, acceptance criteria, [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), and [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) are all on disk as plain markdown — the agent does not need API access to answer these questions.

For agents that can also write back to Hamster (updating [Task](https://tryhamster.com/docs/hamster-studio/tasks) status, creating subtasks), see [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp).

## Tips

* Run `hamster sync --watch` in a background terminal or tmux pane so context stays current while you work.
* Press `e` in the dashboard to open any [Brief](https://tryhamster.com/docs/hamster-studio/briefs), [Task](https://tryhamster.com/docs/hamster-studio/tasks), [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints), or [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) file in your `$EDITOR`.
* Press Space on a [Task](https://tryhamster.com/docs/hamster-studio/tasks) in the [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) tab to cycle its status without leaving the terminal.
* `hamster status` is a quick way to check how many entities are synced and when the last sync ran.

## Related

* [CLI Sync](https://tryhamster.com/docs/hamster-studio/cli/cli-sync)
* [Getting Started](https://tryhamster.com/docs/hamster-studio/cli/cli-authentication)
* [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Cli","item":"https://tryhamster.com/docs/hamster-studio/cli"},{"@type":"ListItem","position":5,"name":"Cli Brief Creation","item":"https://tryhamster.com/docs/hamster-studio/cli/cli-brief-creation"}]}
```
