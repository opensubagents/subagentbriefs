---
description: Upload files or attach URLs to a Brief, then ask the AI to read, summarize, and extract information.
title: Document Analysis | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Document Analysis

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
   * [Creating Briefs](https://tryhamster.com/docs/hamster-studio/briefs/creating-briefs "Creating Briefs")  
   * [Editing Briefs](https://tryhamster.com/docs/hamster-studio/briefs/editing-briefs "Editing Briefs")  
   * [Brief Status](https://tryhamster.com/docs/hamster-studio/briefs/brief-status "Brief Status")  
   * [Brief Tags](https://tryhamster.com/docs/hamster-studio/briefs/brief-tags "Brief Tags")  
   * [Context Documents](https://tryhamster.com/docs/hamster-studio/briefs/context-documents "Context Documents")  
   * [Activity Timeline](https://tryhamster.com/docs/hamster-studio/briefs/activity-timeline "Activity Timeline")  
   * [Sharing Briefs](https://tryhamster.com/docs/hamster-studio/briefs/sharing-briefs "Sharing Briefs")  
   * [Delivering Briefs](https://tryhamster.com/docs/hamster-studio/briefs/delivering-briefs "Delivering Briefs")  
   * [Document Analysis](https://tryhamster.com/docs/hamster-studio/briefs/document-analysis "Document Analysis")

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

# Document Analysis

Upload files or attach URLs to a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), then ask the AI to read, summarize, and extract information from them.

## Overview

Document analysis lets you bring external information into a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) and work with it through the AI assistant. You upload files — PDFs, images, text documents, spreadsheets, code files — or paste in URLs, and they become part of the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s context. From there you can ask the assistant to summarize them, answer questions based on what they contain, extract specific information, or incorporate their content directly into the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) document.

This is particularly useful for [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) that depend on reference material: research papers, design specs, meeting transcripts, third-party documentation, or anything your team has collected that should inform the work.

## How It Works

1. Attach documents to the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) context — From the Context tab in the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) sidebar, upload files or add a URL. Files are processed and stored as searchable context for the brief. Multiple files can be attached.
2. Ask the assistant about them — With documents in context, ask the assistant to work with them. You can ask for a summary, search for something specific, extract action items, or ask the assistant to add content from a document into the brief.
3. The assistant searches the context — When you reference your uploaded documents, the assistant performs a semantic search across the attached files to find the most relevant content. It returns answers with references to which document the information came from.
4. Content is written into the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) — If you ask the assistant to incorporate findings into your document, it writes the extracted content into the appropriate section of the brief.

## File Types Supported

The document analysis agent handles a range of file types:

* PDFs — Full text extraction and analysis
* Images — Visual analysis and description of what the image shows. Uploaded images receive an automatically generated plain-language description that is stored as alt text and used by all AI consumers (chat, [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation, RAG). Hover an image in the Context tab to see its description.
* Text files — Plain text, markdown, and similar formats
* Code files — Source code with structure-aware analysis
* Spreadsheets and data files — Tabular data and structured content
* Video files — Analysis of video content
* JSON and XML — Structured data formats

## Interaction Patterns

You can work with attached documents in several ways through the chat panel:

**Summarize**: "Summarize my uploaded documents" or "Give me the key points from the files I attached." The assistant produces a structured summary organized by theme or document.

**Search**: "Find anything about authentication requirements in my documents" or "Look through the uploaded files for API rate limits." The assistant returns matching content with citations.

**Answer questions**: "Based on the spec I uploaded, what are the acceptance criteria?" or "What does the research document say about user preferences?" The assistant answers directly from the document evidence.

**Analyze**: "Compare the two spec documents I attached" or "What patterns appear across my uploaded files?" The assistant identifies themes, [Connections](https://tryhamster.com/docs/hamster-studio/connections), and differences across multiple documents.

**Extract**: "Extract all action items from the meeting notes I uploaded" or "List the requirements from my attached spec as bullet points." The assistant produces structured output from the document content.

**Update the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)**: "Add the key findings from my uploaded research to the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)" or "Incorporate the decisions from the meeting notes." The assistant extracts the relevant content and writes it into the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) document.

## In-Conversation File Uploads

You can also attach files directly in the chat panel without going through the Context tab. Attach a file to a message and ask the assistant about it in the same turn. The assistant reads the file and responds in the conversation.

When the file contains content that's relevant to the [Brief](https://tryhamster.com/docs/hamster-studio/briefs), the assistant can proactively offer to save it to the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s context so it's available for future questions in that brief.

## Key Capabilities

* **Semantic search**: The assistant finds relevant content in your documents based on meaning, not just keyword matching. Asking about "error handling patterns" finds relevant content even if the document uses different phrasing.
* **Multi-document awareness**: When you have multiple files attached, the assistant works across all of them and can identify [Connections](https://tryhamster.com/docs/hamster-studio/connections), contradictions, or gaps between documents.
* **Source citations**: Answers reference the specific document they drew from, so you know where information came from.
* **Direct document editing**: Content from attached files can be written directly into the [Brief](https://tryhamster.com/docs/hamster-studio/briefs), formatted appropriately for a project document.
* **Persistent context**: Documents attached to a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) remain available for the life of the brief. Any conversation in that [Brief](https://tryhamster.com/docs/hamster-studio/briefs) can reference them without re-uploading.

## Tips

* Attach supporting documents before starting a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) writing session. The assistant will draw on them automatically when relevant, even without an explicit instruction.
* For meeting transcripts, use the assistant's "process meeting notes" flow: it extracts decisions, action items, and discussion points and structures them into a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) section automatically.
* If you have a large reference document (such as a lengthy spec or research report), ask the assistant to summarize it first, then ask follow-up questions on the summary rather than treating the full document as the target.
* Use the Context tab to manage which documents are attached to a brief. You can review what's available and remove files that are no longer relevant to keep the context focused.
* When attaching images — screenshots, diagrams, wireframes — you can ask the assistant to describe what it sees, identify UI elements, or compare a design to the requirements in your brief.

## Related

* [AI Assistant](https://tryhamster.com/docs/hamster-studio/chat/in-documents)
* [Research Agents](https://tryhamster.com/docs/hamster-studio/research-agents)
* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)
* [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Briefs","item":"https://tryhamster.com/docs/hamster-studio/briefs"},{"@type":"ListItem","position":5,"name":"Document Analysis","item":"https://tryhamster.com/docs/hamster-studio/briefs/document-analysis"}]}
```
