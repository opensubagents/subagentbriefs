---
description: How Hamster Studio&#x27;s AI agent reads your messages, runs tools, and replies — long answers move into their own thread so the main chat stays clean.
title: How the AI responds | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

How the AI responds

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
   * [Overview](https://tryhamster.com/docs/hamster-studio/chat "Overview")  
   * [Opening a chat](https://tryhamster.com/docs/hamster-studio/chat/opening "Opening a chat")  
   * [Sending messages](https://tryhamster.com/docs/hamster-studio/chat/messages "Sending messages")  
   * [Branching threads](https://tryhamster.com/docs/hamster-studio/chat/branches "Branching threads")  
   * [How the AI responds](https://tryhamster.com/docs/hamster-studio/chat/responses "How the AI responds")  
   * [Chat in documents](https://tryhamster.com/docs/hamster-studio/chat/in-documents "Chat in documents")  
   * [Voice mode](https://tryhamster.com/docs/hamster-studio/chat/voice "Voice mode")

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

# How the AI responds

How Hamster Studio's AI agent reads your messages, runs tools, and replies — with long answers automatically moving into their own thread so the main chat stays clean.

## Overview

Every message you send in a conversation is handled by an AI agent that understands your workspace — [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), documents, skills, [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods), and connected tools. The agent reads your message, decides what to do, and either writes a response, takes an action (creating a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), generating a [Plan](https://tryhamster.com/docs/hamster-studio/plans), searching context), or asks follow-up questions. Responses stream word-by-word so you see the answer forming, not just a [Result](https://tryhamster.com/docs/hamster-studio/results) that appears all at once.

When the agent's reply gets long, or when it's drafting something substantial like a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or a [Plan](https://tryhamster.com/docs/hamster-studio/plans), the conversation moves into a child thread automatically. The parent chat stays focused; the detail lives in its own space with a clickable card pointing to it.

Hamster's chat is the entry point to the product. Most of the Refine work — turning a customer signal into a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) — happens here.

![AI conversation view showing a streamed response with reasoning trace](https://tryhamster.com/_site/images/features/conversations/ai-responses/ai-conversation-desktop-light.webp?v=6)![AI conversation view showing a streamed response with reasoning trace](https://tryhamster.com/_site/images/features/conversations/ai-responses/ai-conversation-desktop-dark.webp?v=6) 

## How It Works

1. You send a message — Your message appears in the thread immediately. The agent receives it along with recent conversation history and any relevant workspace context.
2. The agent reasons — Before responding, the agent may work through the problem internally. When extended reasoning is active, a collapsible "Thinking" section appears in the thread so you can see the steps it followed. This section closes automatically once the final response begins.
3. Tools run if needed — Depending on what you asked, the agent may run tool calls — searching context, creating a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), filtering [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) by tag, casting alignment, fetching from a connected app. Each runs as a compact status indicator showing whether it's in progress, complete, or waiting for review.
4. The response streams in — The reply appears token-by-token with a blinking cursor at the end of the current word. Markdown — headings, bullets, bold, code — is applied as the text arrives.
5. Long answers move to a child thread — If the response is detailed, the agent relocates it into a child thread automatically and posts a card in the parent so you can jump in. [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation and [Brief](https://tryhamster.com/docs/hamster-studio/briefs) drafting always run in their own child threads.
6. You review and continue — When streaming ends, the cursor disappears. If the agent edited a document, accept/reject buttons appear so you can review the diff before applying. Otherwise, you can reply directly.

## Auto-Threading

Detailed answers, [Brief](https://tryhamster.com/docs/hamster-studio/briefs) drafts, and [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation move out of the main chat into child threads automatically. The parent thread keeps a card linking to the child so the conversation stays followable.

The rules:

* Long answers (multi-paragraph explanations, design or implementation [Plans](https://tryhamster.com/docs/hamster-studio/plans), migrations) move on their own.
* [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints) creation always run in a dedicated child thread, with the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) card landing back in the parent on the agent's first reply.
* [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation gets its own child thread when triggered from chat. The plan-generation card streams progress live and stays in sync if you navigate away and come back.
* Pending tool calls in a child thread show an amber dot on the card in the parent so you can spot work that needs attention.
* Solo threads (no other participants) don't get the share-summary banner — it only appears when other people are involved.

## Reasoning Through Your Workspace

The agent doesn't rely on isolated keyword matches. It traverses the relationships between [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), documents, and conversations to assemble higher-signal answers. It's also team-aware and time-aware — it can prioritise context based on who's involved and what changed recently, so responses stay grounded in your team's current reality.

## Working with Files and URLs

* Drop a `.fig` file — Figma files are accepted as a chat upload. The agent extracts the design context (pages, frames, text, components) and uses it as grounding for whatever you ask next.
* Paste a Figma URL — public Figma files work without auth; private ones use the Figma OAuth connection. Either way, the agent renders the file as a thumbnail with structured content the agent can reference.
* Drop a PDF or markdown file — both are extracted and indexed for the agent.
* Paste any URL — most pages are scraped and summarised so the agent can use them as context.

## Key Capabilities

* **Streaming responses**: Replies appear progressively. You can start reading before the agent has finished writing. Incomplete markdown renders gracefully while streaming.
* **Auto-threading**: Long answers, [Brief](https://tryhamster.com/docs/hamster-studio/briefs) drafts, and [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation move to child threads automatically with a clickable card in the parent.
* **Reasoning traces**: For complex questions, expand the "Thinking" section to see the steps the agent followed.
* **Tool call indicators**: Tool calls render in-thread as compact cards with status. Pending tool calls in a child thread surface as amber dots on the parent's branch entry.
* **Document change review**: When the agent edits a document, accept/reject buttons appear with a diff preview. Changes made while you were away show a "View pending changes" prompt before the buttons.
* **Follow-up questions**: When the agent needs more information, it can respond with a structured set of questions in the input area, stepping you through each one. **These persist across page refreshes** — your in-progress answers don't disappear if you reload.
* **Mention `@hamster` directly**: Address the AI in any thread by mentioning `@hamster`. Mixed mentions like `@hamster do this, @bob what do you think?` always trigger Hamster — Hamster never gets filtered out by other mentions in the same message.
* **Sticky context**: After you mention `@hamster`, follow-ups stay routed to Hamster without re-mentioning. After `@bob`, follow-ups stay with Bob until Hamster is explicitly re-mentioned.
* **Hamster has its own avatar**: The AI shows up as a distinct participant in thread views, with its own avatar in headers, reply indicators, tool calls, and annotation messages — so it's always clear who said what.
* **[Plan](https://tryhamster.com/docs/hamster-studio/plans) generation from any chat**: Trigger [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation from the main chat or a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) chat. The plan-gen card lives in whichever thread you started it from, and reaches a terminal state even if you navigate away mid-flight.
* **Stuck-chat recovery**: If a service hiccup leaves a chat appearing to hang, the next message recovers the lock and the stale items are filtered out automatically. You don't get stuck on "Message is already being processed" anymore.
* **Reviewer-safe**: Teammates with the Reviewer role can ask questions and read replies, but write actions (creating [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), editing documents) are blocked at the agent level — not just hidden in the UI.
* **Live voice** (_This feature may need to be enabled for your workspace._): Hold the microphone button in the chat input (or use the keyboard shortcut Cmd+Shift+S on Mac, Ctrl+Shift+S on Windows) to push-to-talk. The agent responds with text in the thread and synthesised audio.

## Tips

* If you want to understand why the agent made a specific decision, expand the "Thinking" section that appears before its response.
* When the agent produces a document change, click "View Pending Changes" before accepting or rejecting to see a side-by-side diff.
* Drop the customer-call recording, the design file, and the linked context **before** asking for a brief. The agent uses everything attached to ground its work, so the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) comes back in the right shape on the first try.
* If the agent keeps drifting on the last 30% of an answer, it's usually a context problem — paste in the strategy doc, the customer transcript, or whatever else is missing, and the next loop will converge.

## Related

* [Thread Messaging](https://tryhamster.com/docs/hamster-studio/chat/messages) — The full message experience, including file attachments and URL previews
* [Thread Branches](https://tryhamster.com/docs/hamster-studio/chat/branches) — Working in focused sub-conversations
* [Mentions and Notifications](https://tryhamster.com/docs/hamster-studio/collaboration/mentions-notifications)
* [AI Features](https://tryhamster.com/docs/hamster-studio/chat/in-documents)
* [Skills and Methods](https://tryhamster.com/docs/hamster-studio/skills-methods)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Chat","item":"https://tryhamster.com/docs/hamster-studio/chat"},{"@type":"ListItem","position":5,"name":"Responses","item":"https://tryhamster.com/docs/hamster-studio/chat/responses"}]}
```
