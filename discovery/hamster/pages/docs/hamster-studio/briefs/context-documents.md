---
description: Attach files and URLs to a Brief so Hamster can use them in Chat, Plan generation, and Delivery.
title: Context Documents | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Context Documents

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

# Context Documents

Give the AI everything it needs to understand your project by attaching supporting files and URLs to your brief.

## Overview

Context documents are files and web pages you attach to a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) to give the AI assistant richer background information. When you upload a specification, a research report, a design document, or any other supporting material, Hamster processes the content and connects it into your workspace Context Graph.

That means Hamster can use this context across chat, document generation, and [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation while traversing related [Briefs](https://tryhamster.com/docs/hamster-studio/briefs), [Initiatives](https://tryhamster.com/docs/hamster-studio/initiatives), [Tasks](https://tryhamster.com/docs/hamster-studio/tasks), and connected tools to pull in relevant supporting information.

Context documents are managed from the Context tab inside any open brief.

![Context tab showing uploaded documents and saved URLs](https://tryhamster.com/_site/images/features/briefs/context-documents/context-view-desktop-light.webp?v=6)![Context tab showing uploaded documents and saved URLs](https://tryhamster.com/_site/images/features/briefs/context-documents/context-view-desktop-dark.webp?v=6) 

## How It Works

### Uploading Files

1. Open the Context tab — Inside any [Brief](https://tryhamster.com/docs/hamster-studio/briefs), click the Context tab in the document panel.
2. Upload your files — Drag and drop files directly onto the upload area, or click "Browse Files" to pick them from your file system. You can upload multiple files at once.
3. Wait for processing — Each uploaded file is processed automatically: uploading, reading the content, analyzing it, and making it available to Hamster. A status indicator on each document card shows where it is in this process.
4. Files are ready — Once processing reaches the "ready" state, the document is fully indexed and available to the AI when you chat or generate a plan.
5. Remove a file — Click the three-dot menu on a document card and select "Remove" to delete it from the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s context.

### Adding URLs

You can also add web pages as context. Paste a URL into the [Brief](https://tryhamster.com/docs/hamster-studio/briefs)'s chat (the AI will handle extraction) and the page content is saved as a URL document, visible in the "Saved URLs" section of the Context tab.

Saved URLs show the page title, domain, a short description, the date added, and word count. You can open the original page in a new tab or delete the URL document from the three-dot menu.

If a URL goes stale or the source page has changed, use **Re-sync** from the URL document menu to refresh the indexed content.

### Team Connections

The Context tab also shows your team's active [Connections](https://tryhamster.com/docs/hamster-studio/connections) to external services (such as GitHub, Linear, Notion, Google Drive, and others). These [Connections](https://tryhamster.com/docs/hamster-studio/connections) make data from those tools available to the AI across all briefs. You can manage [Connections](https://tryhamster.com/docs/hamster-studio/connections) from the Context Settings page, linked directly from the Context tab.

## Supported File Types

Hamster accepts a wide range of file formats:

| Category      | Formats                                                                                                     |
| ------------- | ----------------------------------------------------------------------------------------------------------- |
| Documents     | PDF (up to 50MB), Word (.doc, .docx, up to 25MB), plain text (.txt, up to 10MB), Markdown (.md, up to 10MB) |
| Spreadsheets  | Excel (.xlsx, up to 25MB), CSV (up to 25MB)                                                                 |
| Presentations | PowerPoint (.pptx, up to 50MB)                                                                              |
| Design files  | Figma (.fig) — thumbnail, structure, and design details extracted                                           |
| Images        | JPEG, PNG, GIF, WebP, SVG (up to 20MB) — OCR enabled                                                        |
| Code          | JavaScript, TypeScript, Python, Java, C++ (up to 5MB)                                                       |
| Data formats  | JSON (up to 5MB), XML, YAML                                                                                 |
| Audio         | MP3, WAV, MP4 audio (up to 100MB) — transcription enabled                                                   |
| Video         | MP4, AVI, MOV (up to 500MB) — transcription enabled                                                         |

## Key Capabilities

* **Multi-file upload**: Select or drag multiple files at once. Each processes independently.
* **Processing status**: Each document shows a live status indicator so you know when it's ready for Hamster to use.
* **Content preview**: Document cards show a truncated preview of the extracted text content so you can confirm the right information was captured.
* **OCR for images**: Images are processed with optical character recognition, extracting any text they contain.
* **AI image descriptions**: When you upload an image, Hamster generates a plain-language description of what the image shows. This description is used everywhere — the chat assistant, [Plan](https://tryhamster.com/docs/hamster-studio/plans) generation, and search — so the content of the image contributes to context. Hover over an uploaded image in the Context tab to see its generated description.
* **Figma file support**: Upload `.fig` files directly. Hamster extracts a visual thumbnail, structure (page names, component hierarchy), and design details from the file. The thumbnail appears on the document card; the extracted content feeds into Hamster's context for [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) and plans.
* **Audio and video transcription**: Audio and video files are transcribed automatically, making spoken content searchable and available to Hamster.
* **URL documents with re-sync**: Web pages saved through the chat appear as cards in the Saved URLs section with title, domain, description, and word count. Re-sync any URL from its menu to refresh stale content.
* **Team [Connections](https://tryhamster.com/docs/hamster-studio/connections)**: Shared integrations with external tools appear in the Context tab and contribute to the AI's [Knowledge](https://tryhamster.com/docs/concepts/knowledge) for all [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) in your workspace.
* **Graph-connected retrieval**: Uploaded context is not treated as isolated files. Hamster can traverse related entities in your workspace graph to pull the most relevant context for your current question or request.

## Tips

* Attach context documents before generating a plan. The [Plan](https://tryhamster.com/docs/hamster-studio/plans) generator draws on all indexed context for the [Brief](https://tryhamster.com/docs/hamster-studio/briefs), producing more detailed and accurate [Tasks](https://tryhamster.com/docs/hamster-studio/tasks) when it has supporting material.
* Use the Context tab to attach the source-of-truth documents for a project: the existing product spec, the relevant research, or the design brief. This way the AI can reference them directly without you having to paste excerpts into the chat.
* For large PDFs, processing may take a minute. You will see the status update in real time on the document card.
* If a document fails processing, the card shows a red error indicator. Try re-uploading the file or check that it is not password-protected.
* Your team's [Connections](https://tryhamster.com/docs/hamster-studio/connections) to external tools (set up in [Connection](https://tryhamster.com/docs/hamster-studio/connections) Settings) are visible at the top of the Context tab. These are shared across all [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) — you do not need to re-attach the same [Connection](https://tryhamster.com/docs/hamster-studio/connections) for each project.

## Related

* [Context Graph](https://tryhamster.com/docs/hamster-studio/context-graph)
* [Connections Overview](https://tryhamster.com/docs/hamster-studio/connections/overview)
* [Generating Plans](https://tryhamster.com/docs/hamster-studio/plans/generating-plans)
* [AI Assistant](https://tryhamster.com/docs/hamster-studio/chat/in-documents)
* [Editing Briefs](https://tryhamster.com/docs/hamster-studio/briefs/editing-briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Briefs","item":"https://tryhamster.com/docs/hamster-studio/briefs"},{"@type":"ListItem","position":5,"name":"Context Documents","item":"https://tryhamster.com/docs/hamster-studio/briefs/context-documents"}]}
```
