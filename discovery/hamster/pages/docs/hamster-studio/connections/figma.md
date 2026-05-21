---
description: Connect Figma so Hamster can reference designs when writing Briefs, Blueprints, and Plans.
title: Figma | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Figma

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

# Figma

Connect Figma so Hamster can reference your designs when writing [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), and plans.

## Overview

The Figma [Connection](https://tryhamster.com/docs/hamster-studio/connections) links your Figma account to Hamster Studio. Once connected, Hamster can pull in relevant designs — screens, components, layout decisions — when you're working on a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or blueprint. Instead of describing a design in words, attach the Figma file and let Hamster work from the actual source.

You can also upload `.fig` files directly to a [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s Context tab. Hamster extracts thumbnails, structure, and design details from the file, making design context available even without an active Figma connection.

## How to Connect

1. Go to **Settings > [Connections](https://tryhamster.com/docs/hamster-studio/connections)** and click the **Figma** card.
2. Click **Connect with Figma**. You'll be taken to Figma to authorize.
3. Review the permissions and click **Allow**.
4. You're returned to Hamster Studio. The [Connection](https://tryhamster.com/docs/hamster-studio/connections) is ready to use.

Hamster only requests read access to your Figma files. It cannot modify your designs.

## What Hamster Can Reference

* Files — Design files in your Figma account, including pages, frames, and components
* Thumbnails — Visual previews that appear in the Context tab and [Brief](https://tryhamster.com/docs/hamster-studio/briefs) editor
* Structure — File names, last modified dates, and how your designs are organized

Hamster uses design context when writing [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), and generating [Task](https://tryhamster.com/docs/hamster-studio/tasks) plans. If a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) mentions a specific screen or component and Figma is connected, Hamster references the actual design instead of working from a text description alone.

## Uploading .fig Files

You can also drop Figma's native `.fig` files directly into a [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s Context tab, the same way you'd upload a PDF or image. Hamster reads the file and extracts:

* Thumbnail — A visual preview on the document card
* Structure — Page names, component hierarchy, and how the file is organized
* Design details — Information Hamster uses as context when writing [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) and generating [Plans](https://tryhamster.com/docs/hamster-studio/plans)

This is useful when you want to share a specific design snapshot, or when working without an active Figma connection.

## Figma URL Context

You can paste a Figma URL directly into chat. Hamster extracts the design and adds it to your [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s context automatically — thumbnails appear in the Context tab alongside your other documents.

* **Private files** use your connected Figma account for authentication.
* **Public files** work without a connection.

This is the fastest way to bring a design into a conversation. No file download or upload required — just paste the link.

## Tips

* Paste a Figma URL in chat instead of uploading a file when you want to reference the latest version of a design. The URL always pulls the current state.
* Connect Figma before generating a [Plan](https://tryhamster.com/docs/hamster-studio/plans) if your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) references specific designs. Hamster produces more accurate [Task](https://tryhamster.com/docs/hamster-studio/tasks) breakdowns when it can see the design, not just read about it.
* Upload `.fig` files for design snapshots you want to freeze as context. The uploaded file captures the design at that point in time, independent of future Figma changes.
* Figma works well alongside GitHub. Hamster can connect designs to the code that implements them when both are connected.
* The Figma [Connection](https://tryhamster.com/docs/hamster-studio/connections) is team-level — connect once and every team member benefits.

## Related

* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)
* [Context Documents](https://tryhamster.com/docs/hamster-studio/briefs/context-documents)
* [Generating Plans](https://tryhamster.com/docs/hamster-studio/plans/generating-plans)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Connections","item":"https://tryhamster.com/docs/hamster-studio/connections"},{"@type":"ListItem","position":5,"name":"Figma","item":"https://tryhamster.com/docs/hamster-studio/connections/figma"}]}
```
