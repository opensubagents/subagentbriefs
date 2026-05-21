---
description: Run Claude Code in an automated loop that picks up tasks, implements them, and moves to the next one. Learn how Hamster helps teams plan, build, and...
title: Loop Command | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Loop Command

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

# Loop Command

The `loop` command runs Claude Code in an automated cycle — it picks the next available task, implements it, marks it done, and moves on. You can step away and come back to completed work.

## Usage

```bash
# Start the automated loop
tm loop

# Watch Claude's work in real-time
tm loop --verbose

# Run in a Docker sandbox for isolation
tm loop --sandbox

```

## How It Works

Each iteration of the loop:

1. Finds the next task respecting dependencies and priorities
2. Builds a prompt with full task context
3. Launches Claude Code to implement the task
4. Waits for completion (detected via structured markers)
5. Moves to the next available task
6. Stops when all tasks are done or a task is blocked

Progress is tracked in `.taskmaster/loop-progress.txt` so you can monitor status.

## Presets

Presets configure the loop for different development workflows:

```bash
# Default preset — standard task execution
tm loop

# TDD preset — enforce test-driven development
tm loop --preset test-coverage

# Linting preset — enforce code quality checks
tm loop --preset linting

# Duplication preset — check for code duplication
tm loop --preset duplication

```

| Preset        | Focus                        |
| ------------- | ---------------------------- |
| default       | Standard task execution      |
| test-coverage | Enforce tests with each task |
| linting       | Run linting after each task  |
| duplication   | Check for duplicate code     |
| entropy       | Minimize code complexity     |

## Options

| Flag             | Description                         |
| ---------------- | ----------------------------------- |
| \--verbose / \-v | Show Claude's real-time output      |
| \--no-output     | Exclude full output to save memory  |
| \--sandbox       | Run in Docker sandbox for isolation |
| \--preset <name> | Use a specific workflow preset      |

## Loop vs Start vs Clusters

| Command           | Best for                                    |
| ----------------- | ------------------------------------------- |
| tm start          | Single task, hands-on implementation        |
| tm loop           | Sequential automation, step away and return |
| tm clusters start | Parallel automation with agent teams        |

## Tips

* Use `--verbose` the first few times to build confidence in what the loop is doing
* The loop respects your dependency graph — it won't skip ahead
* If a task gets blocked, the loop stops and reports why
* You can interrupt with Ctrl+C and resume later — progress is saved

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Automation","item":"https://tryhamster.com/docs/taskmaster/automation"},{"@type":"ListItem","position":5,"name":"Loop","item":"https://tryhamster.com/docs/taskmaster/automation/loop"}]}
```
