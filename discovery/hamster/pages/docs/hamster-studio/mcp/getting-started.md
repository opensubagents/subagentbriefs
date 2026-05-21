---
description: Connect your AI coding tool to Hamster in under a minute — single URL, OAuth sign-in, no plugins or API keys.
title: Getting Started with the MCP Server | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Getting Started

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

# Getting Started with the MCP Server

_Connect your AI coding tool to Hamster in under a minute._

## Overview

The Hamster [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) uses Streamable HTTP, which means connecting is a single URL — no plugins, no binary installs, no API keys. Add the URL to your tool's configuration, sign in once through your browser, and your AI assistant has full access to your project.

Every call runs as you, scoped to the team accounts and roles you already have in Hamster. There is no admin key to leak, no separate user to manage, and no per-session setup once the initial sign-in is complete.

## How It Works

1. Add the server URL — Open your AI tool's MCP configuration file (usually `.mcp.json` in your project root, or the tool's global settings) and add:  
```json  
{  
  "mcpServers": {  
    "hamster": {  
      "url": "https://tryhamster.com/mcp"  
    }  
  }  
}  
```
2. Trigger an authenticated call — The first time your AI tool calls a Hamster tool, it gets back an OAuth challenge that points to Hamster's [Discovery](https://tryhamster.com/docs/concepts/discovery) endpoint. The tool reads the [Discovery](https://tryhamster.com/docs/concepts/discovery) record (`/.well-known/oauth-protected-resource`), opens your browser to Hamster's consent page, and asks you to sign in.
3. Approve and return — Sign in with your normal Hamster credentials and approve the connection. The browser hands a session token back to your AI tool. From this point on, calls are automatic.
4. Start using tools — Your AI tool can now call any of the 20 Hamster tools. For example, asking "what are my current [Tasks](https://tryhamster.com/docs/hamster-studio/tasks)?" triggers `list_tasks` and returns your [Task](https://tryhamster.com/docs/hamster-studio/tasks) list as structured data.

## Supported Tools

Claude Code, Cursor, Windsurf, Codex, and any other tool that supports MCP's Streamable HTTP transport with OAuth 2.1 can connect. The only requirement is that the tool can make outbound HTTPS requests to `tryhamster.com`.

If your tool does not support automatic OAuth [Discovery](https://tryhamster.com/docs/concepts/discovery) yet, you can paste a Bearer token manually instead — the server accepts a Hamster session token in the `Authorization: Bearer …` header.

## Key Capabilities

* **Full project access**: Your AI tool can read [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), browse [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), check [Plans](https://tryhamster.com/docs/hamster-studio/plans), and look up documents — the same information you see in the browser.
* **Write access**: The tool can also create [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), add [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), update status, and manage subtasks. This is useful when you want the AI to track its own progress or break work into smaller pieces.
* **Account switching**: If you belong to multiple team accounts, the tool can switch between them using `switch_account`. The session keeps track of the active account on its own.
* **Permission-scoped**: The server uses your personal session. You only see data you have access to, and team permissions are enforced the same way as in the browser. A Reviewer's AI assistant cannot create [Briefs](https://tryhamster.com/docs/hamster-studio/briefs); a Creator's can.
* **OAuth [Discovery](https://tryhamster.com/docs/concepts/discovery)**: Modern AI tools auto-discover Hamster's OAuth setup from a single URL. No manual client registration required.
* **Stateless**: Each call carries the auth token, so opening and closing [Connections](https://tryhamster.com/docs/hamster-studio/connections) is cheap. Tools can run multiple sessions in parallel without conflicting state.

## Local Development

If you are running Hamster Studio locally, point your MCP configuration at the local proxy:

```json
{
  "mcpServers": {
    "hamster": {
      "url": "http://localhost:8080/mcp"
    }
  }
}

```

The local server starts automatically when you run `pnpm dev` from the Hamster Studio repository.

## Tips

* Ask your AI tool to "check my Hamster [Tasks](https://tryhamster.com/docs/hamster-studio/tasks)" or "what's the next [Task](https://tryhamster.com/docs/hamster-studio/tasks) on my [Brief](https://tryhamster.com/docs/hamster-studio/briefs)?" to trigger the relevant tools naturally.
* If your session expires, the tool will open your browser again to re-authenticate. This happens transparently — no need to re-edit your config.
* You can connect the [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) and the [CLI sync](https://tryhamster.com/docs/hamster-studio/cli/cli-sync) at the same time. The [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp) gives your AI tool live API access; the [CLI](https://tryhamster.com/docs/hamster-studio/cli) sync gives it local markdown files. They complement each other.
* If you connect a tool that does not yet handle OAuth [Discovery](https://tryhamster.com/docs/concepts/discovery), paste a Bearer token manually and revisit when the tool catches up. Hamster supports both flows so you do not have to wait.
* Switching team accounts inside the AI tool (via `switch_account`) does not affect the team you have selected in the browser. They run on independent sessions.

## Related

* [Available Tools](https://tryhamster.com/docs/hamster-studio/mcp/available-tools)
* [MCP Server Overview](https://tryhamster.com/docs/hamster-studio/mcp)
* [CLI Sync](https://tryhamster.com/docs/hamster-studio/cli/cli-sync)
* [Slash Commands](https://tryhamster.com/docs/hamster-studio/cli/slash-commands)
* [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Mcp","item":"https://tryhamster.com/docs/hamster-studio/mcp"},{"@type":"ListItem","position":5,"name":"Getting Started","item":"https://tryhamster.com/docs/hamster-studio/mcp/getting-started"}]}
```
