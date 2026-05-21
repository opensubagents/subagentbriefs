---
description: Export your local task plan to a collaborative Hamster brief for team collaboration. Learn how Hamster helps teams plan, build, and ship software...
title: Exporting Tasks | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Exporting Tasks

* Welcome  
   * [Introduction](https://tryhamster.com/docs/taskmaster "Introduction")

* Getting Started

* Task Workflow

* Automation

* AI Providers

* IDE & Editor Setup

* Team Collaboration  
   * [Overview](https://tryhamster.com/docs/taskmaster/team/overview "Overview")  
   * [Exporting Tasks](https://tryhamster.com/docs/taskmaster/team/exporting-tasks "Exporting Tasks")

* Best Practices

* TDD Workflow

* Technical Capabilities

# Exporting Tasks to Hamster

The `export` command takes your local task plan and creates a collaborative brief on Hamster. This is how you go from solo development to team collaboration.

## Usage

```bash
tm export

```

The command walks you through:

1. Tag selection — Choose which tags to export (multi-select supported)
2. Authentication — OAuth login if not already authenticated
3. Brief creation — Hamster generates a brief with auto-generated title and description
4. Team invitations — Optionally invite team members
5. Context switch — Your CLI context automatically switches to the new brief

## Inviting Team Members

```bash
# Export and invite teammates in one step
tm export --invite

```

You can invite up to 10 team members by email during export. The terminal shows invitation status and a clickable invite URL for sharing.

## What Hamster Does

When you export, Hamster:

* Reverse-engineers a PRD from your task list
* Generates brief titles and descriptions from task content
* Imports all tasks across your selected tags
* Handles all AI inference — your teammates don't need their own API keys

## PRD to Hamster

You can also send a PRD directly to Hamster instead of parsing it locally:

```bash
tm parse-prd my-prd.txt
# Select "Bring to Hamster" when prompted

```

Hamster creates a collaborative brief from your PRD content, generates tasks, and optionally invites your team — all in one step.

## After Exporting

Once exported, you can immediately start working in team mode:

```bash
# See your exported tasks
tm list

# Find the next task
tm next

# Watch for team changes in real-time
tm list --watch

```

Already-exported tags are disabled in the export selector to prevent duplicate exports.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Team","item":"https://tryhamster.com/docs/taskmaster/team"},{"@type":"ListItem","position":5,"name":"Exporting Tasks","item":"https://tryhamster.com/docs/taskmaster/team/exporting-tasks"}]}
```
