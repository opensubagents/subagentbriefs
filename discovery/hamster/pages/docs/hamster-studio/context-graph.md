---
description: The shared memory behind every Hamster answer — your briefs, conversations, decisions, documents, and the people on your team, connected.
title: Context Graph | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Context Graph

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

# Context Graph

_The shared memory behind every Hamster answer — your [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), conversations, decisions, documents, and the people on your team, connected so the AI can reason over them as one workspace._

## Overview

Hamster keeps a live picture of your workspace called the **[Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph)**. It is the layer the AI assistant reads from when it answers a question, drafts a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), or generates a plan. Instead of a flat pile of documents, the graph captures _how_ your work is connected: which [Brief](https://tryhamster.com/docs/hamster-studio/briefs) belongs to which [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives), which [Task](https://tryhamster.com/docs/hamster-studio/tasks) lives under which [Brief](https://tryhamster.com/docs/hamster-studio/briefs), which conversation produced which decision, and which document was attached to which thread.

That structure is what lets the AI walk relationships when it answers you. Ask "what [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) are linked to the onboarding [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives)?" and Hamster does not have to keyword-match against document chunks — it can read the relationships directly and ground the answer in the actual shape of your workspace.

This page is the home for how the graph works and how it shows up across Hamster. It will grow as the graph gains more surfaces and capabilities.

## What Hamster Gathers

The graph captures the entities your team works with and the relationships between them:

* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) and [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) — the work itself, plus how [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) roll up into [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) and how [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) roll up into initiatives.
* Conversations and threads — the chats that produced [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), the questions that led to a decision, the threads attached to specific [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) and documents.
* Documents — strategy decks, PRDs, customer research, transcripts, and any file your team uploads or links into a brief.
* People — who owns a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), who participated in a thread, who voted on alignment.
* Activity — alignment votes, status changes, and key actions that move work forward.

When you upload a file, attach a document, or create a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), Hamster does not just store the file. It also indexes the content so passages — not just whole files — can surface when they matter, and it records how that file relates to the rest of your workspace.

## How It Stays Current

The graph is a live system, not a one-time index:

* Realtime updates — When a teammate edits a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), attaches a document, or moves a [Task](https://tryhamster.com/docs/hamster-studio/tasks), the graph updates within seconds. The AI assistant sees the new state on its next reply.
* Backfill on connect — When you connect a tool or upload a batch of context, Hamster works through the content in the background and adds it to the graph as it processes. You can keep using Hamster while it catches up.
* File content extraction — Uploaded PDFs, Word docs, and similar files are parsed for their text content, not just their filenames, so the AI can search inside them as easily as inside a brief.

You do not need to do anything to maintain the graph. There is no manual indexing step, no "rebuild" button, no separate tool to manage. As your workspace evolves, the graph evolves with it.

## How Retrieval Feeds the AI's Answers

When you ask the AI a question — in a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) chat, a thread, or a [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation — Hamster does not just stuff a generic chunk of text into the prompt. Retrieval works in three complementary ways:

1. Direct entity reads. If you mention a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), an [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives), or a document by name or link, the AI reads it directly. No fuzzy matching needed when the answer is in a known place.
2. Relationship-first lookup. When the question spans connected work — "what's the latest on the [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) in this [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives)?" — the AI walks the relationships between entities first. This catches [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) that should be relevant even when they do not share keywords with your question.
3. Semantic search across passages. When the question is open-ended, the AI searches across passages (the chunks of text inside [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), documents, and threads) and returns the most relevant ones along with where they came from. Each match carries enough context for the AI to cite it back to you.

For multi-step questions, Hamster's planner can chain these together — read a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), expand to its linked [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives), search across the documents attached to both — and stay within a sensible budget so answers stay fast.

## Where You Will See It

* Chat — Replies in any conversation can reference past threads, linked [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) and [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), attached documents, and the relationships between them. See [AI Responses](https://tryhamster.com/docs/hamster-studio/chat/responses).
* Documents and context — Uploaded files and linked documents are indexed into the graph. Document **passages** can map to different parts of the graph so the right section, not just the right file, can surface. See [Context Documents](https://tryhamster.com/docs/hamster-studio/briefs/context-documents).
* [Plans](https://tryhamster.com/docs/hamster-studio/plans) — [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation pulls in the related [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives), prior decisions, and documents that should inform the [Plan](https://tryhamster.com/docs/hamster-studio/plans), not just the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) in isolation. See [Generating Plans](https://tryhamster.com/docs/hamster-studio/plans/generating-plans).

## Capabilities

* Relationship-first retrieval — The assistant prioritizes context that is _linked_ to your current work, not just textually similar.
* Passage-level grounding — When the AI cites a document, it cites the specific passage, not the whole file.
* Team- and time-aware context — Recent activity, ownership, and who is involved can influence which linked context surfaces first.
* Traceability — You can reason from outcomes back through execution, [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), and the conversations and decisions that led there.
* Account-isolated — The graph is scoped to your account. Queries always run within your team's data — no risk of context leaking across workspaces.

## Tips

* The richer the inputs, the better the retrieval. Upload customer research, attach strategy docs, and link [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) into [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives) — every relationship gives the AI another path to find the right context.
* If the AI's answer feels off, check whether the right context is actually linked. Often a missing [Brief](https://tryhamster.com/docs/hamster-studio/briefs)→[Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) link or a forgotten document upload explains why a relevant passage did not surface.
* Hamster keeps file content searchable, so naming a file well matters less than making sure its content is in the file. The AI reads the content, not just the title.
* Newly uploaded documents take a few seconds to a few minutes to index, depending on size. The status indicator on the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) tells you when processing is complete.

## Related

* [Context Documents](https://tryhamster.com/docs/hamster-studio/briefs/context-documents)
* [AI Responses](https://tryhamster.com/docs/hamster-studio/chat/responses)
* [Generating Plans](https://tryhamster.com/docs/hamster-studio/plans/generating-plans)
* [Conversations](https://tryhamster.com/docs/hamster-studio/chat)
* [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Context Graph","item":"https://tryhamster.com/docs/hamster-studio/context-graph"}]}
```
