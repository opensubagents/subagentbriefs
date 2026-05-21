---
description: Writing a PRD (Product Requirements Document) is the starting point of every task flow in Taskmaster. Learn how Hamster helps teams plan, build, and...
title: PRD Creation and Parsing | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

PRD Creation and Parsing

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

# Writing a PRD

A PRD (Product Requirements Document) is the starting point of every task flow in Taskmaster. It defines what you're building and why. A clear PRD dramatically improves the quality of your tasks, your model outputs, and your final product — so it's worth taking the time to get it right.

> **You don't need to define your whole app up front. You can write a focused PRD just for the next feature or module you're working on.**

> **You can start with an empty project or you can start with a feature PRD on an existing project.**

> **You can add and parse multiple PRDs per project using the --append flag**

## What Makes a Good PRD?

* Clear objective — what’s the outcome or feature?
* Context — what’s already in place or assumed?
* Constraints — what limits or requirements need to be respected?
* Reasoning — why are you building it this way?

The more context you give the model, the better the breakdown and results.

## Writing a PRD for Taskmaster

> **An example PRD can be found in .taskmaster/templates/example\_prd.txt**

You can co-write your PRD with an LLM model using the following workflow:

1. Chat about requirements — explain what you want to build.
2. Show an example PRD — share the example PRD so the model understands the expected format. The example uses formatting that work well with Taskmaster's code. Following the example will yield better results.
3. Iterate and refine — work with the model to shape the draft into a clear and well-structured PRD.

This approach works great in Cursor, or anywhere you use a chat-based LLM.

## Where to Save Your PRD

Place your PRD file in the `.taskmaster/docs` folder in your project.

* You can have **multiple PRDs** per project.
* Name your PRDs clearly so they’re easy to reference later.  
   * Examples: `dashboard_redesign.txt`, `user_onboarding.txt`

## Parse your PRD into Tasks

This is where the Taskmaster magic begins.

In Cursor's AI chat, instruct the agent to generate tasks from your PRD:

```
Please use the task-master parse-prd command to generate tasks from my PRD. The PRD is located at .taskmaster/docs/<prd-name>.txt.

```

The agent will execute the following command which you can alternatively paste into the CLI:

```bash
task-master parse-prd --input .taskmaster/docs/<prd-name>.txt

```

This will:

* Parse your PRD document
* Generate a structured `tasks.json` file with tasks, dependencies, priorities, and test strategies

Now that you have written and parsed a PRD, you are ready to start setting up your tasks.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Getting Started","item":"https://tryhamster.com/docs/taskmaster/getting-started"},{"@type":"ListItem","position":5,"name":"Quick Start","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start"},{"@type":"ListItem","position":6,"name":"Prd Quick","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start/prd-quick"}]}
```
