---
description: Install the Hamster CLI and authenticate with a single command.
title: Getting Started | Hamster
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

# Getting Started

Install the Hamster [CLI](https://tryhamster.com/docs/hamster-studio/cli) and authenticate with a single command.

## Install

Run this in your terminal:

```bash
curl -s https://tryhamster.com/cli/install | bash

```

The script installs the [CLI](https://tryhamster.com/docs/hamster-studio/cli) and opens your browser to sign in. After you approve, the session is transferred back to your terminal and you're ready to go. Credentials are stored securely on your machine — you only need to sign in once.

## Initialize a Project

Inside your repository, run:

```bash
hamster init

```

This creates the `.hamster/` directory, runs your first sync, and generates the agent skill file. From here, run `hamster sync --watch` to keep everything up to date as your team works.

## Switch Teams

If you belong to multiple Hamster teams, switch between them without re-authenticating:

```bash
hamster team

```

The [CLI](https://tryhamster.com/docs/hamster-studio/cli) lists your available teams and lets you select which one to work in.

## Automated Environments

For CI/CD pipelines, containers, or sandboxed environments where a browser isn't available, you can authenticate with environment variables instead:

* `HAMSTER_ACCESS_TOKEN` — Provide a valid access token directly
* `HAMSTER_REFRESH_TOKEN` — Provide a refresh token; the [CLI](https://tryhamster.com/docs/hamster-studio/cli) exchanges it for an access token automatically

When environment variables are set, the [CLI](https://tryhamster.com/docs/hamster-studio/cli) skips the browser flow entirely.

## Remote Environments

For SSH sessions or environments without a browser, `hamster auth login` supports a one-time code flow. The [CLI](https://tryhamster.com/docs/hamster-studio/cli) prints a URL and a code — open the URL on any device, enter the code, and the session is issued to your terminal.

## Auto-Update

The [CLI](https://tryhamster.com/docs/hamster-studio/cli) checks for updates automatically and shows a progress indicator when downloading a new version. Updates are verified before installing.

## Tips

* Run `hamster auth login` to re-authenticate or switch accounts at any time.
* The [CLI](https://tryhamster.com/docs/hamster-studio/cli) session is independent from your browser session. Signing out of the web app does not affect it.
* If your account has multi-factor authentication enabled, the sign-in flow handles it automatically.
* Authentication tokens refresh transparently. `hamster sync --watch` runs indefinitely without auth interruptions.
* Set `HAMSTER_ACCESS_TOKEN` in your CI/CD environment to use the [CLI](https://tryhamster.com/docs/hamster-studio/cli) in automated pipelines without interactive sign-in.

## Related

* [CLI Sync](https://tryhamster.com/docs/hamster-studio/cli/cli-sync)
* [Using the CLI](https://tryhamster.com/docs/hamster-studio/cli/cli-brief-creation)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Cli","item":"https://tryhamster.com/docs/hamster-studio/cli"},{"@type":"ListItem","position":5,"name":"Cli Authentication","item":"https://tryhamster.com/docs/hamster-studio/cli/cli-authentication"}]}
```
