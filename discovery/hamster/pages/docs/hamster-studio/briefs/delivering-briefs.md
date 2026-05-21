---
description: Ship a brief to GitHub directly from chat or the brief workspace. Hamster pre-flights your plan, dispatches the job, and links the PR back into the conversation.
title: Delivering Briefs | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Delivering Briefs

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

# Delivering Briefs

Turn a ready [Brief](https://tryhamster.com/docs/hamster-studio/briefs) into a GitHub pull request — from a conversation, or directly from the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) workspace — without leaving Hamster.

## The job delivery does

A [Brief](https://tryhamster.com/docs/hamster-studio/briefs) is only valuable when it ships. Once your [Plan](https://tryhamster.com/docs/hamster-studio/plans) is in place and your team is aligned, the next step is getting the code into a PR. Hamster handles the dispatch, tracks the agent's work live, and links the [Result](https://tryhamster.com/docs/hamster-studio/results) back into the thread where you were already working.

## Two ways to deliver

### From chat

When your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) has a [Plan](https://tryhamster.com/docs/hamster-studio/plans) and a connected GitHub repo, you can trigger [Delivery](https://tryhamster.com/docs/concepts/delivery) directly in conversation. Tell Hamster what you want to ship:

* "Ship this [Brief](https://tryhamster.com/docs/hamster-studio/briefs)"
* "Deliver to myorg/backend"
* "Ship the authentication [Brief](https://tryhamster.com/docs/hamster-studio/briefs) to the API repo"

Hamster checks that everything is ready, dispatches the job to your connected GitHub repo, and posts a [Delivery](https://tryhamster.com/docs/concepts/delivery) card in the conversation. You can keep working in chat — the [Delivery](https://tryhamster.com/docs/concepts/delivery) runs in the background and updates in real time.

### From the brief workspace

Open the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and select **Deliver** from the action bar. Pick the target repo from your connected GitHub accounts, confirm, and dispatch.

Both paths run the same pre-flight checks and use the same [Delivery](https://tryhamster.com/docs/concepts/delivery) agent. The output — a PR or branch — is identical regardless of how you triggered it.

## Before Hamster can deliver

Hamster checks four things before dispatching:

| Check                                                               | What it means                                                                                                                                                                                                                |
| ------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **[Plan](https://tryhamster.com/docs/hamster-studio/plans) exists** | The [Brief](https://tryhamster.com/docs/hamster-studio/briefs) has a generated, accepted [Plan](https://tryhamster.com/docs/hamster-studio/plans) with at least one [Task](https://tryhamster.com/docs/hamster-studio/tasks) |
| **Repo connected**                                                  | A GitHub repo is connected to your account                                                                                                                                                                                   |
| **Push access confirmed**                                           | Hamster can push to that repo                                                                                                                                                                                                |
| **No job in flight**                                                | A [Delivery](https://tryhamster.com/docs/concepts/delivery) for this [Brief](https://tryhamster.com/docs/hamster-studio/briefs) isn't already running                                                                        |

If any check fails, Hamster explains what's missing. Fix it — generate a [Plan](https://tryhamster.com/docs/hamster-studio/plans), connect a GitHub repo in Settings, or wait for the current [Delivery](https://tryhamster.com/docs/concepts/delivery) to finish — then try again.

## Watching delivery happen

A [Delivery](https://tryhamster.com/docs/concepts/delivery) thread opens as soon as the job is dispatched. The agent's work streams in live:

* Boot phases appear first — environment setup, context load
* Each step the agent takes (reading files, writing code, running checks) appears as it completes
* Tool calls and phase transitions render as distinct items so you can follow the agent's reasoning

You can leave the [Delivery](https://tryhamster.com/docs/concepts/delivery) thread and come back. The transcript persists as a permanent record of what was built and why.

## After delivery completes

When the agent finishes, the final step in the [Delivery](https://tryhamster.com/docs/concepts/delivery) thread shows the [Result](https://tryhamster.com/docs/hamster-studio/results):

* **Pull request opened: #123** — clickable link straight to the GitHub PR
* **Branch pushed: feature/my-branch** — clickable link to the GitHub compare page so you can review the diff immediately

No need to switch to GitHub to find what was shipped — the link is right there in the thread.

## If delivery fails

If the agent hits an error, the [Delivery](https://tryhamster.com/docs/concepts/delivery) thread shows the failure inline. The "View [Delivery](https://tryhamster.com/docs/concepts/delivery)" link on the [Delivery](https://tryhamster.com/docs/concepts/delivery) card stays active so you can inspect what happened. Common causes:

* A test or lint check failed during the [Delivery](https://tryhamster.com/docs/concepts/delivery) run — review the agent's output for specifics
* Push access changed — check that Hamster's GitHub [Connection](https://tryhamster.com/docs/hamster-studio/connections) is still active in Settings
* A merge conflict or branch protection rule blocked the push — the thread will describe the blocker

Fix the underlying issue and re-deliver from the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) workspace or chat.

## Related

* [Creating Briefs](https://tryhamster.com/docs/hamster-studio/briefs/creating-briefs)
* [Generating Plans](https://tryhamster.com/docs/hamster-studio/plans/generating-plans)
* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)
* [GitHub Connection](https://tryhamster.com/docs/hamster-studio/connections/github)
* [Routines](https://tryhamster.com/docs/hamster-studio/routines) — automate [Delivery](https://tryhamster.com/docs/concepts/delivery) and other recurring work with event-triggered instructions

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Briefs","item":"https://tryhamster.com/docs/hamster-studio/briefs"},{"@type":"ListItem","position":5,"name":"Delivering Briefs","item":"https://tryhamster.com/docs/hamster-studio/briefs/delivering-briefs"}]}
```
