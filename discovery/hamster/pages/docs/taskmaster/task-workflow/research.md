---
description: Query live web sources from your terminal for current best practices, security patches, and library updates. Learn how Hamster helps teams plan, build,...
title: Research | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Research

* Welcome  
   * [Introduction](https://tryhamster.com/docs/taskmaster "Introduction")

* Getting Started

* Task Workflow  
   * [Tags](https://tryhamster.com/docs/taskmaster/task-workflow/tags "Tags")  
   * [Dependencies](https://tryhamster.com/docs/taskmaster/task-workflow/dependencies "Dependencies")  
   * [Research](https://tryhamster.com/docs/taskmaster/task-workflow/research "Research")  
   * [Scope Adjustment](https://tryhamster.com/docs/taskmaster/task-workflow/scope-adjustment "Scope Adjustment")

* Automation

* AI Providers

* IDE & Editor Setup

* Team Collaboration

* Best Practices

* TDD Workflow

* Technical Capabilities

# Research

AI models have knowledge cutoffs. The research command queries live web sources and returns current answers with citations, so your tasks are informed by the latest information — not stale training data.

## Running a Research Query

```bash
# Ask any question — get a current, cited answer
tm research "best practices for Next.js 15 server actions"

# Research with a specific topic
tm research "Stripe webhook verification Node.js 2025"

```

Research is powered by your configured research model (typically Perplexity Sonar), which searches the live web and returns answers with source citations.

## Saving Research to Tasks

Don't let findings get lost in terminal history. Save research directly to a task:

```bash
# Save findings to subtask 3.4
tm research "Stripe webhook verification" --save-to=3.4

```

The research output is appended to the task's details, so context travels with the work.

## Research-Enhanced Commands

Several Taskmaster commands can use research for better results:

```bash
# Complexity analysis with research — scoring informed by current best practices
tm analyze-complexity --research

# Task expansion with research — subtasks based on latest patterns
tm expand --id=5 --research

# Update a task with research-backed context
tm update-task --id=5 --prompt="update for latest API changes" --research

```

## When to Use Research

* Before implementing tasks — Verify current best practices for your tech stack
* Working with unfamiliar libraries — Get up-to-date implementation guidance
* Security-related work — Find latest security recommendations and known issues
* Dependency updates — Research breaking changes and migration guides
* Performance optimization — Get current performance best practices
* Debugging complex issues — Search for known solutions and workarounds

## Configuring the Research Model

```bash
# See current research model
tm models

# Switch to a different research model
tm models --set-research sonar-deep-research

# Use interactive setup
tm models --setup

```

The research model defaults to Perplexity Sonar. You can switch to Perplexity Sonar Deep Research for more thorough answers, or any other provider that supports internet-connected queries.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Task Workflow","item":"https://tryhamster.com/docs/taskmaster/task-workflow"},{"@type":"ListItem","position":5,"name":"Research","item":"https://tryhamster.com/docs/taskmaster/task-workflow/research"}]}
```
