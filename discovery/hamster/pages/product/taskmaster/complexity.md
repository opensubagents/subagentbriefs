---
description: AI scores each task 1-10 for complexity and recommends which ones to expand. Stop guessing where the risk is.
title: Complexity Analysis — Taskmaster | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

[Taskmaster](https://tryhamster.com/product/taskmaster)/Complexity Analysis

# Know what needs to be broken down.

AI scores each task 1-10 for complexity and recommends which ones to expand. Stop guessing where the risk is — let AI tell you.

Scoring

## Find the risky tasks

Each task gets a score from 1 (trivial) to 10 (very complex) based on scope, dependencies, and unknowns. High-complexity tasks are flagged for expansion before they become blockers.

zsh — taskmaster

→tm analyze-complexity

Analyzing 5 tasks...

1.

Setup repo structure

2

2.

Implement OAuth

7

3.

Build payment system

9

4.

Add user dashboard

5

5.

Write unit tests

3

⚠️ Recommend expansion: Tasks 2, 3 (complexity ≥ 7)

Interpretation

## What the scores mean

Scores map to clear action guidance. Low scores are safe to execute as-is, medium scores can optionally be expanded, and high scores should always be broken down before implementation.

Low (1-3)

Straightforward tasks. Clear scope, minimal dependencies. Safe to execute as-is.

Medium (4-6)

Some complexity. Consider expanding if you want more granular progress tracking.

High (7-10)

Significant complexity or unknowns. Strongly recommended for expansion before execution.

Workflow

## From analysis to action

Run complexity analysis to identify risky tasks, then expand the flagged ones into manageable subtasks. Two commands to go from uncertainty to a clear plan.

zsh — taskmaster

→tm analyze-complexity --research

Analyzing 12 tasks...

⚠️ 2 tasks recommended for expansion (score ≥ 7)

→tm expand --id=3 --research

✓ Generated 6 subtasks for task 3

Key capabilities

* Score tasks 1-10 based on implementation complexity
* Flag tasks that need expansion before execution
* Research-backed analysis with --research flag
* Generate full complexity reports
* Recommend specific expansion thresholds
* Works alongside parse-prd and expand commands

Related features

[Task Expansion](https://tryhamster.com/product/taskmaster/expand) — Break down complex tasks into subtasks.

[Parse PRD](https://tryhamster.com/product/taskmaster/parse-prd) — Generate the tasks to analyze.

[Research](https://tryhamster.com/product/taskmaster/research) — Get more info on complex areas.

## Analyze your task complexity.

Run `tm analyze-complexity` before you start coding.

[Get started](https://github.com/eyaltoledano/claude-task-master#readme)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Product","item":"https://tryhamster.com/product"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/product/taskmaster"},{"@type":"ListItem","position":4,"name":"Complexity","item":"https://tryhamster.com/product/taskmaster/complexity"}]}
```
