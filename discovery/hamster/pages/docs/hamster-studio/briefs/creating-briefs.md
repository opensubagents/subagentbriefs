---
description: Start a brief from a chat — describe what you want, and Hamster comes back with a draft in its own thread.
title: Creating Briefs | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Creating Briefs

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
   * [Creating Briefs](https://tryhamster.com/docs/hamster-studio/briefs/creating-briefs "Creating Briefs")  
   * [Editing Briefs](https://tryhamster.com/docs/hamster-studio/briefs/editing-briefs "Editing Briefs")  
   * [Brief Status](https://tryhamster.com/docs/hamster-studio/briefs/brief-status "Brief Status")  
   * [Brief Tags](https://tryhamster.com/docs/hamster-studio/briefs/brief-tags "Brief Tags")  
   * [Context Documents](https://tryhamster.com/docs/hamster-studio/briefs/context-documents "Context Documents")  
   * [Activity Timeline](https://tryhamster.com/docs/hamster-studio/briefs/activity-timeline "Activity Timeline")  
   * [Sharing Briefs](https://tryhamster.com/docs/hamster-studio/briefs/sharing-briefs "Sharing Briefs")  
   * [Delivering Briefs](https://tryhamster.com/docs/hamster-studio/briefs/delivering-briefs "Delivering Briefs")  
   * [Document Analysis](https://tryhamster.com/docs/hamster-studio/briefs/document-analysis "Document Analysis")

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

* Account Settings

# Creating Briefs

Start a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) from a chat — describe what you want, and Hamster comes back with a draft in its own thread.

## Overview

Most [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) are born in chat. You type "we should add tag-based filtering to [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)," the AI agent replies in a child thread with a draft [Brief](https://tryhamster.com/docs/hamster-studio/briefs), and a clickable card showing the new [Brief](https://tryhamster.com/docs/hamster-studio/briefs) lands in your conversation. From there you open the [Brief](https://tryhamster.com/docs/hamster-studio/briefs), refine it, share it, and ship it. There is no separate [Brief](https://tryhamster.com/docs/hamster-studio/briefs) authoring wizard — chat is the entry point, and the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) link is always visible in the agent's first reply.

You can also create a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) without chat — from the [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) list, from the [CLI](https://tryhamster.com/docs/hamster-studio/cli), or from the Hamster Chrome extension when you want to pin a URL to a new brief.

![Briefs list view showing project briefs](https://tryhamster.com/_site/images/features/briefs/creating-briefs/briefs-list-view-light.gif?v=6)![Briefs list view showing project briefs](https://tryhamster.com/_site/images/features/briefs/creating-briefs/briefs-list-view-dark.gif?v=6) 

## How It Works

![Creating a new brief from the briefs page](https://tryhamster.com/_site/images/features/briefs/creating-briefs/create-brief-flow-light.gif?v=6)![Creating a new brief from the briefs page](https://tryhamster.com/_site/images/features/briefs/creating-briefs/create-brief-flow-dark.gif?v=6) 
1. Describe what you want in chat — Open a conversation and type what you'd like to ship. You can drop attachments alongside the prompt — `.fig` files, PDFs, markdown, images, or pasted URLs. The agent grounds the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) in those attachments instead of treating them as decoration.
2. The AI drafts the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) in a child thread — Long answers and [Brief](https://tryhamster.com/docs/hamster-studio/briefs) drafts move into their own child thread automatically, keeping the parent chat clean. The agent's first reply includes a clickable [Brief](https://tryhamster.com/docs/hamster-studio/briefs) card so you can jump straight in.
3. Or click "New [Brief](https://tryhamster.com/docs/hamster-studio/briefs)" in the [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) list — If you'd rather start from a blank document, navigate to [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) in the sidebar and click "New [Brief](https://tryhamster.com/docs/hamster-studio/briefs)" in the top-right. A dialog asks for a title (up to 255 characters) and an optional description.
4. Open and edit — The editor opens with the AI chat panel alongside it, ready for your first prompt. The chat already has access to whatever the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) contains.
5. Save automatically — Everything you type is saved in real time. Collaborators see your changes as you make them.

## Where Briefs Can Be Created

* Hamster AI chat — the primary path. [Brief](https://tryhamster.com/docs/hamster-studio/briefs) creation runs in a spawned child thread so the parent conversation stays focused.
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) list — "New [Brief](https://tryhamster.com/docs/hamster-studio/briefs)" button in the top-right of the [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) section.
* [CLI](https://tryhamster.com/docs/hamster-studio/cli) — create [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) from your terminal with the Hamster [CLI](https://tryhamster.com/docs/hamster-studio/cli); positional [Brief](https://tryhamster.com/docs/hamster-studio/briefs) argument and URL parsing are supported. See [CLI Brief Creation](https://tryhamster.com/docs/hamster-studio/cli/cli-brief-creation).
* Chrome extension — pin the URL of any page you're reading to a new [Brief](https://tryhamster.com/docs/hamster-studio/briefs), with the page acting as the first context document.
* From a Slack message — when the Slack bot is connected, [Brief](https://tryhamster.com/docs/hamster-studio/briefs) creation can happen inline; the bot also posts the new [Brief](https://tryhamster.com/docs/hamster-studio/briefs) URL back to the originating Slack thread.

A descriptive title makes [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) easier to find later. "Redesign the onboarding flow for mobile users" beats "Onboarding redesign."

## Tips

* A descriptive title makes [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) easier to find later. "Redesign the onboarding flow for mobile users" beats "Onboarding redesign."
* Drop the customer call recording, the Figma file, and the linked notion of what you've already tried into chat _before_ asking for a brief. The agent uses everything attached as grounding.
* If the agent comes back asking clarifying questions, answer them in the same thread — your answers persist across page refreshes, so you can keep iterating.
* Use the search bar in the [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) toolbar to find a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) by title in real time. You don't need to press Enter.

## Related

* [Editing Briefs](https://tryhamster.com/docs/hamster-studio/briefs/editing-briefs)
* [Brief Status](https://tryhamster.com/docs/hamster-studio/briefs/brief-status)
* [Generating Plans](https://tryhamster.com/docs/hamster-studio/plans/generating-plans)
* [CLI Brief Creation](https://tryhamster.com/docs/hamster-studio/cli/cli-brief-creation)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Briefs","item":"https://tryhamster.com/docs/hamster-studio/briefs"},{"@type":"ListItem","position":5,"name":"Creating Briefs","item":"https://tryhamster.com/docs/hamster-studio/briefs/creating-briefs"}]}
```
