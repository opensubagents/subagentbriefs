---
description: Connect the tools your Team already uses so Hamster can ground Chat, Briefs, Plans, and Delivery in real work.
title: Connections Overview | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Overview

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

# Connections Overview

Give the AI access to the tools your team already uses, so it understands your project without being told every time.

## Overview

[Connections](https://tryhamster.com/docs/hamster-studio/connections) are integrations between Hamster Studio and the external services your team relies on. Setting up a [Connection](https://tryhamster.com/docs/hamster-studio/connections) once gives every member of your workspace access to that data source — making the AI more accurate and contextually aware without requiring manual input each time.

![Connections settings page showing available integrations in a grid layout](https://tryhamster.com/_site/images/features/connections/overview/connections-overview-desktop-light.webp?v=6)![Connections settings page showing available integrations in a grid layout](https://tryhamster.com/_site/images/features/connections/overview/connections-overview-desktop-dark.webp?v=6) 

## What Connections Are

[Connections](https://tryhamster.com/docs/hamster-studio/connections) are integrations between Hamster Studio and the external services your team relies on — code repositories, issue trackers, communication tools, and documentation platforms. When you connect a service, Hamster can read data from it and use that data as context when you interact with the AI.

Without [Connections](https://tryhamster.com/docs/hamster-studio/connections), the AI only knows what you tell it in the current conversation. With [Connections](https://tryhamster.com/docs/hamster-studio/connections), it has access to your actual project: the issues in your backlog, the messages in relevant Slack channels, the pages in your Notion workspace, the code in your repository.

## Why Connect Your Tools

**Better answers.** When you ask "what are we building in this sprint?" Hamster can check your issue tracker rather than asking you to paste in the tickets.

**Richer briefs.** When you generate a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), the AI can reference real issues, real code, and real documentation rather than working from scratch.

**Less manual context.** You stop spending time re-explaining your project to the AI at the start of every conversation.

## How It Works

When you add a [Connection](https://tryhamster.com/docs/hamster-studio/connections), the service's data becomes available to the AI. The AI searches across all your connected sources when responding, pulling in the most relevant content automatically.

Some [Connections](https://tryhamster.com/docs/hamster-studio/connections) (Jira, Google Drive) search the service in real time when Hamster needs context, so you always get current data. Others (GitHub, Linear, Notion, Figma) sync data on [Connection](https://tryhamster.com/docs/hamster-studio/connections) and can be re-synced at any time. Slack installs a bot in your workspace that responds directly to @mentions and DMs.

Some [Connections](https://tryhamster.com/docs/hamster-studio/connections) go beyond read access. Issue trackers like Linear support two-way [Task](https://tryhamster.com/docs/hamster-studio/tasks) sync — [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) you create in Hamster flow to your tracker as issues, and status changes in the tracker flow back. Slack's bot lets you interact with Hamster from inside your team's conversations. These keep your tools in lockstep without manual updating.

Your team's [Connections](https://tryhamster.com/docs/hamster-studio/connections) are shared. One person sets up the GitHub [Connection](https://tryhamster.com/docs/hamster-studio/connections); everyone in the workspace benefits.

## Adding a Connection

1. Go to **Settings > [Connections](https://tryhamster.com/docs/hamster-studio/connections)** in your workspace.
2. Find the service you want to connect in the grid.
3. Click the service card to open the [Connection](https://tryhamster.com/docs/hamster-studio/connections) dialog.
4. Follow the [Connection](https://tryhamster.com/docs/hamster-studio/connections) steps — sign in to the service and authorize Hamster, or enter an access token.
5. The [Connection](https://tryhamster.com/docs/hamster-studio/connections) appears in your active [Connections](https://tryhamster.com/docs/hamster-studio/connections) list. The AI can start using it immediately.

## Removing a Connection

Click any active [Connection](https://tryhamster.com/docs/hamster-studio/connections) card and select **Remove**. The [Connection](https://tryhamster.com/docs/hamster-studio/connections) is deleted from both Hamster and the connected service. The AI will no longer have access to data from that source.

## Security

Credentials are encrypted at rest and never exposed to the browser after initial setup. All [Connections](https://tryhamster.com/docs/hamster-studio/connections) request only the minimum permissions required to read data.

## Related

* [AI Assistant](https://tryhamster.com/docs/hamster-studio/chat/in-documents)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Connections","item":"https://tryhamster.com/docs/hamster-studio/connections"},{"@type":"ListItem","position":5,"name":"Overview","item":"https://tryhamster.com/docs/hamster-studio/connections/overview"}]}
```
