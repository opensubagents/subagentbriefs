---
description: Frequently asked questions about Taskmaster. Learn how Hamster helps teams plan, build, and ship software faster with AI agents and clear execution...
title: Taskmaster FAQ — Getting Started Guide | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

FAQ

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

# FAQ

## General

### What is Taskmaster?

Taskmaster is an AI-powered task management system for developers. It breaks down projects into structured tasks, manages dependencies, and integrates with your AI coding assistant to execute work systematically.

### Is Taskmaster free?

Yes. Taskmaster is open-source under the MIT License with Commons Clause. You can use it freely for personal and commercial projects. The only restriction is you cannot sell Taskmaster itself as a service.

### What AI providers does Taskmaster support?

Taskmaster works with 15+ providers including Anthropic, OpenAI, Google, Perplexity, xAI, Groq, OpenRouter, Ollama, LM Studio, and more. See [AI Providers](https://tryhamster.com/docs/taskmaster/ai-providers/overview) for the full list.

### Can I use Taskmaster without an API key?

Yes. You can use CLI-based providers like Claude Code (with your subscription) or Gemini CLI (with a free Google account). You can also run fully offline with Ollama or LM Studio. See [Local Models](https://tryhamster.com/docs/taskmaster/ai-providers/local-models).

## Setup

### Which editors does Taskmaster work with?

Taskmaster integrates with 13+ editors including Cursor, Claude Code, VS Code, Windsurf, Roo, Cline, Zed, Kiro, and more. See [Supported Editors](https://tryhamster.com/docs/taskmaster/ide-setup/supported-editors).

### How do I set up Taskmaster for my editor?

Run `tm rules add -y` to auto-detect your editor, or `tm rules add cursor` (replace with your editor) for a specific setup. See [Installation](https://tryhamster.com/docs/taskmaster/getting-started/quick-start/installation).

### Can I use Taskmaster in a monorepo?

Yes. Taskmaster auto-detects monorepo setups via `lerna.json`, `nx.json`, or `turbo.json` and adjusts configuration accordingly.

## Tasks

### What is a PRD?

A PRD (Product Requirements Document) is a text file describing what you want to build. Taskmaster parses it and generates a structured task plan with dependencies. See [PRD Creation](https://tryhamster.com/docs/taskmaster/getting-started/quick-start/prd-quick).

### How do I organize work across multiple features?

Use tags. Each tag gets its own independent task list. See [Tags](https://tryhamster.com/docs/taskmaster/task-workflow/tags).

### Can I move tasks between features?

Yes. Use `tm move --from=5 --from-tag=backlog --to-tag=feature-1` to move tasks between tags. See [Tags](https://tryhamster.com/docs/taskmaster/task-workflow/tags).

### What is task expansion?

Expansion breaks a high-level task into actionable subtasks. For example, "Build user authentication" might expand into subtasks for OAuth setup, session management, password hashing, etc. The complexity analysis command helps determine how many subtasks each task needs.

## Automation

### Can Taskmaster run tasks automatically?

Yes. The `tm loop` command runs tasks in an automated cycle — it picks the next task, implements it, and moves on. See [Loop Command](https://tryhamster.com/docs/taskmaster/automation/loop).

### What are clusters?

Clusters are groups of tasks that can run in parallel. The `tm clusters start` command launches multiple AI agents to work on independent task groups simultaneously. See [Clusters](https://tryhamster.com/docs/taskmaster/capabilities/clusters).

## Team

### Can I collaborate with my team?

Yes. Taskmaster's team mode connects to Hamster for cloud storage, real-time sync, and shared task management. See [Team Collaboration](https://tryhamster.com/docs/taskmaster/team/overview).

### Do my teammates need API keys?

No. In team mode, Hamster handles all AI inference. Individual team members don't need their own API keys.

## Getting Help

* **Discord**: [Join our community](https://discord.gg/taskmasterai)
* **Issues**: [GitHub Issues](https://github.com/eyaltoledano/claude-task-master/issues)
* **Discussions**: [GitHub Discussions](https://github.com/eyaltoledano/claude-task-master/discussions)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Getting Started","item":"https://tryhamster.com/docs/taskmaster/getting-started"},{"@type":"ListItem","position":5,"name":"FAQ","item":"https://tryhamster.com/docs/taskmaster/getting-started/faq"}]}
```
