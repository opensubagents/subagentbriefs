---
description: Every meaningful change to a brief, skill, or method is captured as a version — and you can always restore an earlier one without losing history.
title: Document Versioning | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Document Versioning

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

# Document Versioning

Every meaningful change to a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), skill, or [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) is captured as a version — and you can always restore an earlier one without losing history.

## Overview

Document versioning gives you a complete audit trail of how a document evolved. Versions are created automatically as you edit, and you can save named checkpoints at any point you consider significant. If a document goes in the wrong [Direction](https://tryhamster.com/docs/concepts/direction) — or you need to recover content that was removed — you can restore it to any recorded state.

Versioning runs in the background and applies to [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), skills, and methods. It deduplicates intelligently: a new version is only created when the **meaning** of the document changes, not when collaborator metadata or other invisible state shifts. So you don't get phantom versions in the history that show "no changes."

The version timeline is what your team aligns _on_. If the alignment vote happened against Version 3, you can always come back and see exactly what Version 3 looked like.

![Document version history panel showing version timeline with auto and manual checkpoints](https://tryhamster.com/_site/images/features/collaboration/document-versioning/context-versioning-desktop-light.webp?v=6)![Document version history panel showing version timeline with auto and manual checkpoints](https://tryhamster.com/_site/images/features/collaboration/document-versioning/context-versioning-desktop-dark.webp?v=6) 

## How It Works

1. A baseline version is created automatically — When you first write real content into a new [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or document, a baseline version is saved.
2. Edits are tracked continuously — As you and your collaborators edit, the system records lightweight checkpoints behind the scenes.
3. A new version snapshots after editing settles — When the document has been idle for a few minutes, the accumulated checkpoints consolidate into a new version snapshot. The version gets an AI-generated title and description.
4. Save a named checkpoint manually — At any point, save a named version from the document's history. Give it a meaningful label like "Approved by stakeholder" or "After kickoff changes" so it's easy to find later.
5. Restore an earlier version — Pick any version from the history and restore. The document content is replaced with that version's content, and the restore itself is recorded as a new "restore" version. History is never destroyed.
6. Compare two versions — Pick any two versions and see a side-by-side diff highlighting what was added, removed, or rewritten.

## Key Capabilities

* **Automatic versioning**: You don't need to do anything. Versions are created based on editing activity.
* **Content-aware deduplication**: A new version is only created when the document's meaning actually changes. Live-collaboration metadata, reconnects, and other behind-the-scenes activity don't produce phantom "no changes" versions in the history.
* **Named versions**: Save a named checkpoint at any meaningful moment. Names can be up to 255 characters. If you save a named version when the content hasn't changed since the last one, the name is applied to the existing version instead of creating a duplicate.
* **AI-generated summaries**: Each version automatically receives a generated title and description summarising what changed. They appear in the version history to help you find the right version at a glance.
* **Visual diff viewer**: Select any two versions for a structural diff. Additions, deletions, and modifications are highlighted at the paragraph level.
* **Version timeline**: A vertical timeline of all versions with version number, summary, timestamp, and type (auto, manual, restore). Failed or skipped versions are excluded so the timeline stays clean.
* **Restore without losing history**: Restoring creates a new "restore" version rather than overwriting. The complete history is always preserved.
* **Version numbering**: Versions are numbered sequentially starting at 0, giving a clear sense of how many distinct states the document has passed through.
* **Linked to [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation**: When a [Plan](https://tryhamster.com/docs/hamster-studio/plans) is generated from a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), the system records which version of the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) was used. You can always trace the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) state that produced any given plan.
* **Linked to alignment**: Activity timeline groups by version, so alignment votes and concerns are tied to the exact state of the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) they were cast against. See [Activity Timeline](https://tryhamster.com/docs/hamster-studio/briefs/activity-timeline).
* **Real-time updates**: The version history updates live. New versions — by you, a teammate, or the AI — appear without a page refresh.
* **Reviewer-safe**: Teammates with the Reviewer role see the document and version history fully read-only. No greyed-out controls, and no Reviewer cursor leaks into other people's editors. Reviewers can still browse history and view diffs.

## Version Types

| Type          | When it's created                                |
| ------------- | ------------------------------------------------ |
| Baseline (v0) | Automatically on first real content write        |
| Auto          | Automatically after editing activity settles     |
| Manual        | When you explicitly save a named checkpoint      |
| Restore       | When you restore the document to a prior version |

## Tips

* Save a named version before major reviews or before asking someone to make significant edits. Named versions are much easier to identify in history than auto-generated ones.
* Restoring replaces the current document but doesn't delete history. You can always restore again to any version, including ones that came after the one you just restored.
* If the document hasn't changed since the last version, saving a manual version names the existing version rather than creating a new one — and you'll see a confirmation that it did.
* Use the diff viewer to answer "what did we agree on between Version 3 and Version 4?" — it pairs naturally with the alignment votes shown on the Activity tab.
* Version history is visible to every member of the team account who has access to the document.

## Related

* [Real-Time Editing](https://tryhamster.com/docs/hamster-studio/collaboration/real-time-editing)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs/editing-briefs)
* [Activity Timeline](https://tryhamster.com/docs/hamster-studio/briefs/activity-timeline)
* [Skills and Methods](https://tryhamster.com/docs/hamster-studio/skills-methods)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Collaboration","item":"https://tryhamster.com/docs/hamster-studio/collaboration"},{"@type":"ListItem","position":5,"name":"Document Versioning","item":"https://tryhamster.com/docs/hamster-studio/collaboration/document-versioning"}]}
```
