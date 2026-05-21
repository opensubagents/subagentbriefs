---
description: Recommended workflows, productivity tips, and patterns for getting the most out of Taskmaster. Learn how Hamster helps teams plan, build, and ship...
title: Best Practices | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Best Practices Overview

* Welcome  
   * [Introduction](https://tryhamster.com/docs/taskmaster "Introduction")

* Getting Started

* Task Workflow

* Automation

* AI Providers

* IDE & Editor Setup

* Team Collaboration

* Best Practices  
   * [Best Practices Overview](https://tryhamster.com/docs/taskmaster/best-practices/index "Best Practices Overview")  
   * [Advanced Configuration](https://tryhamster.com/docs/taskmaster/best-practices/configuration-advanced "Advanced Configuration")  
   * [Advanced Tasks](https://tryhamster.com/docs/taskmaster/best-practices/advanced-tasks "Advanced Tasks")

* TDD Workflow

* Technical Capabilities

# Best Practices

These patterns and workflows will help you move faster, stay organized, and get better results from Taskmaster across your projects.

## The Recommended Workflow

Follow this cycle for the best results on any project:

1. Write a PRD — Describe what you want to build in plain text
2. Parse it — `tm parse-prd` generates a structured task plan
3. Analyze complexity — `tm analyze-complexity` scores every task
4. Review the report — `tm complexity-report` shows what needs breaking down
5. Expand complex tasks — `tm expand` splits high-complexity tasks into subtasks
6. Research unknowns — `tm research` gathers live information for technical decisions
7. Pick your next task — `tm next` selects the highest-priority unblocked task
8. Implement — Work on the task with full context from details and test strategy
9. Update if needed — `tm update` keeps future tasks aligned if plans change
10. Mark complete — `tm set-status --id=N --status=done` and move on

This cycle keeps your project structured while adapting to what you learn during implementation.

## Start with Complexity Analysis

Before writing any code, run complexity analysis on your task list:

`tm analyze-complexity --research` 

This scores every task on a 1–10 scale and recommends how many subtasks each one needs. Then review the formatted report:

`tm complexity-report` 

**Why this matters:** Tasks that seem simple in a PRD often hide significant complexity. Analyzing upfront prevents surprises mid-implementation and helps you allocate time accurately.

Expand your highest-complexity tasks first:

```bash
# Expand a specific complex task
tm expand --id=5

# Expand with additional context
tm expand --id=5 --prompt="Focus on security considerations"

# Expand all pending tasks at once
tm expand --all

```

## Research Before You Build

Use the built-in research command whenever you're working with unfamiliar technology, making architectural decisions, or need information beyond AI training data:

```bash
# Basic research
tm research "JWT best practices for refresh token rotation"

# Research with task context
tm research "React Query v5 migration" --id=15

# Research with file context
tm research "Optimize this database schema" --files=src/db/schema.ts

# Save findings directly to a task
tm research "OAuth PKCE flow" --save-to=12

```

Research uses your configured research model (typically Perplexity) to pull live information from the web. This is especially valuable for:

* Security-sensitive implementations
* New library or framework adoption
* Performance optimization strategies
* Debugging complex issues

**Tip:** Research first, then update your tasks with the findings. This produces better subtasks and implementation details than guessing.

## View Multiple Tasks Together

When planning your next stretch of work, view several tasks at once for a bird's-eye perspective:

```bash
# View multiple tasks in a compact table
tm show 5,7,9

# Mix parent tasks and subtasks
tm show 44,44.1,55,55.2

```

The multi-task view shows a summary table with status, priority, and progress indicators. You can also perform batch operations — marking multiple tasks as in-progress, expanding all of them, or checking dependency relationships at a glance.

## Keep Tasks in Sync with Reality

Plans change during implementation. When your approach diverges from what was originally planned, update future tasks so they reflect reality:

```bash
# Update all tasks from a given ID forward
tm update --from=4 --prompt="Switched from REST to GraphQL for the API layer"

# Use research-backed updates for better suggestions
tm update --from=4 --prompt="Migrating to MongoDB" --research

# Update a single task's details
tm update-task --id=3 --prompt="Need to handle pagination differently"

```

This rewrites future task details while preserving completed work — no need to start over or manually rewrite your plan.

## Use Tags for Parallel Workstreams

Tags let you maintain separate task lists for different features, branches, or experiments:

```bash
# Create a tag from your current git branch
tm add-tag --from-branch

# Create a named tag
tm add-tag api-v2 --description="API v2 redesign"

# Switch context
tm use-tag auth

# Copy current tasks into a new tag for experimentation
tm add-tag experiment --copy-from-current

```

Tags prevent merge conflicts when multiple team members create tasks on different branches, and make it easy to context-switch between workstreams without losing track of progress.

## Optimize MCP Token Usage

If you use Taskmaster through an MCP-enabled editor, you can control how many tools are loaded to manage context window usage:

| Preset   | Tools Loaded | Token Cost | Best For             |
| -------- | ------------ | ---------- | -------------------- |
| core     | 7 essential  | \~5,000    | Daily development    |
| standard | 15 common    | \~10,000   | Balanced feature set |
| all      | 36 total     | \~21,000   | Full functionality   |

Configure this in your MCP settings:

```json
{
  "mcpServers": {
    "task-master-ai": {
      "env": {
        "TASK_MASTER_TOOLS": "standard"
      }
    }
  }
}

```

For long-running operations like PRD parsing or research, extend the MCP timeout:

```json
{
  "mcpServers": {
    "task-master-ai": {
      "timeout": 300
    }
  }
}

```

## Quick Tips

* Validate dependencies regularly — Run `tm validate-dependencies` to catch circular or missing dependencies before they block you
* Use `--research` liberally — Adding the `--research` flag to `expand`, `update`, and `analyze-complexity` pulls live information for better results
* Keep task details specific — The more actionable your task details, the better your AI assistant can help implement them
* Track status honestly — Mark tasks as `in-progress` when you start and `done` when you finish. This keeps `tm next` accurate
* Break down early — Expand complex tasks before you start implementing, not when you're stuck halfway through

## Next Steps

* [Advanced Tasks](https://tryhamster.com/docs/taskmaster/best-practices/advanced-tasks) — AI-driven development workflow, task reorganization, and merge conflict resolution
* [Advanced Configuration](https://tryhamster.com/docs/taskmaster/best-practices/configuration-advanced) — Config files, environment variables, and provider-specific setup

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Best Practices","item":"https://tryhamster.com/docs/taskmaster/best-practices"},{"@type":"ListItem","position":5,"name":"Index","item":"https://tryhamster.com/docs/taskmaster/best-practices/index"}]}
```
