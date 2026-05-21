---
description: Connect Google Drive so the AI can search files and documents as Context Graph grounding.
title: Google Drive | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Google Drive

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

# Google Drive

Connect Google Drive so the AI can search your files and documents as context.

_This feature may need to be enabled for your workspace._

## Overview

The Google Drive [Connection](https://tryhamster.com/docs/hamster-studio/connections) lets the AI search the files in your Google Drive when answering questions or generating briefs. This covers files in My Drive and any shared drives you have access to, including Google Docs and other document types.

Rather than syncing all your Drive content upfront, the AI searches Google Drive at the time you ask a question, so you always get [Results](https://tryhamster.com/docs/hamster-studio/results) from the current state of your files.

The [Connection](https://tryhamster.com/docs/hamster-studio/connections) uses Google OAuth — you authorize with your Google account and the integration uses the permissions you grant.

## What the AI Can Access

* Files — Files in My Drive and shared drives you have access to
* Google Docs — Document content from Docs files
* Shared drives — Files in team-level shared drives your account can see

Access is scoped to what your Google account can see. Files shared with specific people that you don't have access to are not included.

## How to Connect

1. Go to **Settings > [Connections](https://tryhamster.com/docs/hamster-studio/connections)** and click the **Google Drive** card.
2. In the dialog, click **Connect with Google**.
3. You are redirected to Google's authorization page.
4. Choose the Google account to connect.
5. Review the permissions and click **Allow**.
6. You are returned to Hamster Studio. The [Connection](https://tryhamster.com/docs/hamster-studio/connections) is ready immediately.

The [Connection](https://tryhamster.com/docs/hamster-studio/connections) is named after the Google account used to authorize.

## Permissions Requested

Hamster requests read access to your Google Drive files and metadata. This includes the ability to read file contents and file metadata. No write permissions are requested. Google displays the full list of requested permissions on the authorization screen before you confirm.

## How Drive Search Works

Google Drive uses live search rather than upfront indexing. When the AI needs Drive context, it queries your Drive at that moment and returns the most relevant results. This means:

* The [Connection](https://tryhamster.com/docs/hamster-studio/connections) is active immediately after authorizing — there is no sync to wait for.
* [Results](https://tryhamster.com/docs/hamster-studio/results) always reflect the current state of your Drive.
* The AI searches file names and content, not just file names.

## Tips

* Connect with the Google account that has access to the files most relevant to your projects. If important documents are in a shared drive, make sure that account has access to that shared drive.
* Google Drive search works well for finding specific documents, reference material, and team files. For structured project management data, Linear or Jira is a better fit.
* If you have documents in multiple Google accounts, you can add multiple Google Drive [Connections](https://tryhamster.com/docs/hamster-studio/connections) — one per account.

## Related

* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)
* [Notion](https://tryhamster.com/docs/hamster-studio/connections/notion)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Connections","item":"https://tryhamster.com/docs/hamster-studio/connections"},{"@type":"ListItem","position":5,"name":"Google Drive","item":"https://tryhamster.com/docs/hamster-studio/connections/google-drive"}]}
```
