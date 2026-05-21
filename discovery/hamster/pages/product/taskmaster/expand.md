---
description: AI breaks down high-level tasks into detailed implementation steps with context, file references, and clear acceptance criteria.
title: Task Expansion — Taskmaster | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

[Taskmaster](https://tryhamster.com/product/taskmaster)/Expand

# Complex tasks into actionable subtasks.

AI breaks down high-level tasks into detailed implementation steps. Each subtask includes context, file references, and clear acceptance criteria.

Expansion

## Expand any task

Pick a task by ID and let AI generate a full breakdown with implementation details, file references, and acceptance criteria. Use --research for Perplexity-backed context.

zsh — taskmaster

→tm expand --id=3 --research

Expanding task 3: "Payment integration"

Analyzed task requirements

Researched best practices

Generated 6 subtasks

Subtasks created:

3.1 - Set up Stripe SDK

3.2 - Create payment form component

3.3 - Implement checkout flow

3.4 - Handle webhook events

3.5 - Add error handling

3.6 - Write integration tests

Before & After

## Vague to specific

AI considers your codebase structure when generating subtasks — referencing real files, function names, and technical patterns for context-aware expansion.

Before

"Add user authentication"

Single vague task

After expansion

1.1 Install NextAuth.js

1.2 Configure auth providers

1.3 Create login/signup pages

1.4 Add session middleware

1.5 Protect API routes

Options

## Control the expansion

Fine-tune expansion output with flags for subtask count, research integration, prompt context, batch processing, and more.

`--num=N`Specify exactly how many subtasks to generate

`--research`Use Perplexity for research-backed expansion

`--force`Replace existing subtasks instead of appending

`--prompt="..."`Add context to guide the expansion

`--all`Expand all pending tasks at once

`tm expand-all`Batch expand multiple tasks

Key capabilities

* Context-aware subtask generation
* Implementation hints with file references
* Clear acceptance criteria per subtask
* Research-backed expansion with Perplexity
* Configurable subtask count
* Batch expansion for all pending tasks

Related features

[Complexity Analysis](https://tryhamster.com/product/taskmaster/complexity) — Know which tasks need expansion.

[Research](https://tryhamster.com/product/taskmaster/research) — Get context for complex expansions.

[Parse PRD](https://tryhamster.com/product/taskmaster/parse-prd) — Generate tasks to expand.

## Break down your first task.

Run `tm expand` and watch complexity dissolve.

[Get started](https://github.com/eyaltoledano/claude-task-master#readme)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Product","item":"https://tryhamster.com/product"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/product/taskmaster"},{"@type":"ListItem","position":4,"name":"Expand","item":"https://tryhamster.com/product/taskmaster/expand"}]}
```
