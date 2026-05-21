---
description: Now that your tasks are generated and reviewed you are ready to begin executing. Learn how Hamster helps teams plan, build, and ship software faster...
title: Executing Tasks | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Executing Tasks

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

# Executing Tasks

Now that your tasks are generated and reviewed you are ready to begin executing.

## Select the Task to Work on: Next Task

Taskmaster has the "next" command to find the next task to work on. You can access it with the following request:

```
What's the next task I should work on? Please consider dependencies and priorities.

```

Alternatively you can use the CLI to show the next task

```bash
task-master next

```

## Discuss Task

When you know what task to work on next you can then start chatting with the agent to make sure it understands the plan of action.

You can tag relevant files and folders so it knows what context to pull up as it generates its plan. For example:

```
Please review Task 5 and confirm you understand how to execute before beginning. Refer to @models @api and @schema 

```

The agent will begin analyzing the task and files and respond with the steps to complete the task.

## Agent Task execution

If you agree with the plan of action, tell the agent to get started.

```
You may begin. I believe in you.

```

## Review and Test

Once the agent is finished with the task you can refer to the task testing strategy to make sure it was completed correctly.

## Update Task Status

If the task was completed correctly you can update the status to done

```
Please mark Task 5 as done

```

The agent will execute

```bash
task-master set-status --id=5 --status=done

```

## Rules and Context

If you ran into problems and had to debug errors you can create new rules as you go. This helps build context on your codebase that helps the creation and execution of future tasks.

## On to the Next Task!

By now you have all you need to get started executing code faster and smarter with Taskmaster.

If you have any questions please check out [Frequently Asked Questions](https://tryhamster.com/docs/taskmaster/getting-started/faq)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Getting Started","item":"https://tryhamster.com/docs/taskmaster/getting-started"},{"@type":"ListItem","position":5,"name":"Quick Start","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start"},{"@type":"ListItem","position":6,"name":"Execute Quick","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start/execute-quick"}]}
```
