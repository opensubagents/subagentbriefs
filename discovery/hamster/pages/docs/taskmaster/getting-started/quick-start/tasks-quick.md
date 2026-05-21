---
description: Review the plan and prepare for execution. Learn how Hamster helps teams plan, build, and ship software faster with AI agents and clear execution...
title: Tasks Setup | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Tasks Setup

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

# Tasks Setup

Now that your tasks are generated you can review the plan and prepare for execution.

> **Not all of the setup steps are required but they are recommended in order to ensure your coding agents work on accurate tasks.**

## Expand Tasks

Used to add detail to tasks and create subtasks. We recommend expanding all tasks using the MCP request below:

```
Expand all tasks into subtasks.

```

The agent will execute

```bash
task-master expand --all

```

## List/Show Tasks

Used to view task details. It is important to review the plan and ensure it makes sense in your project. Check for correct folder structures, dependencies, out of scope subtasks, etc.

To see a list of tasks and descriptions use the following command:

```
List all pending tasks so I can review.

```

To see all tasks in the CLI you can use:

```bash
task-master list

```

To see all implementation details of an individual task, including subtasks and testing strategy, you can use Show Task:

```
Show task 2 so I can review.

```

```bash
task-master show --id=<##>

```

## Update Tasks

If the task details need to be edited you can update the task using this request:

```
Update Task 2 to use Postgres instead of MongoDB and remove the sharding subtask

```

Or this CLI command:

```bash
task-master update-task --id=2 --prompt="use Postgres instead of MongoDB and remove the sharding subtask"

```

## Analyze complexity

Taskmaster can provide a complexity report which can be helpful to read before you begin. If you didn't already expand all your tasks, it could help identify which could be broken down further with subtasks.

```
Can you analyze the complexity of our tasks to help me understand which ones need to be broken down further?

```

The agent will use the `analyze_project_complexity` MCP tool, or you can run it directly with the CLI command:

```bash
task-master analyze-complexity

```

For more comprehensive analysis using your configured research model, you can use:

```bash
task-master analyze-complexity --research

```

> **The `--research` flag uses whatever research model you have configured in `.taskmaster/config.json` (configurable via `task-master models --setup`) for research-backed complexity analysis, providing more informed recommendations.**

You can view the report in a friendly table using:

```
Can you show me the complexity report in a more readable format?

```

For more detailed CLI options, see the [Analyze Task Complexity](https://tryhamster.com/docs/taskmaster/capabilities/cli-root-commands#analyze-task-complexity) section.

Now you are ready to begin [executing tasks](https://tryhamster.com/docs/taskmaster/getting-started/quick-start/execute-quick)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Getting Started","item":"https://tryhamster.com/docs/taskmaster/getting-started"},{"@type":"ListItem","position":5,"name":"Quick Start","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start"},{"@type":"ListItem","position":6,"name":"Tasks Quick","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start/tasks-quick"}]}
```
