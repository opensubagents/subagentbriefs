---
description: Paste a meeting URL and the agent joins the call. After it ends, a brief lands in Hamster with the transcript, summary, and follow-ups.
title: Meeting Agent | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Meeting Agent

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

# Meeting Agent

_Paste a meeting URL and the agent joins the call. Twenty minutes after the meeting ends, a fresh [Brief](https://tryhamster.com/docs/hamster-studio/briefs) lands in Hamster — with the transcript, summary, decisions, and follow-ups already wired into your [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph)._

## Overview

The Meeting Agent turns spoken context into a first-class Hamster artefact. You hand it a meeting link from Google Meet, Zoom, or Microsoft Teams. It joins the call, records the transcript, and once the meeting ends it generates a structured AI summary, creates a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and document, links it to the right [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives), and posts a notification back to the channel where you started.

This is the input pipe most aligned with how founders already work: "I talk to customers, then I build." Customer calls and team meetings are the highest-signal source of refinement context — and historically the hardest thing to get into Hamster. The Meeting Agent closes that gap. It also reinforces the way teams capture interviews and customer stories: those conversations get a structured home rather than dying in Notion or Otter.

The flow is asynchronous and fault-tolerant. Each stage — agent dispatch, transcript fetch, summary generation, [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph) linking, Slack notification — runs as its own job with retries, so a transient failure on one step doesn't drop the whole capture.

## How It Works

1. Submit a meeting URL — Open the command palette (`Cmd+K`) and pick **Join Meeting**, or use the Hamster Slack bot. Paste the meeting link and click **Join**.
2. The agent joins the call — The Meeting Agent connects within seconds, appears as a participant, and records audio for the duration of the call. You can leave the agent running while you focus on the conversation.
3. The meeting ends — When the call wraps, the agent leaves automatically. No "save before quit" step.
4. Transcript and summary land — A few minutes later, Hamster pulls the transcript and runs it through structured AI summary generation. The output includes a meeting title, identified participants, decisions, action items, strategic insights, and a concise markdown summary.
5. A [Brief](https://tryhamster.com/docs/hamster-studio/briefs) appears in your workspace — Hamster creates a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and document seeded with the summary. The [Brief](https://tryhamster.com/docs/hamster-studio/briefs) is linked to mentioned [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) and [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) in your [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph) automatically, so it shows up in the right places.
6. Slack pings you — If you started from Slack, the notification posts as a thread reply in the originating channel. Otherwise it lands in your default notifications surface. The ping includes the meeting title, top action items, decision count, and a deep link to the full summary in Hamster.

## What the Summary Captures

Every meeting summary is structured so your [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph) can use it:

* Meeting title — A short, human-readable name.
* Participants — Speakers identified from the transcript.
* Action items — Each with a [Task](https://tryhamster.com/docs/hamster-studio/tasks), optional owner, and optional due date.
* Decisions — What was decided, and which participants were involved.
* Insights — Strategic themes, risks, and opportunities surfaced in the call.
* Mentioned [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) and [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) — Names and IDs that fuzzy-match into your existing [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) and tasks.

The full transcript is preserved alongside the summary, so you can always go back to the raw conversation.

## Where Transcripts Land

Each meeting becomes a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) in your workspace, and the document inside that [Brief](https://tryhamster.com/docs/hamster-studio/briefs) holds the formatted summary. The transcript itself lives on the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and can be referenced by the AI when answering questions about the meeting.

Mentioned [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) are matched against your existing [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) titles. When there's a hit, the new [Brief](https://tryhamster.com/docs/hamster-studio/briefs) is linked to that [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) — so the meeting shows up under the right strategic theme without anyone wiring it manually. Mentioned [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are linked the same way.

This means a customer call about your onboarding redesign automatically appears connected to the Onboarding [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives), and the action items reference the right tasks.

## Starting from Slack

If you have the [Slack bot](https://tryhamster.com/docs/hamster-studio/connections/slack) connected, you can dispatch the Meeting Agent directly from a channel or DM. The summary notification posts as a thread reply in the same conversation, so the Slack thread becomes a permanent record of the meeting and its outcomes — with a deep link back to the full [Brief](https://tryhamster.com/docs/hamster-studio/briefs) in Hamster.

If the originating thread is no longer accessible, the notification falls back to a fresh post in the channel.

## Privacy and Security

* **Workspace admins control the agent.** Only users with workspace **settings.manage** permission can dispatch a Meeting Agent. Other roles can read the resulting [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) once they're created.
* **Credentials are encrypted.** API keys for the meeting provider are stored in the Hamster vault and never appear in job payloads, logs, or client responses.
* **Meeting URLs are not logged.** Meeting links can contain join codes and passcodes, so Hamster only logs the hostname for debugging.
* **Webhooks are signed.** Inbound transcript events are verified with a timing-safe HMAC check, so only your meeting provider can deliver transcripts back to your workspace.
* **Standard team permissions apply.** Meeting [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) follow the same role-based access rules as any other [Brief](https://tryhamster.com/docs/hamster-studio/briefs) — only members of your Hamster team can read them.

Tell participants the agent is recording. Most meeting providers also display a recording indicator while the agent is in the call.

## Supported Meeting Providers

The Meeting Agent accepts URLs from:

* Google Meet
* Zoom
* Microsoft Teams

URLs are validated client-side before the agent is dispatched, so you'll see an error immediately if you paste a link from an unsupported provider.

## Tips

* Submit the URL a minute or two before the meeting starts so the agent has time to join. Joining late is fine — the agent records from the moment it connects.
* Keep meeting names in your calendar consistent with [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) names. The summary's "mentioned [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives)" matcher fuzzy-matches against [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) titles, so consistent naming improves auto-linking.
* Use the Slack dispatch path for customer calls. The thread reply gives non-Hamster stakeholders a one-click way to read the full summary without an account switch.
* If a transcript fails to process, check the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) — failure state is captured on the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) itself with the last error, and you can re-dispatch from the same meeting URL.

## Related

* [Slack](https://tryhamster.com/docs/hamster-studio/connections/slack)
* [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)
* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Connections","item":"https://tryhamster.com/docs/hamster-studio/connections"},{"@type":"ListItem","position":5,"name":"Meeting Agent","item":"https://tryhamster.com/docs/hamster-studio/connections/meeting-agent"}]}
```
