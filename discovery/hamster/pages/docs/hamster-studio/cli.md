---
description: Pull your Hamster briefs, tasks, and skills into the same repo your AI coding agents work in — and run delivery from the terminal.
title: CLI | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

CLI

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

# CLI

_Pull your Hamster [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), and skills into the same repo your AI coding agents work in — and run [Delivery](https://tryhamster.com/docs/concepts/delivery) commands without leaving the terminal._

## Overview

The Hamster [CLI](https://tryhamster.com/docs/hamster-studio/cli) is a single Go binary that turns your Hamster workspace into local markdown your AI coding agents can read directly. [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and [Task](https://tryhamster.com/docs/hamster-studio/tasks) content land in `.hamster/`, your shared agent skills land in `.agents/skills/`, and the same paths are visible to Claude Code, Cursor, Codex, GitHub Copilot, Continue, and Windsurf — so every agent reads the same source of truth.

The [CLI](https://tryhamster.com/docs/hamster-studio/cli) is a sync engine, not an editor. Editing [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), and skills happens in Hamster (or, for skills, optionally in your repo with bidirectional sync). The [CLI](https://tryhamster.com/docs/hamster-studio/cli)'s job is to make that content show up beside your code.

## What's in this section

* [CLI Authentication](https://tryhamster.com/docs/hamster-studio/cli/cli-authentication) — Install the [CLI](https://tryhamster.com/docs/hamster-studio/cli) and connect it to your account
* [CLI Brief Creation](https://tryhamster.com/docs/hamster-studio/cli/cli-brief-creation) — Create [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) from the terminal or jump into an existing [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s context with one command
* [CLI Sync](https://tryhamster.com/docs/hamster-studio/cli/cli-sync) — Pull [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), and [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) to your local repository as markdown files
* [Slash Commands](https://tryhamster.com/docs/hamster-studio/cli/slash-commands) — Run Hamster slash commands like `/ship` from inside Claude Code and other agent surfaces

## Common Commands

| Command                           | What it does                                                                                                                                                                                                                                                                                                                                                                                        |
| --------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| hamster auth login                | Browser sign-in; stores your session in your OS keychain                                                                                                                                                                                                                                                                                                                                            |
| hamster init                      | Create .hamster/ and pick which team this repo syncs with                                                                                                                                                                                                                                                                                                                                           |
| hamster sync \[identifier\]       | Pull [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), and [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) for the active team. Accepts a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) slug, UUID, or full Studio URL |
| hamster sync --watch              | Continuous live sync — local files update as [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) change                                                                                                                                                                                                                                                                                     |
| hamster team list / team switch   | List or switch the active team account                                                                                                                                                                                                                                                                                                                                                              |
| hamster brief create              | Create a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) from the terminal                                                                                                                                                                                                                                                                                                               |
| hamster task status <id> <status> | Move a [Task](https://tryhamster.com/docs/hamster-studio/tasks) to a new status                                                                                                                                                                                                                                                                                                                     |
| hamster skills sync               | Bidirectional skill sync — pull updates and push local edits                                                                                                                                                                                                                                                                                                                                        |
| hamster skills agents             | Pick which AI agents (Claude Code, Continue, Windsurf, …) get symlinks to .agents/skills/                                                                                                                                                                                                                                                                                                           |

Run `hamster --help` for the full command tree.

## Skills Sync

The [CLI](https://tryhamster.com/docs/hamster-studio/cli) keeps your shared agent skills in sync between your repo and your workspace. `hamster skills sync` runs in both directions by default:

* Pull — Fetches new, updated, or removed skills from Hamster. A TUI selector lets you pick which to apply.
* Push — Detects skills you (or an AI agent) have edited locally and offers to send them back. Conflicts surface a `[K]eep local / [U]se remote / [S]kip` prompt before anything is overwritten.
* Asset-aware — Per-file SHA-256 fingerprints catch changes to bundled references and assets, not just the SKILL.md body.

If your IDE or agent expects skills under its own path (`.claude/skills`, `.continue/skills`, `.windsurf/skills`, etc.) instead of the universal `.agents/skills/`, run `hamster skills agents` to pick which directories should symlink to the canonical location. Hamster maintains symlinks safely — it never deletes the canonical data even if an agent directory was previously a symlink.

`hamster skills sync --pull-only` and `--push-only` flags are available when you want to scope the sync to one direction.

## Slash Commands in Agent Surfaces

The [CLI](https://tryhamster.com/docs/hamster-studio/cli) registers Hamster slash commands inside agent surfaces that support them. The most common one is `/ship`, which kicks off background [Delivery](https://tryhamster.com/docs/concepts/delivery) for a brief. Slash commands are not authored in your repo — they are generated from the skills the [CLI](https://tryhamster.com/docs/hamster-studio/cli) syncs, so the available commands stay current automatically.

See [Slash Commands](https://tryhamster.com/docs/hamster-studio/cli/slash-commands) for the full list and where each one runs.

## Where the CLI Runs

The same binary works in three contexts:

1. Your local machine — Interactive auth, browser login, OS keychain storage.
2. CI pipelines — Set `HAMSTER_ACCOUNT_ID` and authenticate with an access token environment variable to skip every prompt.
3. Cloud sandboxes — Hamster's [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents) run the [CLI](https://tryhamster.com/docs/hamster-studio/cli) inside their sandbox environment to pull live [Brief](https://tryhamster.com/docs/hamster-studio/briefs) state before each [Delivery](https://tryhamster.com/docs/concepts/delivery) run.

Auth credentials live in your OS keychain by default (macOS Keychain, Windows Credential Manager, or the Linux Secret Service). On WSL or headless setups without a keychain, the [CLI](https://tryhamster.com/docs/hamster-studio/cli) falls back to an encrypted file using a passphrase you set in `HAMSTER_AUTH_PASSPHRASE`.

## Tips

* Pass a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) slug, UUID, or even a full `tryhamster.com/...` URL straight into `hamster sync` — the [CLI](https://tryhamster.com/docs/hamster-studio/cli) parses all three and only syncs that brief.
* Add `.hamster/` and `.claude/skills/hamster-project-context/` to your `.gitignore`. They are generated and account-specific.
* Run `hamster sync --watch` in a side terminal during a session — your AI agent always sees the latest [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and [Task](https://tryhamster.com/docs/hamster-studio/tasks) state without you needing to remember to re-sync.
* Use `hamster team switch` when you move between client workspaces. The [CLI](https://tryhamster.com/docs/hamster-studio/cli) cleans the previous team's directory before re-syncing the new one.
* The [CLI](https://tryhamster.com/docs/hamster-studio/cli) checks GitHub Releases for updates on a TTL — when a new version is available, you will see an inline notice on the next command.

## Related

* [MCP Server](https://tryhamster.com/docs/hamster-studio/mcp)
* [Creating Briefs](https://tryhamster.com/docs/hamster-studio/briefs/creating-briefs)
* [Generating Plans](https://tryhamster.com/docs/hamster-studio/plans/generating-plans)
* [Cloud Agents](https://tryhamster.com/docs/hamster-studio/cloud-agents)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Cli","item":"https://tryhamster.com/docs/hamster-studio/cli"}]}
```
