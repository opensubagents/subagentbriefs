---
description: An interactive AI flow that gathers information from your codebase or external URLs and adds the findings to your brief before you generate a plan.
title: Guided Research | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Guided Research

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
   * [Generating Plans](https://tryhamster.com/docs/hamster-studio/plans/generating-plans "Generating Plans")  
   * [Guided Research](https://tryhamster.com/docs/hamster-studio/plans/guided-research "Guided Research")  
   * [Understanding Plans](https://tryhamster.com/docs/hamster-studio/plans/understanding-plans "Understanding Plans")

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

# Guided Research

An interactive AI flow that gathers information from your codebase or external URLs and adds the findings to your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) before you generate a plan.

## Overview

Guided Research is a conversational flow you run inside a [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s AI conversation. It walks you through choosing what to research, where to look, and whether to add the findings to your brief. Use it when your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) lacks technical context, you want to ground the [Plan](https://tryhamster.com/docs/hamster-studio/plans) in how your codebase already works, or you need to pull in information from external documentation before [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation begins.

![Guided research flow in a brief conversation showing topic selection and source options](https://tryhamster.com/_site/images/features/plans/guided-research/plan-research-desktop-light.webp?v=6)![Guided research flow in a brief conversation showing topic selection and source options](https://tryhamster.com/_site/images/features/plans/guided-research/plan-research-desktop-dark.webp?v=6) 

## How It Works

1. Start the flow — In the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s conversation, tell the AI you want to research a topic. Phrases like "help me research something" or "guide me through research" trigger the guided research flow.
2. Name your topic — The AI asks what topic you would like to research. This becomes the focus for all subsequent searches.
3. Choose your sources — The AI asks where to look:  
   * **Codebase** — searches your connected codebase for relevant code, patterns, and implementations  
   * **URLs** — fetches and analyzes one or more web pages you provide  
   * **Both** — searches the codebase and analyzes URLs simultaneously
4. Provide URLs if needed — If you chose URLs or both, the AI asks for the links to analyze. You can provide multiple URLs.
5. Review the findings — The AI presents the research [Results](https://tryhamster.com/docs/hamster-studio/results) organized by source: codebase findings, URL findings, or both. You review everything before anything is written to your brief.
6. Decide what to add — The AI asks whether you want the findings added to your brief. Choose Yes to have the findings synthesized and written into the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) in a structured format. Choose No to discard the findings without making any changes.

## Key Capabilities

* **Codebase-aware research**: When you search the codebase, the AI looks for existing implementations, patterns, and relevant code that should inform the plan. The findings help the [Plan](https://tryhamster.com/docs/hamster-studio/plans) agent understand what already exists versus what needs to be built.
* **URL extraction**: The AI fetches and analyzes the content of any web pages you provide — documentation, design specs, API references, competitor analysis — and summarizes the relevant parts in the context of your topic.
* **Parallel research**: When you choose to research both the codebase and URLs, both searches run at the same time, so you get [Results](https://tryhamster.com/docs/hamster-studio/results) faster.
* **Human-in-the-loop confirmation**: Findings are presented for review before anything is written to your brief. You retain control over what context goes into the document.
* **Structured [Brief](https://tryhamster.com/docs/hamster-studio/briefs) update**: When you confirm the findings should be added, the AI synthesizes them into a well-organized section covering key points, source [Connections](https://tryhamster.com/docs/hamster-studio/connections), and recommendations. It does not dump raw [Results](https://tryhamster.com/docs/hamster-studio/results) into the brief.

## Other Research Options

Beyond the guided research flow, the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) AI conversation supports two additional research modes:

**Standard research** — Tell the AI to "research the codebase and update the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)" or similar phrases. This runs a broader search across your codebase, organizational documents, and any URL or file you mention in the same message, then writes the findings directly to the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) without a confirmation step.

**Deep research** — For topics requiring multi-angle investigation, the AI can spawn parallel research threads across the web and your internal [Knowledge](https://tryhamster.com/docs/concepts/knowledge) base, then synthesize the findings into a new [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or update the existing one.

## Tips

* Run guided research before generating a [Plan](https://tryhamster.com/docs/hamster-studio/plans) when your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) describes a feature that touches existing code. The [Plan](https://tryhamster.com/docs/hamster-studio/plans) agent will use the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s content during generation, so codebase findings already in the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) [Result](https://tryhamster.com/docs/hamster-studio/results) in more accurate, implementation-aware tasks.
* You can run guided research multiple times on the same [Brief](https://tryhamster.com/docs/hamster-studio/briefs), adding findings from different topics or sources in separate passes.
* If you want the AI to focus on a specific aspect of the topic, mention it when naming your research topic — for example, "authentication flows in the current codebase" rather than just "authentication."
* For documentation-heavy features, providing URLs to the relevant docs (third-party libraries, API references, design systems) gives the [Plan](https://tryhamster.com/docs/hamster-studio/plans) agent concrete implementation details to work from.

## Related

* [Generating Plans](https://tryhamster.com/docs/hamster-studio/plans/generating-plans)
* [Understanding Plans](https://tryhamster.com/docs/hamster-studio/plans/understanding-plans)
* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Plans","item":"https://tryhamster.com/docs/hamster-studio/plans"},{"@type":"ListItem","position":5,"name":"Guided Research","item":"https://tryhamster.com/docs/hamster-studio/plans/guided-research"}]}
```
