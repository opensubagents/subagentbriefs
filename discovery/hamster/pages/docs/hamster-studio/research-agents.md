---
description: Use Research Agents to gather information from multiple sources and write findings into your documents.
title: Research Agents | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Research Agents

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

* [Taskmaster](https://tryhamster.com/docs/taskmaster "Taskmaster")
* Workspace

* Teams

* Collaboration

* Account Settings

# Research Agents

Automatically gather information from multiple sources and write the findings into your document.

## Overview

[Research Agents](https://tryhamster.com/docs/hamster-studio/research-agents) handle the work of collecting information from different places and synthesizing it into something useful. Instead of searching your codebase, checking your team's guidelines, reading a linked article, and then writing it all up yourself, you describe what you want researched and the agent does all of that in one go. The [Results](https://tryhamster.com/docs/hamster-studio/results) land directly in your [Brief](https://tryhamster.com/docs/hamster-studio/briefs), [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints), or [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) — organized and ready to work with.

[Research Agents](https://tryhamster.com/docs/hamster-studio/research-agents) are part of the AI assistant and activate automatically when you ask for research. You don't need to choose anything from a menu — the assistant handles the right approach based on what you're asking for.

## How It Works

1. Trigger a research request — In the chat panel, describe what you want the agent to research. For example: "Research how we handle authentication in the codebase and update the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)" or "Find our approach to this feature in the [Methods Library](https://tryhamster.com/docs/hamster-studio/skills-methods/methods-library) and add a summary."
2. The agent runs parallel searches — Depending on what you asked, the agent may search your team's [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) library for organizational context, your [Methods Library](https://tryhamster.com/docs/hamster-studio/skills-methods/methods-library) for process patterns, your connected codebase, any URLs you've mentioned, files you've attached, and linked project management issues. These run in parallel to keep things fast.
3. Findings are synthesized — Once all searches complete, a synthesis step combines the [Results](https://tryhamster.com/docs/hamster-studio/results) and writes them into your document in the appropriate section, or returns a summary in the chat if you asked a question rather than requesting a document update.
4. Steps are visible in the chat — You see each step labelled as it runs: "Searching organizational context," "Researching codebase," "Extracting URL content." When everything completes, the final [Result](https://tryhamster.com/docs/hamster-studio/results) appears and the steps collapse automatically.

## Research Flows

Different research scenarios trigger different flows:

**Full research** activates when you ask for a comprehensive investigation. It searches your [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods), codebase, any provided URL, attached files, and linked project issues — all in parallel — and then synthesizes everything into your document. This is the most thorough option.

**Quick research** answers a focused question without modifying your document. Use it when you want to know where something is implemented or how a specific pattern works, without committing the findings to the brief.

**URL-to-document** extracts content from a specific webpage and adds it to your brief. Paste or mention a URL in your message, ask the agent to add it to your [Brief](https://tryhamster.com/docs/hamster-studio/briefs), and it fetches the page, pulls out the key points, and writes them in.

**Meeting notes** processes a meeting transcript or notes file and extracts decisions, action items, and discussion points, then structures them as a meeting summary section in your brief.

**Linear research** pulls in context from linked project management issues when you reference an issue ID in your message. The findings are incorporated alongside any other research sources.

## Key Capabilities

* **Parallel execution**: Multiple searches run at the same time. A full research request that covers [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods), codebase, and a URL runs them concurrently rather than one after another.
* **Organizational context awareness**: The agent checks your team's [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) library for relevant company guidelines, standards, and principles before writing. If your [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) say how your team approaches a particular type of work, the agent incorporates that framing.
* **Process pattern matching**: The agent searches your [Methods Library](https://tryhamster.com/docs/hamster-studio/skills-methods/methods-library) for relevant workflows and procedures. If your team has documented an SOP or implementation pattern that applies, it gets included.
* **Codebase research**: When your workspace has a codebase connected, the agent can search it for implementation patterns, relevant files, and architecture decisions.
* **Source attribution**: URL content added to a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) includes a reference to the source page.
* **Focused or comprehensive**: Ask for a quick lookup or a deep dive. The agent matches its scope to your request.

## Tips

* The more specific your research request, the more focused the output. "Research how we currently handle rate limiting in the API layer, following our backend guidelines" gives better [Results](https://tryhamster.com/docs/hamster-studio/results) than "research rate limiting."
* Mention a URL in your message if you want the agent to pull from an external source. The agent detects URLs automatically and includes URL extraction in the flow.
* Attach files to your [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s context before asking for research. Meeting transcripts, design specs, and reference documents become source material the agent can incorporate.
* Use quick research when you want to check something without adding it to your document. It's faster and keeps your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) clean.
* If you've already done a research run and want to update the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) with new information, ask the agent to "add to" or "update" a specific section rather than running a full research pass again.

## Related

* [AI Assistant](https://tryhamster.com/docs/hamster-studio/chat/in-documents)
* [Document Analysis](https://tryhamster.com/docs/hamster-studio/briefs/document-analysis)
* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Research Agents","item":"https://tryhamster.com/docs/hamster-studio/research-agents"}]}
```
