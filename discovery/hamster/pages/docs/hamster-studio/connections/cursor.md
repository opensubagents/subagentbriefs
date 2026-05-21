---
description: Connect Cursor so Hamster context can support AI-assisted work inside your development environment.
title: Cursor | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Cursor

* [Documentation](https://tryhamster.com/docs "Documentation")
* [Getting Started](https://tryhamster.com/docs/hamster-studio/getting-started "Getting Started")
* [Common Challenges](https://tryhamster.com/docs/solutions "Common Challenges")
* Concepts
* [Overview](https://tryhamster.com/docs/concepts "Overview")
* [Direction](https://tryhamster.com/docs/concepts/direction "Direction")
* [Discovery](https://tryhamster.com/docs/concepts/discovery "Discovery")
* [Delivery](https://tryhamster.com/docs/concepts/delivery "Delivery")
* [Knowledge](https://tryhamster.com/docs/concepts/knowledge "Knowledge")
* By stage
* [Small teams](https://tryhamster.com/docs/for/small-teams "Small teams")
* [Startups & mid-size](https://tryhamster.com/docs/for/startups-and-mid-size "Startups & mid-size")
* [Enterprise & scaling](https://tryhamster.com/docs/for/enterprise-and-scaling "Enterprise & scaling")
* [Joining a team](https://tryhamster.com/docs/joining-a-team "Joining a team")
* Direction
* [Goals](https://tryhamster.com/docs/hamster-studio/goals "Goals")
* [Metrics](https://tryhamster.com/docs/hamster-studio/metrics "Metrics")
* [Results](https://tryhamster.com/docs/hamster-studio/results "Results")
* Discovery

* Hamster Chat

* [Research Agents](https://tryhamster.com/docs/hamster-studio/research-agents "Research Agents")
* Delivery
* [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives "Initiatives")

* Briefs

* Plans

* Tasks

* [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents "Cloud Agents")
* [Routines](https://tryhamster.com/docs/hamster-studio/routines "Routines")
* Knowledge

* Blueprints

* Methods

* [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph "Context Graph")

* Connections  
   * [Overview](https://tryhamster.com/docs/hamster-studio/connections/overview "Overview")  
   * [GitHub](https://tryhamster.com/docs/hamster-studio/connections/github "GitHub")  
   * [Linear](https://tryhamster.com/docs/hamster-studio/connections/linear "Linear")  
   * [Figma](https://tryhamster.com/docs/hamster-studio/connections/figma "Figma")  
   * [Slack](https://tryhamster.com/docs/hamster-studio/connections/slack "Slack")  
   * [Meeting Agent](https://tryhamster.com/docs/hamster-studio/connections/meeting-agent "Meeting Agent")  
   * [Notion](https://tryhamster.com/docs/hamster-studio/connections/notion "Notion")  
   * [Google Drive](https://tryhamster.com/docs/hamster-studio/connections/google-drive "Google Drive")  
   * [Jira](https://tryhamster.com/docs/hamster-studio/connections/jira "Jira")  
   * [Cursor](https://tryhamster.com/docs/hamster-studio/connections/cursor "Cursor")

* Surfaces

* CLI

* MCP Server

* [Taskmaster](https://tryhamster.com/docs/taskmaster "Taskmaster")
* Workspace

* Teams

* Collaboration

* Account Settings

# Cursor

Connect Cursor IDE to enable [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) that can run [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) directly in your codebase.

## Overview

The Cursor [Connection](https://tryhamster.com/docs/hamster-studio/connections) is different from other connections. While GitHub, Linear, Slack, and Notion give the AI read access to data for context, the Cursor [Connection](https://tryhamster.com/docs/hamster-studio/connections) enables a different capability: [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) that can perform coding [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) inside your development environment.

When Cursor is connected, Hamster can delegate coding work to an agent running in your Cursor IDE — writing code, applying changes, and working through [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) while you focus on other things.

This is an advanced feature that operates on your local development environment. It requires an active Cursor installation with an active session.

## What It Enables

* Background coding [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) — Agents can work on implementation [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) in your codebase
* Code changes — The agent can write new files, modify existing ones, and apply diffs

The Cursor [Connection](https://tryhamster.com/docs/hamster-studio/connections) is distinct from the read-only context connections. It allows the agent to take action, not just retrieve information.

## How to Connect

1. Go to **Settings > [Connections](https://tryhamster.com/docs/hamster-studio/connections)** and click the **Cursor** card.
2. In the dialog, enter your **Cursor API Key**.
3. Click **Connect**.

The [Connection](https://tryhamster.com/docs/hamster-studio/connections) is ready once saved. Unlike OAuth [Connections](https://tryhamster.com/docs/hamster-studio/connections), there is no redirect to an external site.

## Getting Your Cursor API Key

Your Cursor API key is available in the Cursor settings.

To find it:

1. Open Cursor.
2. Go to **Cursor Settings**.
3. Copy your API key from the account or API section.

## One Connection Per Workspace

Cursor is a single-connection service. You can have one active Cursor [Connection](https://tryhamster.com/docs/hamster-studio/connections) per workspace. Once connected, the Cursor card no longer appears in the Add [Connections](https://tryhamster.com/docs/hamster-studio/connections) grid. To change the connected Cursor account, remove the existing [Connection](https://tryhamster.com/docs/hamster-studio/connections) first and then add a new one.

## Tips

* [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) work best on well-defined, scoped tasks. Providing clear [Task](https://tryhamster.com/docs/hamster-studio/tasks) descriptions and context produces better [Results](https://tryhamster.com/docs/hamster-studio/results) than open-ended requests.
* The agent operates in your local Cursor environment. Make sure Cursor is running and your project is open when you want the agent to work.
* Review changes made by the agent before committing them. [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) can make mistakes, particularly on complex or ambiguous tasks.
* Connecting GitHub alongside Cursor helps the agent understand your repository structure and code conventions before making changes.

## Related

* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)
* [GitHub](https://tryhamster.com/docs/hamster-studio/connections/github)
* [Task Overview](https://tryhamster.com/docs/hamster-studio/tasks/task-overview)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Connections","item":"https://tryhamster.com/docs/hamster-studio/connections"},{"@type":"ListItem","position":5,"name":"Cursor","item":"https://tryhamster.com/docs/hamster-studio/connections/cursor"}]}
```
