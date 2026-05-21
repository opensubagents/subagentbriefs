---
description: Cluster visualization and autonomous execution with iTerm2/tmux for parallel task processing. Learn how Hamster helps teams plan, build, and ship...
title: Clusters | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Clusters

* Welcome  
   * [Introduction](https://tryhamster.com/docs/taskmaster "Introduction")

* Getting Started

* Task Workflow

* Automation

* AI Providers

* IDE & Editor Setup

* Team Collaboration

* Best Practices

* TDD Workflow

* Technical Capabilities  
   * [MCP Tools](https://tryhamster.com/docs/taskmaster/capabilities/mcp "MCP Tools")  
   * [CLI Commands](https://tryhamster.com/docs/taskmaster/capabilities/cli-root-commands "CLI Commands")  
   * [Task Structure](https://tryhamster.com/docs/taskmaster/capabilities/task-structure "Task Structure")  
   * [Clusters](https://tryhamster.com/docs/taskmaster/capabilities/clusters "Clusters")

# Clusters & Execution

Task Master automatically detects **execution clusters** — groups of tasks that can run in parallel, sequenced by their dependency graph. The `clusters` command visualizes your execution topology, and `clusters start` launches an autonomous Claude Code session to execute the plan.

## Recommended Setup

For the best experience with `tm clusters start`, use **iTerm2** with **tmux control mode**. This gives Claude Code's agent teams the ability to open split panes and manage parallel work visually.

### Step-by-step

1. Open iTerm2 (macOS) — [download here](https://iterm2.com) if you don't have it
2. Start tmux in control mode:  
```bash  
tmux -CC  
```  
iTerm2 will open a native tmux integration window. This lets Claude Code spawn panes and tabs that iTerm2 manages natively — no raw tmux key bindings needed.
3. Run the command:  
```bash  
tm clusters start --tag <tag>  
```  
Or without a tag to execute the active tag:  
```bash  
tm clusters start  
```

**Tip:** `tmux -CC` is iTerm2's "control mode" — it bridges tmux sessions with iTerm2's native tab/pane management. You get all the benefits of tmux (session persistence, pane splitting) with iTerm2's UI. Claude Code's agent teams leverage this to orchestrate parallel task execution across panes.

## Visualizing Clusters

Before executing, use `tm clusters` to understand your project's execution topology.

### Tag-level phases

Without a `--tag` flag, `clusters` shows your tags organized into execution phases:

```bash
tm clusters

```

Tags at the same level can run in parallel. Tags at higher levels depend on lower levels completing first.

### Task-level clusters

Drill into a specific tag to see how its tasks are clustered:

```bash
tm clusters --tag backend

```

Each cluster groups tasks that share the same topological level — they have no dependencies on each other and can execute concurrently.

### Output formats

| Flag                   | Output                               | Use case                                                           |
| ---------------------- | ------------------------------------ | ------------------------------------------------------------------ |
| _(default)_            | Table with cluster breakdown         | Quick overview                                                     |
| \--tree                | ASCII dependency tree                | Understanding task relationships                                   |
| \--diagram mermaid     | Rendered Mermaid diagram in terminal | Visual dependency graph                                            |
| \--diagram mermaid-raw | Raw Mermaid syntax                   | Copy-paste into docs, PRs, or [mermaid.live](https://mermaid.live) |
| \--json                | Raw JSON                             | Programmatic access                                                |

```bash
# Visual dependency graph
tm clusters --tag backend --diagram mermaid

# Raw Mermaid for embedding in docs
tm clusters --diagram mermaid-raw > execution-plan.mmd

```

## Executing Clusters

### `tm clusters start`

Builds an execution plan from your task graph and launches an interactive Claude Code session with agent teams enabled.

```bash
tm clusters start --tag <tag>

```

**What happens:**

1. Task Master loads your tasks and detects clusters from the dependency DAG
2. An execution plan is built — showing clusters, task count, and estimated turns
3. The plan is displayed for review
4. Claude Code launches with a system prompt containing the full execution context
5. Agent teams mode is enabled (`CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1`), allowing Claude to spawn sub-agents for parallel task execution

### CLI options

| Option                 | Description                                  |
| ---------------------- | -------------------------------------------- |
| \-t, --tag <tag>       | Tag to execute (default: active tag)         |
| \--dry-run             | Show execution plan without launching Claude |
| \--parallel <n>        | Max concurrent tasks per level (default: 5)  |
| \--resume              | Resume from a previous checkpoint            |
| \--continue-on-failure | Keep going even if some tasks fail           |
| \--json                | Output the execution plan as JSON            |
| \-p, --project <path>  | Project root (auto-detected if not provided) |

### Dry run

Preview the execution plan without launching a Claude session:

```bash
tm clusters start --tag backend --dry-run

```

### Resume from checkpoint

If a session is interrupted (Ctrl+C), Task Master saves a checkpoint automatically. Resume where you left off:

```bash
tm clusters start --tag backend --resume

```

## Example Workflow

```bash
# 1. See the big picture -- tag-level execution phases
tm clusters

# 2. Drill into a tag
tm clusters --tag backend

# 3. Preview the execution plan
tm clusters start --tag backend --dry-run

# 4. Open iTerm2, start tmux control mode, and execute
tmux -CC
tm clusters start --tag backend

```

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Capabilities","item":"https://tryhamster.com/docs/taskmaster/capabilities"},{"@type":"ListItem","position":5,"name":"Clusters","item":"https://tryhamster.com/docs/taskmaster/capabilities/clusters"}]}
```
