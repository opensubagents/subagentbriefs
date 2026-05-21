---
description: Turn a completed Brief into a structured Plan and Task breakdown with one click.
title: Generating Plans | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Generating Plans

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

# Generating Plans

Turn a completed [Brief](https://tryhamster.com/docs/hamster-studio/briefs) into a structured [Task](https://tryhamster.com/docs/hamster-studio/tasks) breakdown with one click.

## Overview

[Plan](https://tryhamster.com/docs/hamster-studio/plans) generation reads the content of your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and produces a two-level [Task](https://tryhamster.com/docs/hamster-studio/tasks) hierarchy: a set of parent [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) covering the major areas of work, each automatically elaborated into subtasks with detailed descriptions and acceptance criteria. The entire process runs in the background, and [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) appear in the [Plan](https://tryhamster.com/docs/hamster-studio/plans) view as they are created.

Generation uses Hamster's [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph), so [Plans](https://tryhamster.com/docs/hamster-studio/plans) can pull from related [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives), documents, prior work, and team context rather than treating your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) as an isolated input.

![Plan view showing tasks generated from a brief](https://tryhamster.com/_site/images/features/plans/generating-plans/plan-view-desktop-light.webp?v=6)![Plan view showing tasks generated from a brief](https://tryhamster.com/_site/images/features/plans/generating-plans/plan-view-desktop-dark.webp?v=6) 

## How It Works

1. Open your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) — Navigate to any [Brief](https://tryhamster.com/docs/hamster-studio/briefs) in your workspace. The [Plan](https://tryhamster.com/docs/hamster-studio/plans) tab shows an empty state until a [Plan](https://tryhamster.com/docs/hamster-studio/plans) has been generated.
2. Click "Generate [Plan](https://tryhamster.com/docs/hamster-studio/plans)" — Hamster Studio analyzes your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) content and searches for relevant context from your connected [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods), and codebase. A progress indicator shows the current generation phase.
![Plan tab showing flow steps and task cards appearing progressively during AI plan generation](https://tryhamster.com/_site/images/features/plans/generating-plans/plan-generating-desktop-light.webp?v=6)![Plan tab showing flow steps and task cards appearing progressively during AI plan generation](https://tryhamster.com/_site/images/features/plans/generating-plans/plan-generating-desktop-dark.webp?v=6) 
1. Parent [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are created — The AI produces a set of top-level [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) that represent the main areas of work. These appear in the [Plan](https://tryhamster.com/docs/hamster-studio/plans) view as soon as they are ready, before elaboration is complete.
2. Subtasks are elaborated in parallel — Each parent [Task](https://tryhamster.com/docs/hamster-studio/tasks) is expanded into detailed subtasks simultaneously. Each subtask includes a description, scope boundaries, and acceptance criteria. The [Plan](https://tryhamster.com/docs/hamster-studio/plans) fills in progressively as elaboration threads complete.
3. [Plan](https://tryhamster.com/docs/hamster-studio/plans) is finalized — Once all [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) have been elaborated, the progress indicator clears and the full [Plan](https://tryhamster.com/docs/hamster-studio/plans) is available for review and delivery.

## Key Capabilities

* **Watch [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) appear in real time**: [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) stream into the [Plan](https://tryhamster.com/docs/hamster-studio/plans) view as they're generated. You can start reviewing early parent [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) while the rest of the [Plan](https://tryhamster.com/docs/hamster-studio/plans) is still being built.
* **Progress tracking**: A progress card at the top of the [Plan](https://tryhamster.com/docs/hamster-studio/plans) view shows the current generation phase and how far along the process is. You always know what Hamster is doing and how much is left.
* **Context-aware generation**: Before creating [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), Hamster searches your [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods), connected tools (including Figma designs if connected), and your codebase. The [Plan](https://tryhamster.com/docs/hamster-studio/plans) reflects your team's actual patterns and existing work, not a generic breakdown.
* **Graph-aware planning**: Hamster can traverse related entities and context neighborhoods while planning, selecting what is most relevant across [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives), and documents.
* **No overlap between [Tasks](https://tryhamster.com/docs/hamster-studio/tasks)**: Each parent [Task](https://tryhamster.com/docs/hamster-studio/tasks) is elaborated with awareness of its siblings. Hamster avoids creating subtasks that duplicate work covered by other parent tasks.
* **Focus areas**: When triggering generation from the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s chat, you can specify a target number of [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) or particular focus areas to shape the output.
* **Refine with chat**: After a [Plan](https://tryhamster.com/docs/hamster-studio/plans) is generated, the [Plan](https://tryhamster.com/docs/hamster-studio/plans) view has a chat panel scoped to your plan. Ask Hamster to split a parent [Task](https://tryhamster.com/docs/hamster-studio/tasks), add a missing subtask, rewrite acceptance criteria, or change the scope — without regenerating from scratch. Hamster reads the current [Plan](https://tryhamster.com/docs/hamster-studio/plans) and applies changes directly.
* **Drag-and-drop reordering**: Drag [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) to reorder them. The new order is saved and respected during delivery.
* **Regeneration**: If the [Plan](https://tryhamster.com/docs/hamster-studio/plans) doesn't reflect what you need, regenerate it from the [Plan](https://tryhamster.com/docs/hamster-studio/plans) tab. This clears all existing [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) and produces a fresh [Plan](https://tryhamster.com/docs/hamster-studio/plans) from the current [Brief](https://tryhamster.com/docs/hamster-studio/briefs) content. This action cannot be undone.

## Generation Phases

The progress header shows the current phase as [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation runs:

| Phase                                                                | What is happening                                                                                            |
| -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| Analyzing [Brief](https://tryhamster.com/docs/hamster-studio/briefs) | The AI is reading and parsing the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) content         |
| Generating [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) | Parent [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are being created one by one                |
| Processing [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) | The completed parent [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) are collected for elaboration |
| Generating subtasks                                                  | Each parent [Task](https://tryhamster.com/docs/hamster-studio/tasks) is being elaborated in parallel         |

## Tips

* Write a thorough [Brief](https://tryhamster.com/docs/hamster-studio/briefs) before generating a plan. The richer the context in your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) — requirements, constraints, background research — the more accurate and detailed the generated [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) will be. Use the [Guided Research](https://tryhamster.com/docs/hamster-studio/plans/guided-research) flow first if you need to gather information before generating.
* If you are not happy with the initial [Plan](https://tryhamster.com/docs/hamster-studio/plans), use the Regenerate button after editing your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) to add more detail or clarification rather than manually reworking every task.
* Generation can take a few minutes for complex briefs. You do not need to stay on the page — the [Plan](https://tryhamster.com/docs/hamster-studio/plans) is persisted and will be ready when you return.

## Related

* [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph)
* [Guided Research](https://tryhamster.com/docs/hamster-studio/plans/guided-research)
* [Understanding Plans](https://tryhamster.com/docs/hamster-studio/plans/understanding-plans)
* [Creating Briefs](https://tryhamster.com/docs/hamster-studio/briefs/creating-briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Plans","item":"https://tryhamster.com/docs/hamster-studio/plans"},{"@type":"ListItem","position":5,"name":"Generating Plans","item":"https://tryhamster.com/docs/hamster-studio/plans/generating-plans"}]}
```
