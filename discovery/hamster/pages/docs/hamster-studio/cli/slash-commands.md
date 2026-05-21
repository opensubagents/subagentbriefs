---
description: Run Hamster delivery commands directly from your AI coding agent — `/ship` a brief, sync your skills, and drive workflow without alt-tabbing.
title: Slash Commands | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Slash Commands

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
   * [CLI Sync](https://tryhamster.com/docs/hamster-studio/cli/cli-sync "CLI Sync")  
   * [Getting Started](https://tryhamster.com/docs/hamster-studio/cli/cli-authentication "Getting Started")  
   * [Using the CLI](https://tryhamster.com/docs/hamster-studio/cli/cli-brief-creation "Using the CLI")  
   * [Slash Commands](https://tryhamster.com/docs/hamster-studio/cli/slash-commands "Slash Commands")

* MCP Server

* [Taskmaster](https://tryhamster.com/docs/taskmaster "Taskmaster")
* Workspace

* Teams

* Collaboration

* Account Settings

# Slash Commands

_Run Hamster [Delivery](https://tryhamster.com/docs/concepts/delivery) commands directly from your AI coding agent — `/ship` a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), sync your skills, and drive workflow without alt-tabbing back to the browser._

## Overview

Slash commands are short verbs your AI coding agent recognizes when it is working in a Hamster-synced repo. They live in the agent surface (Claude Code's command palette, for example) and call into the Hamster [CLI](https://tryhamster.com/docs/hamster-studio/cli) under the hood. Because they are wired up by the [CLI](https://tryhamster.com/docs/hamster-studio/cli) itself — not authored in your repo — the list of available commands stays current with every `hamster sync`.

The most important slash command is `/ship`. It is how Hamster's cloud [Delivery](https://tryhamster.com/docs/concepts/delivery) agents pick up a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and drive it to a pull request. Other slash commands cover sync hygiene, skill management, and quick lookups.

## How It Works

1. Sync your repo — Run `hamster sync` (or `hamster sync --watch`) at least once. The [CLI](https://tryhamster.com/docs/hamster-studio/cli) generates a Claude skill at `.claude/skills/hamster-project-context/SKILL.md` that registers the available slash commands inside Claude Code.
2. Open your agent — Start a session in Claude Code, Cursor, Codex, or another agent that reads from `.agents/skills/` or `.claude/skills/`. The agent picks up the Hamster skill and the commands it exposes.
3. Type the command — In Claude Code, type `/` to open the command palette, then pick a Hamster command (or type its name). Other agent surfaces use their own command UX, but the underlying commands are the same.
4. Pass arguments — Most commands take a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) identifier — a display ID like `HAM-123`, a slug, or a full Studio URL. The [CLI](https://tryhamster.com/docs/hamster-studio/cli) parses any of those formats.

## Where Slash Commands Run

| Surface                                                                 | Command UX                                                                                                                                |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Claude Code                                                             | / opens the command palette; Hamster commands appear under the hamster-project-context skill                                              |
| Cursor                                                                  | Available through the agent's command surface when the universal skills directory is connected                                            |
| Codex / Copilot / Continue / Windsurf                                   | Each agent uses its own command surface; the same skill files drive the available commands                                                |
| [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) | The cloud sandbox invokes commands like /ship non-interactively as part of [Delivery](https://tryhamster.com/docs/concepts/delivery) runs |

The slash commands themselves are generated by `hamster sync` from the skills in your workspace, so they update automatically when your team adds or changes a [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) or skill that introduces new commands.

## The Most Useful Commands

### `/ship <brief-id>`

Hands a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) to Hamster's cloud [Delivery](https://tryhamster.com/docs/concepts/delivery) system and drives it through to a pull request.

When you run `/ship HAM-123`, Hamster's sandboxed [Cloud Agent](https://tryhamster.com/docs/hamster-studio/cloud-agents):

1. Pulls the latest [Brief](https://tryhamster.com/docs/hamster-studio/briefs), [Task](https://tryhamster.com/docs/hamster-studio/tasks), and context state from your workspace using the [CLI](https://tryhamster.com/docs/hamster-studio/cli) inside the sandbox.
2. Opens the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and walks the [Task](https://tryhamster.com/docs/hamster-studio/tasks) list in priority and dependency order.
3. Drives an AI coding agent inside the sandbox to do the work, with the [Brief](https://tryhamster.com/docs/hamster-studio/briefs), [Plan](https://tryhamster.com/docs/hamster-studio/plans), [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods), and [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) all on disk as context.
4. Opens a pull request when the work is done — or pauses for clarification when it hits an ambiguous decision.

You stay in your editor while it runs. Streaming progress appears in the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s [Delivery](https://tryhamster.com/docs/concepts/delivery) thread on Hamster, and the resulting PR links back to the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) automatically.

### `hamster task status <id> <status>`

Move a [Task](https://tryhamster.com/docs/hamster-studio/tasks) to `todo`, `in_progress`, or `done` from the terminal. Useful inside agent runs where the agent should mark its own progress without leaving the shell.

```bash
hamster task assign HAM-123
hamster task status HAM-123 in_progress
# … work happens …
hamster task status HAM-123 done

```

### `hamster sync` and `hamster sync --watch`

Pull the latest [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and [Task](https://tryhamster.com/docs/hamster-studio/tasks) state into `.hamster/`. Run it once at the start of a session, or use `--watch` to keep local files in sync with what your team is doing in the browser.

When the agent cannot find a [Task](https://tryhamster.com/docs/hamster-studio/tasks) or [Brief](https://tryhamster.com/docs/hamster-studio/briefs) that you mention, the right fallback is `hamster sync` first, then look again — the local files may simply be stale.

### `hamster skills sync`

Bidirectional sync for the shared skills your AI agents read. Pulls new and updated skills from your workspace and offers to push back any skills you (or your agent) edited locally. Asset-aware — changes to bundled references and assets are detected too.

```bash
hamster skills sync                  # pull and push
hamster skills sync --pull-only      # pull only
hamster skills sync --push-only      # push only

```

If a skill changed both locally and remotely since your last sync, you will be prompted to keep local, use remote, or skip. Non-interactive runs auto-skip conflicts so nothing is force-overwritten silently.

### `hamster skills agents`

Pick which IDE or agent directories should be linked to the canonical `.agents/skills/` location. Run this once when you onboard a new agent or change tools.

### `hamster brief create`, `hamster blueprint create`, `hamster method create`

Create new [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), or [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) from the terminal. Useful when an AI agent identifies that a new [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) or [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) should exist and wants to draft one without context-switching to the browser.

```bash
hamster brief create --title "Onboarding redesign" --content "## Context..."
echo "## From stdin" | hamster brief create --title "Piped Brief" --content -

```

Always pass `--content` — the markdown is rendered straight into the Studio editor so your collaborators see it immediately.

### `hamster brief get` and `hamster task get`

Print the full content of a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or [Task](https://tryhamster.com/docs/hamster-studio/tasks) in the terminal without switching to the browser. Both accept display IDs (`HAM-123`) or UUIDs.

## Tips

* Pair `hamster sync --watch` with your editor session so `/ship`, `task get`, and `brief get` always see the latest state.
* Slash commands respect your role. A Reviewer cannot ship a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or push skill changes; the command surfaces this back as a permission error rather than failing silently.
* Skill changes pushed via `hamster skills sync` go through Hamster's review and version flow — your team can see the diff before it lands.
* The Hamster [CLI](https://tryhamster.com/docs/hamster-studio/cli) auto-checks for updates and prints a notice when a newer release is available. Run `hamster --version` if you want to check manually.
* If a slash command is missing inside Claude Code, run `hamster sync` once to regenerate the skill file.

## Related

* [CLI Authentication](https://tryhamster.com/docs/hamster-studio/cli/cli-authentication)
* [CLI Sync](https://tryhamster.com/docs/hamster-studio/cli/cli-sync)
* [CLI Brief Creation](https://tryhamster.com/docs/hamster-studio/cli/cli-brief-creation)
* [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents)
* [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Cli","item":"https://tryhamster.com/docs/hamster-studio/cli"},{"@type":"ListItem","position":5,"name":"Slash Commands","item":"https://tryhamster.com/docs/hamster-studio/cli/slash-commands"}]}
```
