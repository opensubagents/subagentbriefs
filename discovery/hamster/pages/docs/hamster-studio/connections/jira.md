---
description: Connect Jira Cloud so the AI can reference projects and synced Briefs can show the Jira work they map to.
title: Jira Integration — Studio Documentation | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Jira

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

# Jira

Connect Jira Cloud so the AI can reference your projects, issues, and work items.

_This feature may need to be enabled for your workspace._

## Overview

The Jira [Connection](https://tryhamster.com/docs/hamster-studio/connections) gives the AI access to your Jira Cloud instance. Once connected, the AI can answer questions about your projects, search issues, and use Jira data as context when generating [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) or responding to questions about your [Team](https://tryhamster.com/docs/hamster-studio/teams)'s work.

Like Slack and Google Drive, Jira uses live search — the AI queries Jira at the time of your request rather than syncing all data upfront. This means the AI always works with current issue data.

The [Connection](https://tryhamster.com/docs/hamster-studio/connections) uses Atlassian OAuth, so you authorize through your Atlassian account.

## What the AI Can Access

* Projects — Jira projects your account has access to
* Issues — Issues, bugs, stories, [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), and epics with their fields and descriptions
* Users — Team members in accessible projects

Access is limited to projects your Atlassian account can see. The [Connection](https://tryhamster.com/docs/hamster-studio/connections) automatically discovers all projects accessible to your account at the time of authorization.

## How to Connect

1. Go to **Settings > [Connections](https://tryhamster.com/docs/hamster-studio/connections)** and click the **Jira** card.
2. In the dialog, click **Connect with Jira**.
3. You are redirected to Atlassian's authorization page.
4. Log in with your Atlassian account and select the Jira Cloud instance to connect.
5. Review the permissions and click **Accept**.
6. You are returned to Hamster Studio. The [Connection](https://tryhamster.com/docs/hamster-studio/connections) is ready immediately.

The [Connection](https://tryhamster.com/docs/hamster-studio/connections) is named after your Jira Cloud instance (for example, "Acme Corp").

## Permissions Requested

Hamster requests read access to Jira work items and user information. Specifically:

* `read:jira-work` — Read projects and issues
* `read:jira-user` — Read user and team information

No write permissions are requested. You cannot create, update, or delete issues through the Hamster connection.

## Multiple Jira Instances

If your Atlassian account has access to more than one Jira Cloud instance, Hamster connects to the first accessible instance. If you need to connect a specific instance, use an Atlassian account that has access only to that instance, or contact support.

## How Jira Search Works

Jira uses live federated search rather than upfront syncing. When the AI needs Jira context, it queries your Jira instance directly at that moment. The [Connection](https://tryhamster.com/docs/hamster-studio/connections) shows as active immediately after authorizing with no sync delay.

Because search is live, [Results](https://tryhamster.com/docs/hamster-studio/results) always reflect the current state of your Jira board — including newly created issues, status changes, and reassignments.

## Sync Badges and Status Mapping

When a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) is mirrored to Jira, Hamster shows a Jira sync badge on the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) header. Click the badge to open the linked Jira epic or work item.

[Brief](https://tryhamster.com/docs/hamster-studio/briefs) status changes can sync to the mapped Jira status when two-way sync is enabled for your workspace. Jira status changes can also flow back to the matching [Brief](https://tryhamster.com/docs/hamster-studio/briefs). Hamster preserves local [Brief](https://tryhamster.com/docs/hamster-studio/briefs) context, alignment votes, and [Activity Timeline](https://tryhamster.com/docs/hamster-studio/briefs/activity-timeline) entries while keeping the external status visible for teams that still run execution rituals in Jira.

## Tips

* Connect with the Atlassian account that has access to the projects most relevant to your Hamster workspace. If some projects are restricted, the AI will not be able to reference them.
* Jira is most useful for [Teams](https://tryhamster.com/docs/hamster-studio/teams) tracking work in Jira alongside planning in Hamster. The AI can answer questions like "what are the open bugs in the Payments project?" or "what did we ship last sprint?"
* If you use both Jira and Linear, you can connect both. The AI draws on all connected sources when answering questions.

## Related

* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)
* [Linear](https://tryhamster.com/docs/hamster-studio/connections/linear)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Connections","item":"https://tryhamster.com/docs/hamster-studio/connections"},{"@type":"ListItem","position":5,"name":"Jira","item":"https://tryhamster.com/docs/hamster-studio/connections/jira"}]}
```
