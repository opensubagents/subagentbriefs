---
description: Define task ordering with dependencies so work happens in the right sequence. Learn how Hamster helps teams plan, build, and ship software faster with...
title: Dependencies | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Dependencies

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

# Managing Dependencies

Dependencies define the order work should happen in. When task 5 depends on task 3, Taskmaster ensures task 3 is completed before recommending task 5.

## Adding Dependencies

```bash
# Task 5 depends on task 3 — task 3 must be done first
tm add-dependency --id=5 --depends-on=3

# Remove a dependency
tm remove-dependency --id=5 --depends-on=3

```

## How Dependencies Affect Your Workflow

Dependencies power several Taskmaster features:

* **`tm next`** only recommends tasks whose dependencies are all satisfied
* **`tm list --ready`** filters to tasks that are unblocked and ready to start
* **`tm list --blocking`** shows tasks that other tasks are waiting on
* **`tm clusters`** groups tasks by dependency level for parallel execution

## Finding High-Impact Work

The `--ready` and `--blocking` filters help you focus on what matters:

```bash
# Tasks you can start right now (all dependencies met)
tm list --ready

# Tasks that are holding up other work
tm list --blocking

# The sweet spot — tasks you can start that also unblock others
tm list --ready --blocking

```

## Validating Dependencies

Check your dependency graph for problems:

```bash
# Check for circular dependencies or references to missing tasks
tm validate-dependencies

# Automatically fix invalid dependencies
tm fix-dependencies

```

## Dependency Resolution Rules

* A dependency is satisfied when its task status is `done` or `cancelled`
* Dependencies work across tags — task 5 in `feature-auth` can depend on task 3 in `core`
* When you mark a parent task as `done`, all its subtasks are automatically marked `done` too
* The `tm next` command walks the full dependency graph to find the highest-priority unblocked task

## Best Practices

1. Set dependencies during PRD parsing — A well-structured PRD generates tasks with proper ordering automatically
2. Validate periodically — Run `tm validate-dependencies` after reorganizing tasks
3. Use `--ready --blocking` — This combo surfaces the most impactful work
4. Don't over-depend — Only add dependencies where there's a genuine ordering requirement

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Task Workflow","item":"https://tryhamster.com/docs/taskmaster/task-workflow"},{"@type":"ListItem","position":5,"name":"Dependencies","item":"https://tryhamster.com/docs/taskmaster/task-workflow/dependencies"}]}
```
