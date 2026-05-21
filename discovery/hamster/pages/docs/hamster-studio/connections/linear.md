---
description: Move a Linear issue and the matching Hamster brief, task, or initiative updates within seconds — and vice versa.
title: Linear | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Linear

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

# Linear

_Move a Linear issue and the matching Hamster [Brief](https://tryhamster.com/docs/hamster-studio/briefs), [Task](https://tryhamster.com/docs/hamster-studio/tasks), or [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) updates within seconds — and vice versa. Nobody has to ask "where's the source of truth?"_

## Overview

The Linear [Connection](https://tryhamster.com/docs/hamster-studio/connections) links your Linear workspace to Hamster Studio. When two-way sync is enabled, [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), and [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) in Hamster stay in lockstep with their counterparts in Linear — projects, issues, and initiatives. Update a [Task](https://tryhamster.com/docs/hamster-studio/tasks) status in Hamster and Linear reflects it. Reassign an issue in Linear and Hamster picks it up.

This is the leg of the loop that makes Hamster usable inside [Teams](https://tryhamster.com/docs/hamster-studio/teams) already paying for Linear. Adopting Hamster's [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and alignment surfaces does not require ripping out the existing tracker. The [Team](https://tryhamster.com/docs/hamster-studio/teams) can keep doing standups in Linear while planning in Hamster, and the two stay aligned without anyone copy-pasting statuses.

The [Connection](https://tryhamster.com/docs/hamster-studio/connections) uses OAuth. You authorise Hamster directly through Linear — no token to manage.

## Two-Way Sync

New Linear [Connections](https://tryhamster.com/docs/hamster-studio/connections) start with two-way sync disabled. This gives teams a safe setup path: connect for context first, then enable [Task](https://tryhamster.com/docs/hamster-studio/tasks) syncing when you're ready.

When two-way sync is enabled, [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), and [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) stay synchronized in both directions:

* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) ↔ Linear projects — Title, description, and status flow both ways. Hamster [Brief](https://tryhamster.com/docs/hamster-studio/briefs) status changes update the Linear project status; Linear project status changes update the Hamster [Brief](https://tryhamster.com/docs/hamster-studio/briefs).
* [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) ↔ Linear issues — Title, description, status, priority, assignee, and due date all sync. The status mapping is bootstrapped automatically from your Linear [Team](https://tryhamster.com/docs/hamster-studio/teams)'s workflow states.
* [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) ↔ Linear [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) — Title, description, status, target date, and the [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives)\-to-[Brief](https://tryhamster.com/docs/hamster-studio/briefs) associations sync. Sub-[Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) parent/child relationships flow with intelligent fallback for Linear workspaces that don't support sub-[Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives).

Changes propagate within seconds via webhooks.

### What syncs bidirectionally

| Entity / Field                                                                                                                          | Hamster → Linear | Linear → Hamster |
| --------------------------------------------------------------------------------------------------------------------------------------- | ---------------- | ---------------- |
| [Brief](https://tryhamster.com/docs/hamster-studio/briefs) title and description                                                        | Yes              | Yes              |
| [Brief](https://tryhamster.com/docs/hamster-studio/briefs) status (project status)                                                      | Yes              | Yes              |
| [Task](https://tryhamster.com/docs/hamster-studio/tasks) title and description                                                          | Yes              | Yes              |
| [Task](https://tryhamster.com/docs/hamster-studio/tasks) status                                                                         | Yes              | Yes              |
| [Task](https://tryhamster.com/docs/hamster-studio/tasks) priority                                                                       | Yes              | Yes              |
| [Task](https://tryhamster.com/docs/hamster-studio/tasks) assignee                                                                       | Yes              | Yes              |
| [Task](https://tryhamster.com/docs/hamster-studio/tasks) due date                                                                       | Yes              | Yes              |
| [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) title and description                                              | Yes              | Yes              |
| [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) status                                                             | Yes              | Yes              |
| [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) target date                                                        | Yes              | Yes              |
| [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) ↔ [Brief](https://tryhamster.com/docs/hamster-studio/briefs) links | Yes              | Yes              |
| Sub-initiative hierarchy                                                                                                                | Yes              | Yes              |

### Conflict resolution

When the same field is changed in both tools before either sync completes, Hamster uses last-writer-wins at the field level. The most recent change is applied and both tools converge to the same state. Tiptap document content ([Brief](https://tryhamster.com/docs/hamster-studio/briefs) and [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) bodies) merges through Y.js so concurrent edits don't conflict.

A 5-second loop-prevention window plus per-event idempotency keys stop changes from echoing back and forth.

## Assignee Sync

Assignees flow in both directions. When Linear sends an assignee Hamster doesn't know about, Hamster shows the external user's name with a placeholder avatar on the [Task](https://tryhamster.com/docs/hamster-studio/tasks) and notifies a teammate with invite permissions to invite that person to the workspace. Once they accept the invite, all pending assignments backfill onto their Hamster account automatically.

Hamster never auto-creates shadow user accounts. Every Hamster user is invited explicitly.

## Tagged-Project Filtering

You can scope which Linear projects sync by tagging them with a label in Linear. Instead of syncing everything, add a specific tag and configure Hamster to only sync projects with that tag.

This is useful when your Linear workspace contains projects from multiple teams or [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) and you only want a subset flowing into Hamster.

To configure:

1. Open the Linear [Connection](https://tryhamster.com/docs/hamster-studio/connections) settings in **Workspace Settings > [Connections](https://tryhamster.com/docs/hamster-studio/connections)**.
2. Under **Sync settings**, enable tag-based filtering.
3. Enter the tag name to filter by.

Only projects with the matching tag are synced. Adding the tag to a new project later picks it up automatically. Removing the tag drops the project out of scope.

Hamster-created Linear projects are automatically labeled, so a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) delivered through Hamster always lands inside the configured scope.

## What the AI Can Access

Beyond two-way sync, the [Connection](https://tryhamster.com/docs/hamster-studio/connections) gives the AI read access to your full Linear workspace:

* Teams — Linear teams and their configuration.
* Projects — Projects within each team, with status and metadata.
* Issues — Issues and sub-issues, including titles, descriptions, status, priority, and labels.
* Comments — Comments on issues.
* Attachments — Files and links attached to issues.
* Users — Workspace members and their profiles.

The full workspace syncs on [Connection](https://tryhamster.com/docs/hamster-studio/connections) and is available to the AI immediately. It refreshes through the same webhook stream that powers two-way sync.

## How to Connect

1. Go to **Workspace Settings > [Connections](https://tryhamster.com/docs/hamster-studio/connections)** and click the **Linear** card.
2. In the dialog, click **Connect with Linear**.
3. You're redirected to Linear's authorization page.
4. Review the requested permissions and click **Authorize**.
5. You're returned to Hamster Studio. Choose whether to enable two-way sync or connect for AI context only.
6. If enabling two-way sync, select the Linear team to sync with.

The [Connection](https://tryhamster.com/docs/hamster-studio/connections) is named after your Linear workspace automatically.

### Requirements for two-way sync

Two-way sync requires webhook creation in Linear. The user who authorises the [Connection](https://tryhamster.com/docs/hamster-studio/connections) must have an **Admin** or **Owner** role in their Linear organisation. If the authorising user has a lower role, the [Connection](https://tryhamster.com/docs/hamster-studio/connections) falls back to read-only mode and the sync toggle is disabled.

## Sync Badges and Task Links

[Tasks](https://tryhamster.com/docs/hamster-studio/tasks), [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), and [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) that have synced display a Linear badge with the external identifier (for example, `LIN-123`). Click the badge to jump straight to the Linear issue, project, or initiative.

Linear issues created from Hamster [Plans](https://tryhamster.com/docs/hamster-studio/plans) are also linked back — the Linear issue description includes a reference to the originating Hamster [Brief](https://tryhamster.com/docs/hamster-studio/briefs).

## Status Mapping

Hamster maps [Brief](https://tryhamster.com/docs/hamster-studio/briefs), [Task](https://tryhamster.com/docs/hamster-studio/tasks), and [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) states to the closest Linear workflow state when two-way sync is enabled. The initial mapping is bootstrapped from the Linear [Team](https://tryhamster.com/docs/hamster-studio/teams) you choose during setup.

If Linear adds, renames, or removes workflow states later, Hamster reconciles the mapping during sync. Status changes still show through sync badges, so a teammate can see which Linear project, issue, or [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) mirrors the Hamster object and open it directly.

## Reconnect Without Losing Identity

Disconnecting and reconnecting Linear preserves sync identity. The original entity mappings are kept on a soft-delete tombstone, so when you reconnect the same workspace, [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) and [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) reattach to their existing Linear counterparts instead of creating duplicates.

## Keeping Data Current

Two-way sync changes propagate automatically via webhooks — no manual re-sync is needed for [Routine](https://tryhamster.com/docs/hamster-studio/routines) updates.

If your Linear workspace changes significantly (new teams, restructured projects, a major batch of issues added), trigger a manual reconciliation from the [Connection](https://tryhamster.com/docs/hamster-studio/connections) settings. **Quick Sync** pulls the latest data and reconciles drift between Hamster and Linear.

## Connection Health

Hamster surfaces [Connection](https://tryhamster.com/docs/hamster-studio/connections) health in the [Connection](https://tryhamster.com/docs/hamster-studio/connections) card and a dedicated detail sheet:

* Overview — Status, sync [Direction](https://tryhamster.com/docs/concepts/direction), last sync times, and counts of successful, failed, and skipped operations.
* Logs — Operation history with timestamps, entity types, and direction. Outbound failures capture the wire payload for debugging.
* Conflicts — Any pending field-level conflicts. Resolve them inline with **Use Linear**, **Use Hamster**, or a custom value.

If your Linear OAuth token needs reauthorisation, the card shows a reauth button — click it to refresh credentials without losing your sync state.

## Tips

* You can connect one Linear workspace per Hamster team. If your organisation uses multiple Linear workspaces, connect the one most relevant to the projects you run in this Hamster workspace.
* Enable two-way sync when you want Linear to be your team's execution view while Hamster handles planning. [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) flow from [Brief](https://tryhamster.com/docs/hamster-studio/briefs) to [Plan](https://tryhamster.com/docs/hamster-studio/plans) to Linear without manual copying.
* Linear works well alongside [GitHub](https://tryhamster.com/docs/hamster-studio/connections/github). The AI can correlate issues with the code changes that address them when both sources are connected.
* Keep priority fields current in Linear. The AI uses them to understand what work is critical when answering questions like "what are the open issues in the Onboarding project?"
* Status mapping is bootstrapped on [Connection](https://tryhamster.com/docs/hamster-studio/connections) from your Linear workflow states. If you add new states later, the mapping auto-heals — no manual reconfiguration needed.

## Related

* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)
* [Jira](https://tryhamster.com/docs/hamster-studio/connections/jira)
* [GitHub](https://tryhamster.com/docs/hamster-studio/connections/github)
* [Task Overview](https://tryhamster.com/docs/hamster-studio/tasks/task-overview)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)
* [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Connections","item":"https://tryhamster.com/docs/hamster-studio/connections"},{"@type":"ListItem","position":5,"name":"Linear","item":"https://tryhamster.com/docs/hamster-studio/connections/linear"}]}
```
