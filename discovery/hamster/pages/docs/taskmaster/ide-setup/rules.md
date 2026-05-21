---
description: How Taskmaster rules teach your AI coding assistant to manage tasks effectively. Learn how Hamster helps teams plan, build, and ship software faster...
title: Rules System | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Rules System

* Welcome  
   * [Introduction](https://tryhamster.com/docs/taskmaster "Introduction")

* Getting Started

* Task Workflow

* Automation

* AI Providers

* IDE & Editor Setup  
   * [Supported Editors](https://tryhamster.com/docs/taskmaster/ide-setup/supported-editors "Supported Editors")  
   * [Rules System](https://tryhamster.com/docs/taskmaster/ide-setup/rules "Rules System")

* Team Collaboration

* Best Practices

* TDD Workflow

* Technical Capabilities

# Rules System

Rules are instruction files that teach your AI coding assistant how to use Taskmaster. When rules are installed, your assistant knows how to list tasks, check dependencies, expand work, update status, and follow the right workflow — without you having to explain it every time.

## What Rules Do

A Taskmaster rules file tells your AI assistant:

* How to discover work — Use `tm next` or `tm list --ready` to find available tasks
* How to implement tasks — Read task details, check dependencies, follow the test strategy
* How to track progress — Update task status, append implementation notes to subtasks
* When to expand — Use `tm analyze-complexity` and `tm expand` for complex tasks
* How to handle drift — Use `tm update` when implementation diverges from the plan

## Installing Rules

```bash
# Auto-detect your editor and install
tm rules add -y

# Install for a specific editor
tm rules add cursor

# Guided interactive setup
tm rules setup

```

## How Rules Differ by Editor

Each editor has its own rules format and location:

* **Cursor** uses `.mdc` files in `.cursor/rules/` with frontmatter for rule descriptions
* **Claude Code** uses markdown imports in `CLAUDE.md` pointing to `.taskmaster/CLAUDE.md`
* **VS Code** uses `.github/copilot-instructions.md` for Copilot Chat
* **Windsurf** uses a single `.windsurfrules` file in the project root

The content is functionally identical across editors — only the format and file location change.

## Updating Rules

When you update Taskmaster, re-run the rules command to get the latest instructions:

```bash
tm rules add cursor

```

This updates the rules file with new commands and best practices from the latest version.

## Custom Instructions

Rules don't overwrite your existing editor configuration. For Claude Code, Taskmaster creates `.taskmaster/CLAUDE.md` and adds an import line to your main `CLAUDE.md` — your custom instructions remain untouched.

## Monorepo Support

Taskmaster auto-detects monorepo setups (via `lerna.json`, `nx.json`, or `turbo.json`) and adjusts rules placement accordingly.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Ide Setup","item":"https://tryhamster.com/docs/taskmaster/ide-setup"},{"@type":"ListItem","position":5,"name":"Rules","item":"https://tryhamster.com/docs/taskmaster/ide-setup/rules"}]}
```
