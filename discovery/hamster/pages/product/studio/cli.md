---
description: Hamster syncs your briefs, tasks, and plans into your repo as markdown files in real time. Your coding agent reads them on every action.
title: Agent Context — Hamster CLI | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

[Studio](https://tryhamster.com/product/studio)/Agent Context

# Your agent already knows what to build.

Your agent doesn't just get a task description. It gets the brief, the reasoning, the team's decisions, and the acceptance criteria — synced into your repo as markdown files in real time.

zsh — hamster

![Claude Code](https://tryhamster.com/_site/images/logos/claude_icon.svg?v=6)Claude Code![Cursor](https://tryhamster.com/_site/images/logos/cursor.svg?v=6)Cursor![Gemini CLI](https://tryhamster.com/_site/images/logos/gemini.svg?v=6)Gemini CLI![Codex CLI](https://tryhamster.com/_site/images/logos/codex.svg?v=6)Codex CLI

\> "Let's build the auth feature"

Reading .hamster/briefs/auth.md ...

Reading .hamster/briefs/auth/tasks/HAM-102.md ...

I can see 3 acceptance criteria and a method

for error handling. Starting with session management.

tryhamster.com

Brief/Plan/Context

### Auth Feature

Ready5 tasks

HAM-101Audit current auth flow3/3![Colin Thornton](https://tryhamster.com/_site/_site/avatars/colin_thornton.webp?v=6)

HAM-102Design session management1/3

![Claude Code](https://tryhamster.com/_site/images/logos/claude_icon.svg?v=6)

HAM-103Wireframe token refresh flow0/2![Azikara](https://tryhamster.com/_site/_site/avatars/Azikara.jpg?v=6)

HAM-104Design team invitation screen0/4

![Codex](https://tryhamster.com/_site/images/logos/codex.svg?v=6)

HAM-105Implement role-based access0/3

![Gemini](https://tryhamster.com/_site/images/logos/gemini.svg?v=6)

Compatibility and optionality

## One Hamster, any CLI, IDE, or model.

[![Claude Code](https://tryhamster.com/_site/images/logos/claude.svg?v=6)](https://tryhamster.com/for/claude-code)[![Codex](https://tryhamster.com/_site/images/logos/codex.svg?v=6)](https://tryhamster.com/for/codex)[![Gemini](https://tryhamster.com/_site/images/logos/gemini.svg?v=6)](https://tryhamster.com/for/gemini)[![Cursor](https://tryhamster.com/_site/images/logos/cursor.svg?v=6)](https://tryhamster.com/for/cursor)[![Copilot](https://tryhamster.com/_site/images/logos/copilot.svg?v=6)](https://tryhamster.com/for/copilot)[![Windsurf](https://tryhamster.com/_site/images/logos/windsurf.svg?v=6)](https://tryhamster.com/for/windsurf)[![Cline](https://tryhamster.com/_site/images/logos/cline.svg?v=6)](https://tryhamster.com/for/cline)[![Roo Code](https://tryhamster.com/_site/images/logos/roo.svg?v=6)](https://tryhamster.com/for/roo-code)[![Aider](https://tryhamster.com/_site/images/logos/aider.svg?v=6)](https://tryhamster.com/for/aider)[![Amp](https://tryhamster.com/_site/images/logos/amp.svg?v=6)](https://tryhamster.com/for/amp)[![Grok](https://tryhamster.com/_site/images/logos/grok.svg?v=6)](https://tryhamster.com/for/grok)

![Taskmaster](https://tryhamster.com/_site/images/logos/taskmaster.svg?v=6)

When your briefs, plans, and tasks live inside a vendor's tool, switching costs are brutal. A better model drops and you're stuck — or you start over.

Hamster is the central repository of work, not the model. Briefs and plans stay in one place. The agent is interchangeable. Use Claude for deep reasoning, Gemini for speed, an open-weight model for sensitive code — or a different model for every task on the board.

New frontier model ships on Tuesday? Point it at your `.hamster/` directory and keep going.

MCP

## Agents write back too.

The Hamster MCP server gives your agent 20 tools to mark tasks done, create subtasks, and update status — directly from the coding session. When the agent finishes a task, it updates the plan. No one has to do it manually.

zsh — hamster mcp

\> hamster mark-done HAM-102

 ✓ Task HAM-102 marked done in Hamster Studio

 ✓ Plan progress: 9/12 tasks complete

20 tools available — tasks, briefs, blueprints, skills, methods

Install

## One command to install.

Install the Hamster CLI, initialize your repo, and start working. Your agent has full project context from the first prompt.

`curl -sSL https://tryhamster.com/cli/install | bash`

01

Install the CLI

Run the install command and authenticate with your Hamster workspace. Under a minute.

02

Initialize your repo

Run \`hamster init\`. Creates a .hamster/ directory and starts syncing your project context.

03

Work normally

Open your coding agent. The context files are already there. Ask it to build something — it knows what that means.

Key capabilities

### The full brief, not just a title

The difference between "implement auth" and a brief with the strategy, constraints, compliance requirements, and team decisions. Your agent gets the latter.

### 20 MCP tools built in

Mark tasks done, create subtasks, update status — all from the coding session.

### Works offline

Context files are local. Your agent reads them even without a network connection.

### Any MCP-compatible agent

One server, every tool. Claude Code, Cursor, Gemini CLI, Codex, and more.

### Skill file generation

The CLI generates structured project maps so your agent understands the full codebase.

### No new workflow

You don't pull context in. It's just there. Work the way you already work.

## Wire your agent into the plan.

Free to start. No credit card required.

[Get started free](https://tryhamster.com/auth/sign-up)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Product","item":"https://tryhamster.com/product"},{"@type":"ListItem","position":3,"name":"Studio","item":"https://tryhamster.com/product/studio"},{"@type":"ListItem","position":4,"name":"Cli","item":"https://tryhamster.com/product/studio/cli"}]}
```
