---
description: Taskmaster works with 13+ AI-powered editors and IDEs including Cursor, Claude Code, VS Code, and more. Learn how Hamster helps teams plan, build, and...
title: Supported Editors | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Supported Editors

* Welcome  
   * [Introduction](https://tryhamster.com/docs/taskmaster "Introduction")

* Getting Started

* Task Workflow

* Automation

* AI Providers

* IDE & Editor Setup  
   * [Supported Editors](https://tryhamster.com/docs/taskmaster/ide-setup/supported-editors "Supported Editors")  
   * [Rules System](https://tryhamster.com/docs/taskmaster/ide-setup/rules "Rules System")

* Team Collaboration

* Best Practices

* TDD Workflow

* Technical Capabilities

# Supported Editors

Taskmaster integrates with 13+ AI-powered editors through rules files, slash commands, and MCP server connections. Each editor gets tailored configuration so Taskmaster works natively within your workflow.

## Editor Compatibility

| Editor      | Rules                              | MCP                                | Slash Commands |
| ----------- | ---------------------------------- | ---------------------------------- | -------------- |
| Cursor      | .cursor/rules/taskmaster.mdc       | .cursor/mcp.json                   | Yes            |
| Claude Code | CLAUDE.md \+ .taskmaster/CLAUDE.md | .mcp.json                          | Yes (plugin)   |
| Windsurf    | .windsurfrules                     | .codeium/windsurf/mcp\_config.json | —              |
| VS Code     | .github/copilot-instructions.md    | .vscode/mcp.json                   | —              |
| Roo         | .roo/rules/taskmaster.md           | .roo/mcp.json                      | Yes            |
| Cline       | .clinerules/taskmaster.md          | .cline/mcp\_settings.json          | —              |
| Codex       | codex.md                           | —                                  | Yes            |
| Gemini CLI  | GEMINI.md                          | —                                  | Yes            |
| Kiro        | .kiro/rules/taskmaster.md          | .kiro/mcp.json                     | —              |
| Zed         | .zed/rules/taskmaster.md           | .zed/mcp.json                      | —              |
| Amp         | .amp/rules/taskmaster.md           | .amp/mcp.json                      | —              |
| Trae        | .trae/rules/taskmaster.md          | —                                  | —              |
| OpenCode    | AGENTS.md                          | —                                  | Yes            |

## Quick Setup

The fastest way to configure your editor:

```bash
# Auto-detect your editor and install rules
tm rules add -y

# Or specify your editor explicitly
tm rules add cursor
tm rules add claude

# Set up multiple editors at once
tm rules add cursor,claude,windsurf

```

## What Gets Installed

The `rules add` command configures three things:

1. Rules file — Instructions that teach your AI assistant how to use Taskmaster effectively (what commands to run, when to check dependencies, how to update task status)
2. MCP server config — Connects your editor to the Taskmaster MCP server for direct tool access
3. Slash commands — Editor-specific command shortcuts (where supported)

## Interactive Setup

For a guided experience:

```bash
tm rules setup

```

This auto-detects which editors you have installed and lets you select which ones to configure.

## Removing Rules

```bash
# Remove Taskmaster rules from an editor
tm rules remove cursor

```

The remove command intelligently cleans up only Taskmaster-related configuration without affecting other rules or settings.

## Claude Code Plugin

Claude Code users can also install Taskmaster as a plugin for deeper integration:

```bash
/plugin marketplace add eyaltoledano/claude-task-master
/plugin install taskmaster@taskmaster

```

The plugin provides 49 slash commands (like `/taskmaster:list-tasks`, `/taskmaster:next-task`) and 3 specialized agents for orchestrated task execution.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Ide Setup","item":"https://tryhamster.com/docs/taskmaster/ide-setup"},{"@type":"ListItem","position":5,"name":"Supported Editors","item":"https://tryhamster.com/docs/taskmaster/ide-setup/supported-editors"}]}
```
