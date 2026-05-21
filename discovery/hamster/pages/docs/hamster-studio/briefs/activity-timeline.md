---
description: The audit trail of alignment — who voted, who flipped, what status changed, and on which version of the brief.
title: Activity Timeline | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Activity Timeline

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

# Activity Timeline

The audit trail of alignment — who voted, who flipped, what status changed, and on which version of the brief.

## Overview

The Activity tab is a version-grouped, append-only log of what's happened on a brief. Alignment votes, [Brief](https://tryhamster.com/docs/hamster-studio/briefs) status transitions, and document edits all appear here, bucketed by the version of the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) they happened against. If someone raised a concern on Version 3 and it was resolved by Version 4, the whole progression is visible in one scroll.

The timeline is the visible artefact of the **Align** leg of the loop. Refine produces the [Brief](https://tryhamster.com/docs/hamster-studio/briefs), Align is the team converging on it, and the timeline is how everyone sees that convergence happening.

![Activity timeline showing team alignment grouped by document version](https://tryhamster.com/_site/images/features/briefs/activity-timeline/activity-view-desktop-light.webp?v=6)![Activity timeline showing team alignment grouped by document version](https://tryhamster.com/_site/images/features/briefs/activity-timeline/activity-view-desktop-dark.webp?v=6) 

The Activity tab updates in real time. New votes, status changes, and comments appear as soon as they're submitted — no refresh needed.

## How It Works

1. Open the Activity tab — Inside any [Brief](https://tryhamster.com/docs/hamster-studio/briefs), click **Activity** in the document panel.
2. Scan the team overview — The current version is expanded at the top. A circular progress indicator summarises alignment — green when everyone is aligned, yellow when there are outstanding concerns.
3. Browse by version — Activity is grouped under collapsible version headers (Version 1, Version 2, …). Each group shows the votes, status changes, and edits that happened while that version was current. Older versions stay collapsed by default; click to expand.
4. Cast or update an alignment vote — From the [Brief](https://tryhamster.com/docs/hamster-studio/briefs), mark yourself **Aligned** or flag a **Concern**. Each vote is appended to the timeline as a new entry, so flips show up in the version they happened on. Cleared votes are recorded too, but excluded from the alignment count.
5. Read concerns — The "Concerns" section lists members who flagged issues, along with their comments explaining what needs resolution.
6. Act on feedback — Use the comments to update the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or continue the conversation in the chat panel. When a concern is resolved, the member can update their vote.
7. Load older versions — Use the "Load more" button at the bottom of the timeline to page through earlier versions.

## Key Capabilities

* **Version-grouped timeline**: Activity is bucketed by document version, not just chronologically. You can see which feedback was given against which state of the brief.
* **Append-only votes**: Every vote — including changes and clears — appends a new entry. The timeline never rewrites history, and realtime delivers new entries instantly.
* **Status changes are first-class**: [Brief](https://tryhamster.com/docs/hamster-studio/briefs) transitions (Draft → Refining → Aligned → Shipping → Done) appear in the timeline alongside votes. Status changes triggered by the AI agent show up here too, attributed to Hamster.
* **Live updates**: New votes and status changes appear immediately without refreshing the page. The tab also recovers cleanly when you return to it after a break.
* **Member identification**: Each item shows the team member's name and avatar; AI-driven changes show the Hamster avatar.
* **Pagination**: Load older version groups on demand. A failed load leaves the existing timeline intact and surfaces the error inline.
* **Context-aware empty state**: New [Brief](https://tryhamster.com/docs/hamster-studio/briefs) with no content gets a different empty state from a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) with content but no activity.

## What Counts as Activity

The Activity tab tracks:

* Alignment votes — "ready to proceed," "not yet," or a cleared vote.
* Comments on votes — notes left alongside an alignment vote explaining the reasoning.
* Status changes — transitions between Draft, Refining, Aligned, Shipping, Delivered, Done, and Archived. Status changes made by the AI agent through chat are logged here too.
* Document version markers — references to the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) version each batch of activity happened on. The actual content diffs live in [Document Versioning](https://tryhamster.com/docs/hamster-studio/collaboration/document-versioning).

## Using Alignment to Move Forward

The Activity tab is most useful as a forcing function before generating a plan. Share the [Brief](https://tryhamster.com/docs/hamster-studio/briefs), ask teammates to review, and check the timeline to see whether there's consensus.

Version grouping helps when concerns predate edits: if a stakeholder raised a concern on an earlier version and the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) has since been updated, you can see whether their concern was addressed by the changes in a later version — and whether they've updated their vote to reflect that.

## Tips

* Share the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) with stakeholders before generating a [Plan](https://tryhamster.com/docs/hamster-studio/plans) and ask them to cast alignment votes. A [Brief](https://tryhamster.com/docs/hamster-studio/briefs) with documented alignment is easier to hand off and less likely to [Result](https://tryhamster.com/docs/hamster-studio/results) in rework.
* Use the version grouping to trace decisions. If you need to know why a requirement changed, the activity history shows the feedback that prompted each revision.
* Review the Activity tab during standups to see who still needs to weigh in.
* If a teammate's concern has been addressed by edits, ask them to update their vote so the team overview reflects the current state.

## Related

* [Sharing Briefs](https://tryhamster.com/docs/hamster-studio/briefs/sharing-briefs)
* [Brief Status](https://tryhamster.com/docs/hamster-studio/briefs/brief-status)
* [Document Versioning](https://tryhamster.com/docs/hamster-studio/collaboration/document-versioning)
* [Mentions and Notifications](https://tryhamster.com/docs/hamster-studio/collaboration/mentions-notifications)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Briefs","item":"https://tryhamster.com/docs/hamster-studio/briefs"},{"@type":"ListItem","position":5,"name":"Activity Timeline","item":"https://tryhamster.com/docs/hamster-studio/briefs/activity-timeline"}]}
```
