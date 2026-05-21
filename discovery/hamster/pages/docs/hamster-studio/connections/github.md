---
description: Connect a GitHub repository so the AI can reference your code and Cloud Agents can ship pull requests against it.
title: GitHub | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

GitHub

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

# GitHub

_Connect a GitHub repository so the AI can reference your code, structure, and history — and so [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) can ship pull requests against it._

## Overview

The GitHub [Connection](https://tryhamster.com/docs/hamster-studio/connections) gives Hamster two things at once:

* **Read access for the AI.** Once connected, the AI can answer questions about the codebase, reference file structure and content when generating [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), and ground its suggestions in the repo you're actually working on.
* **A [Delivery](https://tryhamster.com/docs/concepts/delivery) target.** When you configure or launch a [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents), the GitHub [Connection](https://tryhamster.com/docs/hamster-studio/connections) is what lets the agent push commits and open pull requests against the repo.

You connect one repository at a time. You can add multiple GitHub [Connections](https://tryhamster.com/docs/hamster-studio/connections) if your project spans several repositories.

## What It Syncs

* Files and content — The contents of files in the repository at the specified branch.
* Repository structure — Directory layout and file organisation.

GitHub uses a full sync model: data is indexed on [Connection](https://tryhamster.com/docs/hamster-studio/connections) and can be refreshed manually at any time from your [Connections](https://tryhamster.com/docs/hamster-studio/connections) page.

## How to Connect

1. Go to **Workspace Settings > [Connections](https://tryhamster.com/docs/hamster-studio/connections)** and click the **GitHub** card.
2. In the dialog, fill in the following:  
   * **[Connection](https://tryhamster.com/docs/hamster-studio/connections) name** — A label for this [Connection](https://tryhamster.com/docs/hamster-studio/connections) (e.g. "Main Repository" or "Frontend").  
   * **Repository** — The repository in `owner/repo` format (e.g. `acme/web-app`).  
   * **Branch** — The branch to sync (defaults to `main`).  
   * **Personal Access Token** — A GitHub token with read-only access to the repository.
3. Click **Connect Repository**.

The [Connection](https://tryhamster.com/docs/hamster-studio/connections) appears in your active [Connections](https://tryhamster.com/docs/hamster-studio/connections) list and the data is indexed immediately.

## Creating a Personal Access Token

You need a GitHub Personal Access Token (PAT) with the following permissions:

* Contents — Read-only.
* Metadata — Read-only.

To create one:

1. Go to **GitHub > Settings > Developer settings > Personal access tokens > Fine-grained tokens**.
2. Click **Generate new token**.
3. Under **Repository access**, select the specific repository.
4. Under **Permissions**, set Contents and Metadata to Read-only.
5. Generate the token and copy it — you won't be able to see it again.

The Connect GitHub dialog includes a direct link that pre-fills these settings for the repository owner you enter.

If you intend to use the same [Connection](https://tryhamster.com/docs/hamster-studio/connections) for [Delivery](https://tryhamster.com/docs/concepts/delivery) through [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents), grant write access on **Contents** and **Pull requests** as well, so agents can push commits and open PRs.

## Multiple Repositories

If your project spans multiple repositories, add a separate GitHub [Connection](https://tryhamster.com/docs/hamster-studio/connections) for each one. Give each [Connection](https://tryhamster.com/docs/hamster-studio/connections) a descriptive name so you can identify them on the [Connections](https://tryhamster.com/docs/hamster-studio/connections) page.

## Working with Cloud Agents

GitHub [Connections](https://tryhamster.com/docs/hamster-studio/connections) are the foundation for [Delivery](https://tryhamster.com/docs/concepts/delivery) in Hamster:

* A [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) attaches one or more GitHub repos and uses them to boot a sandbox snapshot.
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), [Routines](https://tryhamster.com/docs/hamster-studio/routines), and Slack slash flows can launch [Delivery](https://tryhamster.com/docs/concepts/delivery) into any active [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) that has the right repo attached.
* The [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) executes the work in a sandbox and opens a pull request authored by the user who launched it.

Both flows resolve credentials per-request and never store them in job payloads. PRs are attributed back to the human who triggered the delivery.

## Keeping Data Current

GitHub data is synced on connection. If significant changes have been made to the codebase since you connected, trigger a manual re-sync from the [Connections](https://tryhamster.com/docs/hamster-studio/connections) page to pull in the latest content.

## Connection Health Warnings

Hamster validates token capabilities and shows warning badges when a GitHub token is missing key scopes. Common warnings include "missing push access" or "missing pull request access" — both required if the [Connection](https://tryhamster.com/docs/hamster-studio/connections) will be used for [Delivery](https://tryhamster.com/docs/concepts/delivery). Catching incomplete permissions up front avoids a failed [Delivery](https://tryhamster.com/docs/concepts/delivery) later.

## Tips

* Use descriptive [Connection](https://tryhamster.com/docs/hamster-studio/connections) names when connecting multiple repositories. "API" and "Frontend" are more useful than "Repo 1" and "Repo 2".
* Connect the branch that reflects your current active development — usually `main` or `develop`, not a feature branch.
* If the repository is private, the token must have access to that specific repo. Organisation-level tokens with broad access also work.
* The AI uses repository content as context, not as a code execution environment. It reads and references code but does not run it. Code execution happens inside [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents) sandboxes when you deliver a [Brief](https://tryhamster.com/docs/hamster-studio/briefs).
* Pair GitHub with [Linear](https://tryhamster.com/docs/hamster-studio/connections/linear) or [Jira](https://tryhamster.com/docs/hamster-studio/connections/jira) so the AI can correlate issues with the code changes that address them.

## Related

* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)
* [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents)
* [Linear](https://tryhamster.com/docs/hamster-studio/connections/linear)
* [Jira](https://tryhamster.com/docs/hamster-studio/connections/jira)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Connections","item":"https://tryhamster.com/docs/hamster-studio/connections"},{"@type":"ListItem","position":5,"name":"Github","item":"https://tryhamster.com/docs/hamster-studio/connections/github"}]}
```
