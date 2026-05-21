---
description: Prepare your environment for Taskmaster by installing prerequisites and configuring at least one model API key before running your first commands.
title: Requirements | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Requirements

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

# Requirements

Before you can start using TaskMaster AI, you'll need to install Node.js and set up at least one model API Key.

## 1\. Node.js

TaskMaster AI is built with Node.js and requires it to run. npm (Node Package Manager) comes bundled with Node.js.

### Install Node.js

#### Installation

**Option 1: Download from official website**

1. Visit [nodejs.org](https://nodejs.org)
2. Download the **LTS (Long Term Support)** version for your operating system
3. Run the installer and follow the setup wizard

**Option 2: Use a package manager**

**Windows (Chocolatey)**

```bash
choco install nodejs

```

**Windows (winget)**

```bash
winget install OpenJS.NodeJS

```

## 2\. Model API Key

TaskMaster utilizes AI across several commands, and those require a separate API key. For the purpose of a Quick Start we recommend setting up an API Key with Anthropic for your main model and Perplexity for your research model (optional but recommended).

> **Taskmaster shows API costs per command used. Most users load $5-10 on their keys and don't have to top it off for a few months.**

At least one (1) of the following is required:

1. Anthropic API key (Claude API) - **recommended for Quick Start**
2. OpenAI API key
3. Google Gemini API key
4. Perplexity API key (for research model)
5. xAI API Key (for research or main model)
6. OpenRouter API Key (for research or main model)
7. Claude Code (no API key required - requires Claude Code CLI)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Getting Started","item":"https://tryhamster.com/docs/taskmaster/getting-started"},{"@type":"ListItem","position":5,"name":"Quick Start","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start"},{"@type":"ListItem","position":6,"name":"Requirements","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start/requirements"}]}
```
