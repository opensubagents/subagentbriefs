---
description: Work on tasks together with real-time sync, cloud storage, and team invitations via Hamster. Learn how Hamster helps teams plan, build, and ship...
title: Team Collaboration | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Overview

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

# Team Collaboration

Taskmaster has two operating modes: **solo** and **team**. Solo mode stores tasks locally in your project. Team mode connects to [Hamster](https://tryhamster.com) for cloud storage, real-time sync, and collaboration across your team.

## Getting Started with Team Mode

```bash
# Log in to Hamster
tm login

# Initialize a project in team mode
tm init
# Select "Together" when prompted for workflow

```

Once connected, your tasks are stored in the cloud and synced in real-time across all team members.

## What Team Mode Provides

* Cloud storage — Tasks live on Hamster's servers, accessible from any machine
* Real-time sync — Changes appear instantly for all team members
* AI inference — Hamster handles all AI calls, so individual team members don't need their own API keys
* Brief management — Tasks are organized into collaborative briefs
* Team invitations — Invite up to 10 team members by email

## Working with Briefs

In team mode, tasks are organized into briefs — collaborative workspaces on Hamster:

```bash
# List all briefs in your workspace
tm briefs

# Switch between briefs
tm context

# Set context to a specific brief directly
tm context --set <brief-id>

```

When you switch context, all Taskmaster commands operate on that brief's tasks.

## Real-Time Task Monitoring

```bash
# Watch tasks update in real-time as teammates make changes
tm list --watch

```

In team mode, `--watch` uses real-time cloud sync instead of local file watching, so you see changes from all team members as they happen.

## Rich Task Details

Team mode tasks include additional implementation metadata:

* Relevant files — Files to create, modify, or reference
* Codebase patterns — Coding patterns to follow
* Scope boundaries — What's in and out of scope
* Implementation approach — Step-by-step guidance
* Acceptance criteria — Definition of done checklist

## Authentication

```bash
# Log in (opens browser for OAuth)
tm login

# Log out
tm logout

```

Authentication supports multi-factor authentication with retry logic and live countdown timers.

## Solo vs Team

| Feature           | Solo             | Team                           |
| ----------------- | ---------------- | ------------------------------ |
| Storage           | Local JSON files | Hamster cloud                  |
| Collaboration     | Single user      | Multi-user with real-time sync |
| API keys          | Your own keys    | Hamster provides inference     |
| Offline support   | Full             | Requires internet              |
| Task organization | Tags             | Briefs                         |

You can start in solo mode and [export to team mode](https://tryhamster.com/docs/taskmaster/team/exporting-tasks) later.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Team","item":"https://tryhamster.com/docs/taskmaster/team"},{"@type":"ListItem","position":5,"name":"Overview","item":"https://tryhamster.com/docs/taskmaster/team/overview"}]}
```
