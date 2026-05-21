---
description: Pull teammates into a brief thread, share a public link, or invite a Reviewer to comment without consuming a paid seat.
title: Sharing Briefs | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Sharing Briefs

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

# Sharing Briefs

Pull teammates into a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) thread, share a public link with someone outside the team, or invite a Reviewer to comment without consuming a paid seat.

## Overview

[Briefs](https://tryhamster.com/docs/hamster-studio/briefs) in Hamster Studio belong to a team account. Every member of that account can see every [Brief](https://tryhamster.com/docs/hamster-studio/briefs) — but who is part of the conversation thread, and who can edit, depends on roles and explicit invitations. Share a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) by inviting people to its conversation thread, by handing them a public share link, or by giving them a Reviewer seat on the team so they can comment without taking a paid seat.

Cross-account isolation is strict: a teammate's [Brief](https://tryhamster.com/docs/hamster-studio/briefs) in one account is never visible to people in another, and account membership is checked at every layer — inside the chat agent, inside the editor, and on the database itself.

![Brief header showing participant avatars and the invite dropdown for adding teammates](https://tryhamster.com/_site/images/features/briefs/sharing-briefs/share-brief-desktop-light.webp?v=6)![Brief header showing participant avatars and the invite dropdown for adding teammates](https://tryhamster.com/_site/images/features/briefs/sharing-briefs/share-brief-desktop-dark.webp?v=6) 

## How It Works

1. Open the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) — The participant control sits in the document header, next to the title.
2. Open the invite control — Click the participant avatars or the invite button. A dropdown opens showing current participants and an option to invite more.
3. Invite a teammate — Search by name in the dropdown and select the person. They're added as a participant on the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s conversation thread.
4. Or join / leave directly — If you're already a participant, the same control lets you leave the thread. If not, you can join.
5. Share a public link — For someone outside the team, copy the public share URL of the brief. The share page renders the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) content with an alignment-vote CTA, and lets people sign in to participate without joining your team account.
6. Or invite them to the team — If they need ongoing access, invite them to the team. Choose Reviewer for read-and-comment-only access, or Creator/Admin for write access. See [Inviting Members](https://tryhamster.com/docs/hamster-studio/teams/inviting-members).

## Who Can See and Do What

[Briefs](https://tryhamster.com/docs/hamster-studio/briefs) are scoped to a team account. Within the team, what a member can do depends on their role:

| Role                 | View [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) | Comment / vote | Create / edit | Invite members | Manage settings |
| -------------------- | ---------------------------------------------------------------- | -------------- | ------------- | -------------- | --------------- |
| Reviewer (free seat) | ✓                                                                | ✓              |               |                |                 |
| Creator              | ✓                                                                | ✓              | ✓             | ✓              |                 |
| Admin                | ✓                                                                | ✓              | ✓             | ✓              | ✓               |
| Owner                | ✓                                                                | ✓              | ✓             | ✓              | ✓               |

Reviewers see the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) workspace as fully read-only — no greyed-out controls and no cursor leaking outbound. They can still cast alignment votes and watch the live document. Reviewer seats don't count toward your paid-seat total, so you can bring in stakeholders, designers, or external reviewers without expanding your subscription.

For more on roles, see [Roles and Permissions](https://tryhamster.com/docs/hamster-studio/teams/roles-permissions).

## Key Capabilities

* **Participant avatars**: The document header shows an avatar cluster of current participants.
* **Invite by name**: Search teammates by display name in the invite dropdown.
* **Join and leave**: Participants can leave a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) thread when they no longer need to be involved. Non-participants can join at any time.
* **Thread context shared**: When you invite someone, they get the full conversation thread for that [Brief](https://tryhamster.com/docs/hamster-studio/briefs), including prior messages.
* **Real-time participation**: Newly invited participants appear immediately. Their alignment votes show in the Activity tab as soon as they cast them.
* **Auto-add via mention**: Mentioning a teammate with `@name` in chat adds them to the thread as a participant before the notification fires, so the deep link in their notification always lands in the right place.
* **Public share page**: Each [Brief](https://tryhamster.com/docs/hamster-studio/briefs) has a public share URL. The share page shows the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) body and an alignment vote CTA, with a polished sign-in flow for visitors who aren't on your team yet.
* **Cross-account isolation**: [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) from one team account are never visible from another. Permission checks happen on every API call, every database query, and inside the AI agent — a Reviewer's read-only state is enforced on the server, not just hidden in the UI.
* **Slack alignment unfurls**: When the Slack bot is connected, posting a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) URL into Slack unfurls a Block Kit card where teammates can cast alignment votes natively. [Brief](https://tryhamster.com/docs/hamster-studio/briefs) flexpanes in Slack render the markdown description and let editors update the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) from inside Slack.

## Inviting Someone Who Isn't on Your Team

The invite-to-thread dropdown only shows members of your current team account. If you need to collaborate with someone who isn't on the team yet:

* Quick read — share the public share link.
* Comment-only access — invite them to the team as a Reviewer (free seat).
* Edit access — invite them as a Creator or Admin.

See [Inviting Members](https://tryhamster.com/docs/hamster-studio/teams/inviting-members).

## Tips

* Invite stakeholders early so they can follow the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s development in the chat thread instead of receiving a finished document with no context.
* For [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) that need formal sign-off, invite the relevant people and ask them to cast an alignment vote in the Activity tab. This creates a record of who agreed and when.
* Use the Reviewer role for product, design, or business stakeholders who need to comment but aren't editing. It's a free seat and gives them a clean read-only experience.
* You don't need to invite someone as a thread participant just for them to see the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) — every team member can read briefs. Participation is specifically about the conversation thread.

## Related

* [Activity Timeline](https://tryhamster.com/docs/hamster-studio/briefs/activity-timeline)
* [Inviting Members](https://tryhamster.com/docs/hamster-studio/teams/inviting-members)
* [Roles and Permissions](https://tryhamster.com/docs/hamster-studio/teams/roles-permissions)
* [Real-time Editing](https://tryhamster.com/docs/hamster-studio/collaboration/real-time-editing)
* [Slack Connection](https://tryhamster.com/docs/hamster-studio/connections/slack)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Briefs","item":"https://tryhamster.com/docs/hamster-studio/briefs"},{"@type":"ListItem","position":5,"name":"Sharing Briefs","item":"https://tryhamster.com/docs/hamster-studio/briefs/sharing-briefs"}]}
```
