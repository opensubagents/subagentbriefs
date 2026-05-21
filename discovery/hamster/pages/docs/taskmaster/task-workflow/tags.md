---
description: Organize tasks into separate workstreams with tags for parallel feature development. Learn how Hamster helps teams plan, build, and ship software...
title: Tags in Taskmaster — Task Workflow Guide | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Tags

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

# Organizing Work with Tags

Tags let you split your project into independent workstreams. Each tag gets its own task list, so you can work on `feature-auth`, `feature-payments`, and `bugfixes` without them interfering with each other.

## Creating Tags

```bash
# Create a new tag
tm add-tag feature-auth

# Create a tag from your current Git branch name
tm add-tag --from-branch feature/auth

```

## Switching Between Tags

```bash
# Switch to a tag — all commands now operate on this tag's tasks
tm use-tag feature-auth

# List all tags with progress stats
tm tags

```

The `tm tags` output shows task counts, completion percentage, and how many tasks are ready to work on for each tag.

## Managing Tags

```bash
# Rename a tag
tm rename-tag old-name new-name

# Copy all tasks from one tag to another
tm copy-tag source-tag destination-tag

# Delete a tag
tm delete-tag feature-auth

```

## Moving Tasks Between Tags

When priorities shift, move tasks between workstreams without losing context:

```bash
# Move task 5 from backlog to the active feature tag
tm move --from=5 --from-tag=backlog --to-tag=feature-1

# Move a task and pull its dependencies along
tm move --from=5 --from-tag=backlog --to-tag=feature-1 --with-dependencies

# Move multiple tasks at once
tm move --from=5,6,7 --from-tag=backlog --to-tag=feature-1

```

If a task ID already exists in the destination tag, Taskmaster will suggest how to resolve the conflict.

## Filtering Across Tags

See the full picture across all your workstreams:

```bash
# List ready tasks across every tag
tm list --ready --all-tags

# List all tags that have work available
tm tags --ready

```

## How Tags Work

Each tag stores its tasks in a separate file (`tasks.json` for the default tag, `tasks_feature-auth.json` for named tags). Complexity reports are also tag-specific, so analysis stays relevant to each workstream.

Tags are ideal for:

* Parallel feature development — Work on multiple features without task ID conflicts
* Sprint planning — Create a tag per sprint and move tasks in
* Bug triage — Separate bugs from feature work
* Team coordination — Different team members work on different tags

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Task Workflow","item":"https://tryhamster.com/docs/taskmaster/task-workflow"},{"@type":"ListItem","position":5,"name":"Tags","item":"https://tryhamster.com/docs/taskmaster/task-workflow/tags"}]}
```
