---
description: Taskmaster runs as an MCP server, exposing all CLI commands as tools your AI agent can use directly. Works with Cursor, Windsurf, Claude Code, and more.
title: MCP Server — Taskmaster | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

[Taskmaster](https://tryhamster.com/product/taskmaster)/MCP Server

# Works inside your AI IDE.

Taskmaster runs as an MCP server, exposing all CLI commands as tools your AI agent can use directly. Native integration with Cursor, Windsurf, Claude Code, and more.

Setup

## Quick setup

Add one config file to your editor and Taskmaster connects as an MCP server. Your AI agent gets full access to every command.

.cursor/mcp.json

{
  "mcpServers": {
    "taskmaster": {
      "command": "npx",
      "args": ["-y", "task-master-ai"],
      "env": {
        "ANTHROPIC_API_KEY": "your-key"
      }
    }
  }
}

Editors

## Works where you code

Any editor that supports MCP can use Taskmaster tools. Native integration with Cursor, VS Code, Windsurf, Claude Code, and any terminal.

Cursor

MCP

VS Code

MCP

Windsurf

MCP

Claude Code

Native

Any Terminal

CLI

Tools

## Every command becomes a tool

Your AI agent reads tasks, implements code, updates status, and grabs the next task — all within your normal coding flow. The full Taskmaster CLI is available as MCP tools.

`get_tasks`

List all tasks with status

`get_task`

Get details for a specific task

`next_task`

Find the next task to work on

`set_task_status`

Update task status

`add_task`

Create new tasks with AI

`expand_task`

Break down tasks into subtasks

`parse_prd`

Generate tasks from documents

`research`

Query live sources

`analyze_complexity`

Score task complexity

Key capabilities

* Every CLI command exposed as an MCP tool
* Native integration with major AI editors
* One config file setup
* Agent reads, implements, and updates automatically
* Works alongside any MCP-compatible tool
* Full CLI parity — no features left behind

Related features

[Bring Your Own Key](https://tryhamster.com/product/taskmaster/byok) — Configure the AI provider your MCP server uses.

[Task Expansion](https://tryhamster.com/product/taskmaster/expand) — Available as expand\_task tool.

[Research](https://tryhamster.com/product/taskmaster/research) — Available as research tool.

## Connect your AI IDE.

One config file. Full Taskmaster access.

[Get started](https://github.com/eyaltoledano/claude-task-master#readme)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Product","item":"https://tryhamster.com/product"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/product/taskmaster"},{"@type":"ListItem","position":4,"name":"Mcp Server","item":"https://tryhamster.com/product/taskmaster/mcp-server"}]}
```
