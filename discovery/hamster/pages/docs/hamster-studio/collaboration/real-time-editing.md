---
description: Multiple teammates can edit the same brief or document at once with live cursor visibility and instant updates that keep collaboration in sync.
title: Real-Time Editing | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Real-Time Editing

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

* Surfaces

* CLI

* MCP Server

* [Taskmaster](https://tryhamster.com/docs/taskmaster "Taskmaster")
* Workspace

* Teams

* Collaboration  
   * [Real-Time Editing](https://tryhamster.com/docs/hamster-studio/collaboration/real-time-editing "Real-Time Editing")  
   * [Mentions & Notifications](https://tryhamster.com/docs/hamster-studio/collaboration/mentions-notifications "Mentions & Notifications")  
   * [Document Versioning](https://tryhamster.com/docs/hamster-studio/collaboration/document-versioning "Document Versioning")

* Account Settings

# Real-Time Editing

Multiple team members can edit the same [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or document at the same time, with each person's changes and cursor position visible to everyone else instantly.

## Overview

Real-time editing lets your whole team work inside a document simultaneously without stepping on each other's work. You see who else is present, where their cursor is, and what they're typing — all as it happens. Changes merge automatically, so there is no need to take turns editing or reconcile separate copies.

This is most useful during [Brief](https://tryhamster.com/docs/hamster-studio/briefs) reviews, kickoff sessions, and any situation where several people need to shape content together rather than asynchronously.

![Brief editor with three collaborator cursors at different positions and typing indicators active](https://tryhamster.com/_site/images/features/collaboration/real-time-editing/multi-collaborator-editing-desktop-light.webp?v=6)![Brief editor with three collaborator cursors at different positions and typing indicators active](https://tryhamster.com/_site/images/features/collaboration/real-time-editing/multi-collaborator-editing-desktop-dark.webp?v=6) 

## How It Works

1. Open any [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or document — When you navigate to a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), skill, or [Method](https://tryhamster.com/docs/hamster-studio/skills-methods), the editor connects automatically to a shared editing session for that document.
2. Editing begins — As soon as the editor shows a "connected" status, your changes broadcast to every other person who has the document open. Their changes appear in your editor with no page refresh needed.
3. See who's present — Each active editor appears as a colored cursor label showing their name. Labels disappear automatically when someone closes the document or goes idle for more than 30 seconds.
![Team alignment popover showing collaborator presence and activity status](https://tryhamster.com/_site/images/features/collaboration/real-time-editing/team-alignment-popover-desktop-light.webp?v=6)![Team alignment popover showing collaborator presence and activity status](https://tryhamster.com/_site/images/features/collaboration/real-time-editing/team-alignment-popover-desktop-dark.webp?v=6) 
1. Changes save automatically — Edits save to the database continuously as you type. If your [Connection](https://tryhamster.com/docs/hamster-studio/connections) drops, the editor reconnects on its own and syncs any changes you made offline when it comes back.

## Key Capabilities

* **Concurrent editing**: Any number of team members can edit the same document at once. Edits from each person merge without conflict.
* **Cursor presence**: Colored cursor labels show where each active editor is working in the document. Each person gets a consistent color tied to their name.
* **Automatic reconnection**: If your [Connection](https://tryhamster.com/docs/hamster-studio/connections) drops, the editor retries with increasing wait times (starting at 300 milliseconds, up to 10 seconds). Your work is preserved during disconnects.
* **Local backup**: In the rare case that a save to the database fails, your changes are held locally in the browser until connectivity is restored.
* **AI agent participation**: The Hamster AI assistant can edit documents in the same session. Its changes appear alongside human edits.
![Brief editor with a collaborator's cursor visible alongside the current user's edits](https://tryhamster.com/_site/images/features/collaboration/real-time-editing/brief-editor-collab-desktop-light.webp?v=6)![Brief editor with a collaborator's cursor visible alongside the current user's edits](https://tryhamster.com/_site/images/features/collaboration/real-time-editing/brief-editor-collab-desktop-dark.webp?v=6) ![Team alignment popover showing active collaborators and their current status in the document](https://tryhamster.com/_site/images/features/collaboration/real-time-editing/team-alignment-popover-desktop-light.webp?v=6)![Team alignment popover showing active collaborators and their current status in the document](https://tryhamster.com/_site/images/features/collaboration/real-time-editing/team-alignment-popover-desktop-dark.webp?v=6) 

## Tips

* The editor shows a status indicator ("connecting", "connected", "disconnected") in the header. Wait for "connected" before making important edits in an unstable network environment.
* Cursor labels for other editors fade after 30 seconds of no activity from that user. This keeps the interface clean during long sessions where some participants step away.
* If you paste a very large block of content (images, large text dumps), the save may take a moment longer than a normal keystroke. The editor handles this gracefully, but you may notice a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) delay.
* Real-time editing works inside [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), skills, and methods. It does not apply to [Task](https://tryhamster.com/docs/hamster-studio/tasks) fields, comments, or settings.

## Related

* [Document Versioning](https://tryhamster.com/docs/hamster-studio/collaboration/document-versioning)
* [Mentions and Notifications](https://tryhamster.com/docs/hamster-studio/collaboration/mentions-notifications)
* [Editing Briefs](https://tryhamster.com/docs/hamster-studio/briefs/editing-briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Collaboration","item":"https://tryhamster.com/docs/hamster-studio/collaboration"},{"@type":"ListItem","position":5,"name":"Real Time Editing","item":"https://tryhamster.com/docs/hamster-studio/collaboration/real-time-editing"}]}
```
