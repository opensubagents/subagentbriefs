---
description: Connect Notion so the AI can reference pages, databases, and documentation as workspace context.
title: Notion | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Notion

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

# Notion

Connect your Notion workspace so the AI can reference your pages, databases, and documentation.

## Overview

The Notion [Connection](https://tryhamster.com/docs/hamster-studio/connections) gives the AI access to the pages and databases in your Notion workspace. Once connected, the AI can read your product documentation, project notes, decision logs, and any other content you have in Notion. This is particularly useful for teams that use Notion as their primary [Knowledge](https://tryhamster.com/docs/concepts/knowledge) base.

The [Connection](https://tryhamster.com/docs/hamster-studio/connections) uses OAuth — you authorise through Notion's own login flow and select which pages and databases to share.

## What It Syncs

* Pages — Notion pages with their full text content
* Databases — Notion databases and their records
* Database properties — Structured fields within databases
* Embedded files — Files attached to pages

Notion syncs content on connection. Data is indexed and available to the AI immediately. You can trigger a re-sync at any time from the [Connections](https://tryhamster.com/docs/hamster-studio/connections) page.

## How to Connect

1. Go to **Settings > [Connections](https://tryhamster.com/docs/hamster-studio/connections)** and click the **Notion** card.
2. In the dialog, click **Connect with Notion**.
3. You are redirected to Notion's authorization page.
4. Log in to Notion if prompted, then select which pages and databases to share with Hamster.
5. Click **Allow access**.
6. You are returned to Hamster Studio. Indexing begins automatically.

The [Connection](https://tryhamster.com/docs/hamster-studio/connections) is named after your Notion workspace.

## Controlling What Notion Shares

Notion requires you to explicitly select which pages and databases to share with any integration. Hamster only has access to the content you select during authorization. You can add or remove pages at any time by going to the page in Notion, clicking the three-dot menu, and managing the [Connection](https://tryhamster.com/docs/hamster-studio/connections) under **[Connections](https://tryhamster.com/docs/hamster-studio/connections)**.

If you add new pages after connecting, Notion does not share them automatically. You need to go to those pages in Notion and grant access to the Hamster integration, then trigger a re-sync in Hamster.

## Tips

* Share your most important documentation and reference material first. You can always add more later.
* Databases with structured properties (status, owner, due date) are particularly useful — the AI can answer questions about database contents more precisely than from unstructured prose.
* If you have a large Notion workspace, consider which pages are actually relevant to the projects you run in Hamster rather than sharing everything. Focused context tends to produce better results.
* After adding new Notion pages to the integration, trigger a re-sync from the [Connections](https://tryhamster.com/docs/hamster-studio/connections) page so the new content is available to the AI.

## Related

* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)
* [Slack](https://tryhamster.com/docs/hamster-studio/connections/slack)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Connections","item":"https://tryhamster.com/docs/hamster-studio/connections"},{"@type":"ListItem","position":5,"name":"Notion","item":"https://tryhamster.com/docs/hamster-studio/connections/notion"}]}
```
