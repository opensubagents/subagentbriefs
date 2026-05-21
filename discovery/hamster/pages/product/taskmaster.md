---
description: Give your AI agents structure. Parse PRDs, manage dependencies, and ship code that matches requirements. CLI-first, open source, works with any AI IDE.
title: Taskmaster — Structured task management for AI agents | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Taskmaster

# Structure for AI. Sanity for you.

AI agents are fast but directionless. Taskmaster gives them a structured task list with dependencies, context, and acceptance criteria — so they build what you actually need.

[Read the docs](https://github.com/eyaltoledano/claude-task-master#readme)

`curl -sSL https://tryhamster.com/cli/install | bash`

zsh — taskmaster

→\~/hamstertm list

IDPRIORITYTITLESTATUS

ABC-120lowSetup repo structure✓ done

ABC-123highImplement OAuth Flow○ pending

└— 123.1\-Setup Google Strategy○ pending

ABC-124mediumUser Dashboard UI! blocked

## Stop building the wrong thing fast.

The tools are powerful, but the workflow is broken.

Linear

Figma

Slack

GitHub

⚠️ Context Switching...

### Context Hunting

You spend more time jumping between Linear tickets, Figma designs, and Slack threads than actually coding.

prompt: "Build auth system"

Auth0?

JWT?

Firebase?

AI deciding implementation details...

### AI Decides How

A simple prompt leaves the implementation details to the AI. Without a plan, it builds the wrong thing, fast.

Intent

tm next

Shipped

### No Standard Flow

Vibe coding is fun for side projects. But teams need a predictable path from intent to shipped code.

zsh — taskmaster

requirements.txt (PRD)

Build a user authentication system with email/password and OAuth...

Workflow

## PRD → Tasks → Subtasks → Done

Start with requirements. End with shipped code. Taskmaster manages everything in between.

[tm parse-prdTurn any doc into structured tasks](https://tryhamster.com/product/taskmaster/parse-prd)[tm expandBreak complex tasks into subtasks](https://tryhamster.com/product/taskmaster/expand)

`tm next`

Get the next task with full context

`tm set-status`

Track progress as you ship

Complexity Analysis

## Know what needs to be broken down.

tm analyze-complexity scores each task 1–10 and recommends which ones to expand. Stop guessing. Let AI tell you where the risk is.

[Explore Complexity Analysis→](https://tryhamster.com/product/taskmaster/complexity)

zsh — taskmaster

→tm analyze-complexity

Analyzing 5 tasks...

1.

Setup repo structure

2

2.

Implement OAuth

7

3.

Build payment system

9

4.

Add user dashboard

5

5.

Write unit tests

3

⚠️ Recommend expansion: Tasks 2, 3 (complexity ≥ 7)

Research

## Fresh info beyond the cutoff.

AI models have knowledge cutoffs. tm research queries live sources for the latest best practices, security patches, and library updates.

[Explore Research→](https://tryhamster.com/product/taskmaster/research)

zsh — taskmaster

→tm research "React Query v5 best practices"

Autopilot

## Test-driven development on autopilot.

A state machine that runs the full Red → Green → Refactor cycle. Creates branches, runs tests, retries on failure. You review. It ships.

zsh — taskmaster

→\~/repotm autopilot start ABC-123

\[autopilot\] Initializing TDD workflow for task ABC-123...

\[autopilot\] Created branch task/abc-123-oauth

## Local or connected. Your choice.

Taskmaster works standalone with your own API keys. Connect to Hamster for team sync and hosted AI.

### Local Mode

Fully offline, your keys

* Parse PRDs locally with `tm parse-prd`
* Tasks stored in `.taskmaster/` directory
* Bring your own API key (Anthropic, OpenAI, Gemini, Ollama, etc.)
* Works with Claude Code & Gemini CLI (no key needed)

Configure via `tm models --setup`

### Connected to Hamster

Team sync, hosted AI

* Briefs become tasks via `tm briefs`
* Sync local work to cloud with `tm export`
* No API keys needed — inference via Hamster
* Invite teammates to collaborate on briefs

Your PM plans in Hamster, you execute in terminal

Hamster Sync

## Briefs become tasks in seconds.

Pull down team plans instantly. No context switching. No copy-pasting requirements from Notion.

zsh — taskmaster

→\~/projecttm briefs

Tagged Task Lists

## Isolated contexts for branches.

Working on multiple features? Use tags to keep task lists separate. No merge conflicts. No crossed wires. Switch contexts instantly.

NEXT TASK

ID: ABC-123

### Implement Auth

Set up the authentication flow using Supabase Auth. Include email/password and Google provider.

Priority

High

Complexity

5/10

Suggested Actions

→tm set-status -s in-progress

→tm show --json | cursor

Integrations

## Works where you work.

CLI-first means it works everywhere. Native MCP support for AI IDEs.

[Explore MCP Server→](https://tryhamster.com/product/taskmaster/mcp-server)

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

Open Source

## Open source. Always.

Taskmaster is MIT licensed. Read the code, contribute, fork it. The core will always be free.

[Star on GitHub](https://github.com/eyaltoledano/claude-task-master)[View Changelog](https://tryhamster.com/latest?tags=taskmaster)

[25k+GitHub Stars](https://github.com/eyaltoledano/claude-task-master)[1.5M+npm Downloads](https://www.npmjs.com/package/task-master-ai)

Also in Taskmaster

## Everything else you need.

[PRD ParserTransform requirements docs into structured, executable tasks with dependencies and priorities.](https://tryhamster.com/product/taskmaster/parse-prd)[Complexity AnalysisAI scores each task 1–10 for complexity and recommends which ones to break down before you start.](https://tryhamster.com/product/taskmaster/complexity)[Task ExpansionAutomatically expand high-level tasks into detailed subtasks with file references and acceptance criteria.](https://tryhamster.com/product/taskmaster/expand)[Research ToolQuery live sources for the latest best practices, security patches, and library updates.](https://tryhamster.com/product/taskmaster/research)[MCP ServerExpose every CLI command as an MCP tool your AI coding assistant can call directly.](https://tryhamster.com/product/taskmaster/mcp-server)[Bring Your Own Key15+ AI providers, zero-key CLI tools, local models, or zero-config when connected to Hamster.](https://tryhamster.com/product/taskmaster/byok)

From Taskmaster to Studio

## Taskmaster proved planning helps. Studio is where your team aligns.

Taskmaster gives individual developers structured task management for AI agents. Studio brings the whole team into the picture — collaborative briefs, real-time alignment, and a shared plan everyone executes against.

Already using Taskmaster? Studio is where your team aligns before agents execute. The CLI connects both.

[Explore Hamster Studio→](https://tryhamster.com/product/studio)

Taskmaster

Solo developer + AI agent

Parse PRDs, manage tasks, execute with your coding agent. Works offline with your own API keys.

↓

Hamster Studio

Team alignment + AI execution

Collaborative briefs, real-time editing, team plans, issue tracker sync, and the same CLI your agents already use.

## Give your AI agents structure.

Install Taskmaster in seconds. Start shipping code that actually matches the requirements.

[View on GitHub](https://github.com/eyaltoledano/claude-task-master)[Read the Docs](https://github.com/eyaltoledano/claude-task-master#readme)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Product","item":"https://tryhamster.com/product"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/product/taskmaster"}]}
```
