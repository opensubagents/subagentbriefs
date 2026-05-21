---
description: Send and receive messages in a persistent, real-time chat thread — drop in .fig files, paste URLs, mention teammates, and watch responses stream live.
title: Sending messages | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Sending messages

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

# Sending messages

Send and receive messages in a persistent, real-time chat thread — drop in `.fig` files, paste URLs, mention teammates, and watch responses stream in live.

## Overview

Conversations in Hamster Studio happen inside threads — persistent message streams that save automatically and update in real time. You type in the input at the bottom of the screen, send your message, and the thread shows both your message and the AI's reply. Multiple teammates can participate in the same thread, and the AI agent shows up as its own participant alongside humans.

The composer is built for the way you actually share context: paste a Figma URL, drop in a customer-call PDF, attach an image, or `@mention` a teammate — all from the same input.

![Thread messaging view showing team conversation](https://tryhamster.com/_site/images/features/conversations/thread-messaging/thread-messages-desktop-light.webp?v=6)![Thread messaging view showing team conversation](https://tryhamster.com/_site/images/features/conversations/thread-messaging/thread-messages-desktop-dark.webp?v=6) 

## How It Works

1. Type your message — Click the input at the bottom of the conversation. Plain text and rich text formatting are both supported, and the input expands as you type.
2. Attach files or paste URLs — Use the attachment button (the plus icon) to attach files. Paste a URL directly into the input and the thread renders a preview card automatically. Pasted text content over the threshold is converted to an attachment so the message body stays readable.
3. Mention people or `@hamster` — Type `@` followed by the name or part of an email. The picker stays accurate as you narrow it — `@h` → `@ha` → `@ham` always keeps Hamster visible. Mentioned teammates are added to the thread automatically before they're notified, so the deep link in their notification lands on the right item.
4. Send — Press Enter to send, or Shift+Enter to add a new line. Your message appears on the right of the thread instantly while it's being saved.
5. Receive a reply — The AI's response streams in below your message, labelled with the AI's name and avatar. A blinking cursor shows the reply is still being written. Once streaming ends, the cursor disappears.
6. Reply to a specific message — Hover any message and click the reply icon to mark your next message as a reply, with a context indicator shown above the input.

## File and URL Support

| Type                         | What you get                                                                                                                                                               |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Images** (paste or upload) | Square thumbnail in a grid above the message; tap to open a full-size lightbox. Pasted images survive submit and stay attached when the message lands.                     |
| .fig files                   | Uploaded as a chat attachment with a Figma icon and structured description. The AI reads the design context inside the file.                                               |
| PDF                          | Uploaded, extracted, and indexed for the AI to reference.                                                                                                                  |
| Markdown (.md)               | Accepted as a chat upload. Useful for pasting in long specs, transcripts, or research.                                                                                     |
| Pasted Figma URL             | Rendered as a preview card with thumbnail and structured content from the Figma REST API. Public files work unauthenticated; private ones use your Figma OAuth connection. |
| Pasted URL (other)           | Standard URL preview card with title, description, and image, fetched in the background.                                                                                   |
| Pasted long text             | Above the threshold (about 2000 characters), pasted text is converted to an attachment so the message stays readable.                                                      |

You can also send an attachment with no text — useful when you want the AI to look at a file or link without prefacing it.

## Mentions

The mention picker is consistent everywhere: the chat textarea, the rich text composer, and the mention popover all share one resolver, so what you click is always what gets submitted.

* **`@hamster`** addresses the AI directly. The agent always responds when mentioned, even when you also mention a person in the same message.
* **`@teammate`** adds the person to the thread as a participant and sends them a deep-link notification.
* Sticky context — once you mention someone (or Hamster), follow-ups in the same thread stay addressed to them without re-mentioning. Switching threads resets the context.
* The picker filters by name or email and supports keyboard navigation: arrow keys, Enter to confirm, Escape to cancel.

For more on what happens after you mention someone — notifications, deep links, dedupe — see [Mentions and Notifications](https://tryhamster.com/docs/hamster-studio/collaboration/mentions-notifications).

## Key Capabilities

* **Rich text display**: AI responses render as formatted markdown — headings, bullets, code blocks, bold, inline code. Your messages display as plain text with whitespace preserved.
* **File attachments**: Images render as a square-thumbnail grid; documents render as compact preview cards. Click an image to open a lightbox.
* **URL previews**: Pasted URLs render preview cards below the message. Figma URLs get a thumbnail and structured rendering. Previews load lazily as messages scroll into view.
* **Reference link cards**: When the AI references a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), document, or [Task](https://tryhamster.com/docs/hamster-studio/tasks) inline, it renders as a tappable card that navigates straight to the referenced item. Self-references — cards pointing at the page you're already on — are hidden to keep the thread clean.
* **AI participant avatar**: The Hamster AI shows up with its own avatar throughout the thread — in participant headers, reply indicators, tool-call cards, and annotation messages.
* **Typing indicators**: When a teammate or the AI is composing, a typing indicator appears so you know a reply is on the way.
* **Queued messages**: If you send messages faster than the AI processes them, the extras dock above the input as a queue. Cancel any queued message before it's processed.
* **Participant avatars**: Each message from a teammate shows their avatar in the bottom-left of the message group. Consecutive messages from the same person are grouped under a single avatar.
* **Stuck-chat recovery**: If a chat appears to hang because of a service hiccup, the next message recovers the lock automatically and stale items are filtered out so the transcript stays clean.
* **Pinned input on getting started**: On the first-run getting-started chat, the input stays pinned to the bottom so suggested prompts above it don't reflow when you start typing.

## Tips

* Mention someone with `@name` to bring them in. They get a notification, and they're added to the thread before the notification is sent so the deep link works.
* Paste a link — Figma, Notion, a competitor URL — to share context. The AI uses the rendered content when answering, so you can ask it to work with the link directly.
* If the AI's response references a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or document, click the reference card beneath the message to jump there directly.
* Drop in a `.fig` file or a Figma URL when you want the agent to ground a [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or [Plan](https://tryhamster.com/docs/hamster-studio/plans) in real design context, not a description of design.

## Related

* [AI Responses](https://tryhamster.com/docs/hamster-studio/chat/responses) — How the AI generates and streams replies
* [Thread Branches](https://tryhamster.com/docs/hamster-studio/chat/branches) — Forking a message into a focused sub-thread
* [Mentions and Notifications](https://tryhamster.com/docs/hamster-studio/collaboration/mentions-notifications)
* [Context Documents](https://tryhamster.com/docs/hamster-studio/briefs/context-documents) — Attaching documents to [Briefs](https://tryhamster.com/docs/hamster-studio/briefs) for AI context

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Chat","item":"https://tryhamster.com/docs/hamster-studio/chat"},{"@type":"ListItem","position":5,"name":"Messages","item":"https://tryhamster.com/docs/hamster-studio/chat/messages"}]}
```
