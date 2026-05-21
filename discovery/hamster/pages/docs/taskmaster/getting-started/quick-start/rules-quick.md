---
description: Set up IDE rules so your AI assistant knows how to use Taskmaster automatically. Learn how Hamster helps teams plan, build, and ship software faster...
title: Rules and Context | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Rules and Context

* Welcome  
   * [Introduction](https://tryhamster.com/docs/taskmaster "Introduction")

* Getting Started  
   * [Overview](https://tryhamster.com/docs/taskmaster/getting-started "Overview")  
   * [Quick Start](https://tryhamster.com/docs/taskmaster/getting-started/quick-start/quick-start "Quick Start")  
   * [API Keys](https://tryhamster.com/docs/taskmaster/getting-started/api-keys "API Keys")  
   * [FAQ](https://tryhamster.com/docs/taskmaster/getting-started/faq "FAQ")  
   * [Contribute](https://tryhamster.com/docs/taskmaster/getting-started/contribute "Contribute")

* Task Workflow

* Automation

* AI Providers

* IDE & Editor Setup

* Team Collaboration

* Best Practices

* TDD Workflow

* Technical Capabilities

# Rules and Context

Rules are instruction files that teach your AI coding assistant how to use Taskmaster. Once installed, your assistant automatically knows how to find tasks, check dependencies, implement work, and update progress.

## Setting Up Rules

```bash
# Auto-detect your editor and install rules
tm rules add -y

# Or specify your editor
tm rules add cursor
tm rules add claude

# Multiple editors at once
tm rules add cursor,claude,windsurf

```

That's it. Your AI assistant now knows how to use every Taskmaster command in context.

## What Rules Teach Your Assistant

With rules installed, your AI assistant can:

* Find the next task — Runs `tm next` to identify work respecting dependencies and priorities
* Read task context — Uses `tm show` to understand implementation details and test strategy
* Track progress — Updates task status and appends implementation notes to subtasks
* Handle changes — Uses `tm update` when implementation diverges from the plan
* Break down work — Uses `tm expand` to split complex tasks into subtasks

## Building Context Over Time

As you work, build project-specific context by adding rules to your editor's rule files:

* Coding standards — Patterns, conventions, and naming rules specific to your project
* Architecture decisions — Key decisions that affect how tasks should be implemented
* Common pitfalls — Issues you've encountered and how to avoid them

This context improves every future task your AI assistant works on.

## Next Steps

For the full rules reference including all 13+ supported editors, see [Supported Editors](https://tryhamster.com/docs/taskmaster/ide-setup/supported-editors) and [Rules System](https://tryhamster.com/docs/taskmaster/ide-setup/rules).

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Getting Started","item":"https://tryhamster.com/docs/taskmaster/getting-started"},{"@type":"ListItem","position":5,"name":"Quick Start","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start"},{"@type":"ListItem","position":6,"name":"Rules Quick","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start/rules-quick"}]}
```
