---
description: Give AI coding tools direct access to your briefs, tasks, and project context through the Model Context Protocol — no plugins, no API keys.
title: MCP Server | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

MCP Server

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
   * [Getting Started](https://tryhamster.com/docs/hamster-studio/mcp/getting-started "Getting Started")  
   * [Available Tools](https://tryhamster.com/docs/hamster-studio/mcp/available-tools "Available Tools")

* [Taskmaster](https://tryhamster.com/docs/taskmaster "Taskmaster")
* Workspace

* Teams

* Collaboration

* Account Settings

# MCP Server

_Give AI coding tools direct access to your [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), and project context through the Model Context Protocol — no plugins, no API keys, just a URL._

## Overview

The Hamster [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) lets AI coding assistants — Claude Code, Cursor, Windsurf, Codex, and others that support the Model Context Protocol — read and manage your Hamster project directly. Instead of pasting [Task](https://tryhamster.com/docs/hamster-studio/tasks) descriptions into your AI tool, you connect it to Hamster once and the tool can browse your [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), check [Task](https://tryhamster.com/docs/hamster-studio/tasks) details, create subtasks, and update status on its own.

The server exposes 20 tools covering accounts, [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), subtasks, documents, and plans. All access goes through your authenticated session and respects the same permissions you have in the browser. There are no admin keys involved — every call runs as you, scoped to your team's data.

Connecting is a single URL. Your AI tool follows a standard OAuth sign-in the first time you use it; subsequent calls are automatic.

## What's in this section

* [Getting Started](https://tryhamster.com/docs/hamster-studio/mcp/getting-started) — Connect your AI coding tool to Hamster in under a minute
* [Available Tools](https://tryhamster.com/docs/hamster-studio/mcp/available-tools) — The full list of 20 tools your AI tool can use

## How Authentication Works

Hamster's [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) uses OAuth 2.1 — the same standard your IDE already speaks. The first time your AI tool calls a Hamster tool:

1. The tool sees that it needs to authenticate and looks up Hamster's OAuth configuration via a [Discovery](https://tryhamster.com/docs/concepts/discovery) endpoint at `/.well-known/oauth-protected-resource`. This is a public, machine-readable record that tells the tool where to send you for sign-in.
2. The tool opens your browser to Hamster's consent page.
3. You sign in (or confirm if you are already signed in) and approve the connection.
4. The browser hands a session token back to your AI tool.
5. Every subsequent call runs as you, with your team-account permissions enforced server-side.

Most AI tools handle this flow automatically — you just see the browser pop open the first time. If your tool does not support automatic OAuth [Discovery](https://tryhamster.com/docs/concepts/discovery), you can still paste a Bearer token manually.

The [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) never holds an admin key or service-role credential. Every tool call carries your token, which means a Reviewer cannot accidentally edit a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) from inside their AI assistant just because the assistant tried to.

## Related

* [CLI Sync](https://tryhamster.com/docs/hamster-studio/cli/cli-sync)
* [CLI Authentication](https://tryhamster.com/docs/hamster-studio/cli/cli-authentication)
* [Slash Commands](https://tryhamster.com/docs/hamster-studio/cli/slash-commands)
* [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents)
* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Mcp","item":"https://tryhamster.com/docs/hamster-studio/mcp"}]}
```
