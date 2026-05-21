---
description: Increase or decrease task complexity with scope-up and scope-down commands. Learn how Hamster helps teams plan, build, and ship software faster with AI...
title: Scope Adjustment | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Scope Adjustment

* Welcome  
   * [Introduction](https://tryhamster.com/docs/taskmaster "Introduction")

* Getting Started

* Task Workflow  
   * [Tags](https://tryhamster.com/docs/taskmaster/task-workflow/tags "Tags")  
   * [Dependencies](https://tryhamster.com/docs/taskmaster/task-workflow/dependencies "Dependencies")  
   * [Research](https://tryhamster.com/docs/taskmaster/task-workflow/research "Research")  
   * [Scope Adjustment](https://tryhamster.com/docs/taskmaster/task-workflow/scope-adjustment "Scope Adjustment")

* Automation

* AI Providers

* IDE & Editor Setup

* Team Collaboration

* Best Practices

* TDD Workflow

* Technical Capabilities

# Adjusting Task Scope

Sometimes a task is too ambitious for the current phase, or too simple and needs more depth. The `scope-up` and `scope-down` commands let you adjust task complexity without starting from scratch.

## Reducing Scope

When a task is too complex for the current milestone, scope it down to focus on the essentials:

```bash
# Simplify task 5 — focus on core functionality
tm scope-down --id=5

# Light simplification
tm scope-down --id=5 --strength=light

# Aggressive simplification
tm scope-down --id=5 --strength=heavy

# Scope down multiple tasks at once
tm scope-down --id=10,11,12

```

Scoping down preserves the original intent while removing non-essential requirements. The AI considers what can be deferred to a future iteration.

## Increasing Scope

When a task needs more depth or additional requirements:

```bash
# Add more detail and requirements to task 5
tm scope-up --id=5

# Light enhancement
tm scope-up --id=5 --strength=light

# Significant enhancement
tm scope-up --id=5 --strength=heavy

```

Scoping up adds implementation detail, edge cases, validation requirements, or related functionality that strengthens the task.

## Strength Levels

| Level   | Effect                                                    |
| ------- | --------------------------------------------------------- |
| light   | Minor adjustments — trim or add small details             |
| regular | Moderate changes — meaningful scope changes (default)     |
| heavy   | Major changes — significantly simplify or expand the task |

## Custom Direction

Guide the AI on exactly how to adjust scope:

```bash
# Scope down with specific direction
tm scope-down --id=5 --prompt="Remove OAuth integration, use simple API key auth instead"

# Scope up with specific requirements
tm scope-up --id=5 --prompt="Add rate limiting and request validation"

```

## When to Use Scope Adjustment

* Phase planning — Scope down tasks for an MVP, scope up for v2
* Sprint fitting — Adjust tasks to fit available time
* Iterative refinement — Start simple, then scope up as you learn more
* Team coordination — Scope down for junior developers, scope up for senior ones
* Milestone alignment — Match task complexity to project milestones

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Task Workflow","item":"https://tryhamster.com/docs/taskmaster/task-workflow"},{"@type":"ListItem","position":5,"name":"Scope Adjustment","item":"https://tryhamster.com/docs/taskmaster/task-workflow/scope-adjustment"}]}
```
