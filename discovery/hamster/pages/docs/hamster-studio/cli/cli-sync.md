---
description: Keep your coding agent in sync with your project context — briefs, tasks, blueprints, and methods update on disk in real time.
title: CLI Sync | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

CLI Sync

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

# CLI Sync

Keep your coding agent in sync with your project context — [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), and [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) update on disk in real time.

## Overview

When you run `hamster sync --watch`, the [CLI](https://tryhamster.com/docs/hamster-studio/cli) holds a live [Connection](https://tryhamster.com/docs/hamster-studio/connections) to Hamster Studio and writes every change to your `.hamster/` directory as it happens. A teammate updates [Task](https://tryhamster.com/docs/hamster-studio/tasks) requirements in the browser — within seconds, the markdown file on your disk reflects the change. Your coding agent reads that file on its next action and has current context.

This is the core of what the [CLI](https://tryhamster.com/docs/hamster-studio/cli) does: it turns your project management context into a local, always-current [Knowledge](https://tryhamster.com/docs/concepts/knowledge) base that your coding agent can read directly.

## What Your Agent Gets

Every synced file is a markdown document with structured YAML frontmatter. A [Task](https://tryhamster.com/docs/hamster-studio/tasks) file includes the [Task](https://tryhamster.com/docs/hamster-studio/tasks) description, acceptance criteria, priority, estimated complexity, and dependency chain. A [Brief](https://tryhamster.com/docs/hamster-studio/briefs) file has the full product requirements. [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) contain architecture decisions. [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) capture team conventions.

When your coding agent starts a session in a repo with `.hamster/` synced, it can read these files to understand:

* What to build — the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s requirements and the [Task](https://tryhamster.com/docs/hamster-studio/tasks)'s instructions
* When it's done — the acceptance criteria listed in the [Task](https://tryhamster.com/docs/hamster-studio/tasks)
* How to build it — [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) for architecture patterns, [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) for team conventions
* What to work on next — [Task](https://tryhamster.com/docs/hamster-studio/tasks) priority, status, and dependency ordering

No copy-pasting requirements into chat. No switching windows to check a [Task](https://tryhamster.com/docs/hamster-studio/tasks) description. The context is on disk, in the repo, updated live.

## Skill Generation

After each sync, the [CLI](https://tryhamster.com/docs/hamster-studio/cli) generates a skill file at `.claude/skills/hamster-project-context/SKILL.md`. This file tells your agent where every synced document lives, how to interpret the frontmatter fields, and how to navigate between [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), and methods. It loads automatically at session start.

The skill file also includes current statistics — how many [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), and [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) are synced, and when the last sync ran — so the agent knows the scope of the project it is working on.

## What Gets Synced

| Entity                                                               | Local path                                               | What's in it                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------- | --------------------------------------------------------------------- |
| [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)          | .hamster/{account}/briefs/{brief}/brief.md               | Product requirements and context                                      |
| [Tasks](https://tryhamster.com/docs/hamster-studio/tasks)            | .hamster/{account}/briefs/{brief}/tasks/HAM-001-title.md | Instructions, acceptance criteria, priority, complexity, dependencies |
| [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints)  | .hamster/{account}/blueprints/{name}.md                  | Architecture decisions and patterns                                   |
| [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) | .hamster/{account}/methods/{name}.md                     | Team conventions and processes                                        |

Done and archived [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) are excluded automatically. Your `.hamster/` directory only contains active work.

## One-Time and Continuous Sync

`hamster sync` runs once and exits — useful for CI environments or quick refreshes.

You can also target a single [Brief](https://tryhamster.com/docs/hamster-studio/briefs) directly by passing a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) UUID, slug, or full Studio URL.

`hamster sync --watch` runs continuously. It does an initial full sync, then listens for changes over a live connection. Individual files update as they change — the [CLI](https://tryhamster.com/docs/hamster-studio/cli) does not re-download everything on each edit. If the [Connection](https://tryhamster.com/docs/hamster-studio/connections) drops, it reconnects and runs a full sync to catch anything missed.

Run `hamster sync --force` to ignore the local cache and pull everything fresh.

If `.hamster/` is missing, `hamster sync` auto-initializes the local directory before syncing.

## File Structure

```
.hamster/{account-slug}/
├── briefs/
│   └── my-project/
│       ├── brief.md
│       └── tasks/
│           ├── HAM-001-set-up-auth.md
│           └── HAM-002-build-dashboard.md
├── blueprints/
│   └── engineering-context.md
├── methods/
│   └── code-review-process.md
└── .state.json

.claude/skills/hamster-project-context/
└── SKILL.md

```

Add `.hamster/` to your `.gitignore`. The content is generated and specific to your account.

## Tips

* Run `hamster status` to see sync statistics — what was synced last, how many entities are on disk, and whether anything is stale.
* Watch mode reconnects automatically and runs a full resync on reconnect. You do not need to restart it.
* [Task](https://tryhamster.com/docs/hamster-studio/tasks) files include structured metadata from [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation: priority, estimated hours, dependencies, and acceptance criteria. This is the same information your coding agent uses to pick the right [Task](https://tryhamster.com/docs/hamster-studio/tasks) and know when it is done.
* Combine file sync with the [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) for bidirectional flow: the [CLI](https://tryhamster.com/docs/hamster-studio/cli) gives your agent read access to current context, and the [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) lets it write back — updating [Task](https://tryhamster.com/docs/hamster-studio/tasks) status, creating subtasks, marking work done.

## Related

* [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp)
* [Getting Started](https://tryhamster.com/docs/hamster-studio/cli/cli-authentication)
* [Using the CLI](https://tryhamster.com/docs/hamster-studio/cli/cli-brief-creation)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Cli","item":"https://tryhamster.com/docs/hamster-studio/cli"},{"@type":"ListItem","position":5,"name":"Cli Sync","item":"https://tryhamster.com/docs/hamster-studio/cli/cli-sync"}]}
```
