---
description: Ask questions, create multiple documents, get edit suggestions, and take action on your Briefs from the conversation panel.
title: Chat in documents | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Chat in documents

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

# Chat in documents

_Ask questions, get writing help, create multiple documents, and take action on your [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) — all from the conversation panel alongside your work._

## Overview

The AI assistant is available in every [Brief](https://tryhamster.com/docs/hamster-studio/briefs), [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints), and [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) conversation in Hamster Studio. You interact with it by typing in the chat panel. The assistant understands the document you're currently working on, the [Knowledge](https://tryhamster.com/docs/concepts/knowledge) your workspace has built up, and the context you've explicitly attached. It can answer questions, write and update document sections, create related documents, and trigger actions like generating a [Plan](https://tryhamster.com/docs/hamster-studio/plans) — responding immediately in the same thread where you're working.

The assistant coordinates specialist agents — research, writing, code analysis, document editing — routing your request to the right expert automatically. When a request spans multiple concerns, Hamster fans out to specialists in parallel and synthesizes their work into a single response. You see labelled progress steps as each specialist completes its part.

## How It Works

1. Open the chat panel — On any [Brief](https://tryhamster.com/docs/hamster-studio/briefs), [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints), or [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) page, the AI chat panel is available in the sidebar. Type your message and press Enter or click Send.
2. The assistant reads your context — Before responding, the assistant considers what document you have open, any files or URLs you've attached as context, relevant [Knowledge](https://tryhamster.com/docs/concepts/knowledge) from your workspace ([Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints), [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods), previous conversations), and the conversation history from earlier turns.
3. Requests are routed automatically — Simple questions get answered directly. Requests involving research, file analysis, URL extraction, or multi-step planning are delegated to specialist agents. Hamster decides which specialists to involve and in what order. You see labelled steps in the chat as each specialist completes its work.
4. The response is delivered in-thread — The assistant's answer appears in the conversation. If it updated your document, the changes appear in the editor immediately. You can continue the conversation naturally from there.

## Key Capabilities

* **Document editing**: Ask the assistant to add a section, rewrite a paragraph, or restructure your [Brief](https://tryhamster.com/docs/hamster-studio/briefs). Changes are applied directly to the open document without copy-pasting.
* **Unified document creation**: Ask for a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints), and [Initiative](https://tryhamster.com/docs/hamster-studio/initiatives) in one message. Hamster creates the documents together, links them when it can, and returns the set in one [Hamster Chat](https://tryhamster.com/docs/hamster-studio/chat) thread.
* **Cross-document edit suggestions**: Ask for changes to an existing [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or [Blueprint](https://tryhamster.com/docs/hamster-studio/blueprints), and Hamster opens a suggestion thread on the document instead of silently rewriting it. Review the suggested change in context before applying it.
* **In-context Q&A**: Ask questions about your [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s content, your [Team](https://tryhamster.com/docs/hamster-studio/teams)'s guidelines ([Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints)), or your process library ([Methods](https://tryhamster.com/docs/hamster-studio/skills-methods)). The assistant searches your workspace [Knowledge](https://tryhamster.com/docs/concepts/knowledge) before answering.
* **Multi-step flows**: Structured flows handle more complex requests — researching a topic from multiple sources, extracting content from a URL, processing meeting notes — and run as a visible sequence of labelled steps in the chat.
* **Auto-threading**: When the assistant's response involves a detailed multi-step flow, it can move the conversation to a dedicated thread automatically. This keeps the main conversation focused while giving the detailed work its own space. A link card in the main thread lets you jump to the detail thread at any time.
* **[Brief](https://tryhamster.com/docs/hamster-studio/briefs) management from chat**: You can manage your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) lifecycle directly from the conversation — mark a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) as ready, cast an alignment vote, or notify your [Team](https://tryhamster.com/docs/hamster-studio/teams) — without switching to a different tab or page.
* **Chat suggestions**: When you open a new conversation, quick-start prompts organized into categories (ideas, strategy, features, code) help you start without staring at a blank input.
* **Try again**: If a response misses the mark, ask the assistant to try again from the same message. It re-runs the last flow with any additional guidance you provide.
* **Conversation memory**: The assistant retains context across turns within a thread. It remembers what you discussed earlier and can build on previous responses without you repeating the background.
* **Historical attachments stay in scope**: A screenshot, PDF, or document you uploaded earlier in the conversation is still visible to the assistant several turns later. You can refer back to "the wireframe I sent" or "the spec from yesterday" and the assistant will re-read the file rather than asking you to re-attach it.
* **Writes the language you [Brief](https://tryhamster.com/docs/hamster-studio/briefs) in**: The assistant detects the language of your [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and replies (and generates [Plans](https://tryhamster.com/docs/hamster-studio/plans)) in the same language. A [Brief](https://tryhamster.com/docs/hamster-studio/briefs) written in Spanish gets a Spanish response and a Spanish [Task](https://tryhamster.com/docs/hamster-studio/tasks) list, even when the rest of your workspace is in English.

## How the Assistant Thinks

When your message arrives, Hamster decides how to handle it:

* Direct response — If your message is a question or a conversational exchange, the assistant responds immediately without calling any tools.
* Document action — If you ask the assistant to write, update, or restructure your document, it calls the appropriate editing tools and applies changes in place.
* Specialist delegation — If your request requires research, URL extraction, file analysis, code review, or a combination, Hamster routes to one or more specialist agents. Each specialist runs independently and reports back. Hamster synthesizes their outputs into a single coherent response.
* Clarification — If Hamster needs more information before delegating, it asks you a focused question first rather than guessing.

During a flow, Hamster collects [Results](https://tryhamster.com/docs/hamster-studio/results) from parallel specialists, synthesizes them, and produces the final output — whether that's a written addition to your document or a standalone answer in the thread. Each specialist's contribution appears as a labelled step so you can follow what's happening.

## Permissions

What the assistant can do for you depends on your role on the team:

* **Owners, admins, and creators** can ask the assistant to edit documents, generate [Plans](https://tryhamster.com/docs/hamster-studio/plans), create new [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) from a conversation, and trigger cross-document suggestions.
* **Reviewers** can read, ask questions, and chat with the assistant, but cannot trigger writes. If a reviewer asks the assistant to edit a document or create a new [Brief](https://tryhamster.com/docs/hamster-studio/briefs), the request is declined at the agent layer with an explanation — not just hidden from the UI.

## Tips

* Be specific about what you want the assistant to do to your document. "Add a requirements section covering authentication, data storage, and API rate limits" produces better [Results](https://tryhamster.com/docs/hamster-studio/results) than "update the brief."
* Attach relevant files or URLs to your [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s context before asking the assistant to incorporate them. See [Document Analysis](https://tryhamster.com/docs/hamster-studio/briefs/document-analysis) for how context documents work.
* If the assistant produces a [Result](https://tryhamster.com/docs/hamster-studio/results) that's close but not quite right, continue the conversation rather than starting over. It retains the thread history and can refine its previous response.
* For structured research across your codebase, organizational docs, and external sources, explicitly ask the assistant to "research" the topic. This triggers the full multi-source research flow.
* The assistant works within your workspace's [Knowledge](https://tryhamster.com/docs/concepts/knowledge) — the more complete your [Blueprints](https://tryhamster.com/docs/hamster-studio/blueprints) and [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) are, the more context it has to work with.

## Related

* [Research Agents](https://tryhamster.com/docs/hamster-studio/research-agents)
* [Document Analysis](https://tryhamster.com/docs/hamster-studio/briefs/document-analysis)
* [Voice](https://tryhamster.com/docs/hamster-studio/chat/voice)
* [Routines](https://tryhamster.com/docs/hamster-studio/routines)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)
* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Chat","item":"https://tryhamster.com/docs/hamster-studio/chat"},{"@type":"ListItem","position":5,"name":"In Documents","item":"https://tryhamster.com/docs/hamster-studio/chat/in-documents"}]}
```
