---
description: Launch your AI coding agent with full task context in a single command. Learn how Hamster helps teams plan, build, and ship software faster with AI...
title: Start Command | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Start Command

* Welcome  
   * [Introduction](https://tryhamster.com/docs/taskmaster "Introduction")

* Getting Started

* Task Workflow

* Automation  
   * [Start Command](https://tryhamster.com/docs/taskmaster/automation/start "Start Command")  
   * [Loop Command](https://tryhamster.com/docs/taskmaster/automation/loop "Loop Command")

* AI Providers

* IDE & Editor Setup

* Team Collaboration

* Best Practices

* TDD Workflow

* Technical Capabilities

# Start Command

The `start` command bridges task planning and implementation. It launches your AI coding agent (Claude Code) with the full context of a specific task — details, dependencies, test strategy, and project context — so the agent can begin implementing immediately.

## Usage

```bash
# Start working on a specific task
tm start 5

# Auto-detect the next available task
tm start

```

## What Happens

When you run `tm start`:

1. Taskmaster loads the task's full context — title, description, implementation details, test strategy
2. It checks which dependencies have been completed and includes that context
3. It builds a comprehensive prompt with everything the agent needs
4. It launches Claude Code with the prompt pre-loaded
5. The task status is automatically set to `in-progress`

This means the AI agent starts with full awareness of what to build, what's already done, and how to verify the work — no copy-pasting task details into chat.

## When to Use Start

The `start` command is best for **focused, single-task implementation**. Use it when:

* You want to hand off a well-defined task to the AI agent
* You want the agent to have full task context without manual setup
* You're working through tasks one at a time

For automated multi-task execution, see the [Loop command](https://tryhamster.com/docs/taskmaster/automation/loop) or [Clusters](https://tryhamster.com/docs/taskmaster/capabilities/clusters).

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Automation","item":"https://tryhamster.com/docs/taskmaster/automation"},{"@type":"ListItem","position":5,"name":"Start","item":"https://tryhamster.com/docs/taskmaster/automation/start"}]}
```
