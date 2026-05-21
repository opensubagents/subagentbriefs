---
description: Mention teammates or @hamster from inside any thread or document — the right person gets a deep-link notification to the exact message that mentioned them.
title: Mentions and Notifications | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Mentions & Notifications

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
   * [Real-Time Editing](https://tryhamster.com/docs/hamster-studio/collaboration/real-time-editing "Real-Time Editing")  
   * [Mentions & Notifications](https://tryhamster.com/docs/hamster-studio/collaboration/mentions-notifications "Mentions & Notifications")  
   * [Document Versioning](https://tryhamster.com/docs/hamster-studio/collaboration/document-versioning "Document Versioning")

* Account Settings

# Mentions and Notifications

@mention teammates or `@hamster` from inside any thread or document — the right person gets the right notification, with the deep link to exactly the message that mentioned them.

## Overview

Mentions let you address a specific teammate — or the AI agent — directly inside a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), document, or conversation by typing their name with the `@` symbol. The person you mention is added to the thread, gets a deep-link notification, and can pick up the conversation in context. Notifications also surface other account-level updates so the team stays informed without manual check-ins.

The mention pipeline is built to be predictable. Type `@h`, then `@ha`, then `@ham` — Hamster stays at the top of the autocomplete the whole way through. Click a teammate, send the message, and you can trust three things: they're a participant on the thread, they have a notification, and the notification opens to the exact message they were mentioned in.

![Activity feed showing @mention notifications with links to the referenced documents](https://tryhamster.com/_site/images/features/collaboration/mentions-notifications/activity-mentions-desktop-light.webp?v=6)![Activity feed showing @mention notifications with links to the referenced documents](https://tryhamster.com/_site/images/features/collaboration/mentions-notifications/activity-mentions-desktop-dark.webp?v=6) 

## How It Works

1. Trigger the mention picker — In a [Brief](https://tryhamster.com/docs/hamster-studio/briefs), document, or chat, type `@` followed by any part of a teammate's name or email. A picker appears with matching team members and the Hamster AI.
2. Pick the person (or `@hamster`) — Use arrow keys and Enter, or click directly. The mention is inserted as a styled tag in the content.
3. Send the message — The mention is submitted as a structured target alongside the message body, so the system knows exactly who you meant.
4. The mentioned person is added to the thread — Mentioned teammates are added as participants before notifications fire, so they have permission to read and reply when they click through.
5. A deep-link notification is sent — The recipient gets an in-app notification linked to the exact thread item that mentioned them. Real-time [Delivery](https://tryhamster.com/docs/concepts/delivery) (if enabled for your workspace) pushes it instantly; otherwise it appears on their next page load. The notification keeps the surrounding conversation context, so they can read the thread and understand why they were mentioned before clicking through.
6. Sticky context handles follow-ups — Once you've mentioned someone in a thread, follow-up messages stay routed to them without re-mentioning. Switch threads to reset.
7. Read or dismiss — The recipient can mark a notification read (clears the unread badge but keeps it in the list) or dismiss it (removes it). Notifications expire automatically after about a month.

## Mention Targets

| Target                        | Behaviour                                                                                                                                                                        |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| @hamster                      | The AI agent always responds when mentioned, even when you also mention people in the same message. Hamster sticks to the thread until a different mention replaces the context. |
| @teammate                     | Adds them as a participant, sends a deep-link notification, and routes follow-ups to them until a different mention replaces the context.                                        |
| Mixed (@hamster \+ @teammate) | Hamster responds; teammates are added and notified. No more situations where the AI gets silently filtered out by other mentions in the same message.                            |

## Key Capabilities

* **Mention teammates and the AI**: The picker includes every team member and the Hamster AI. You can direct a question or [Task](https://tryhamster.com/docs/hamster-studio/tasks) at the AI the same way you would a person.
* **Predictable autocomplete**: Progressive filtering (`@h` → `@ham` → `@hamster`) is consistent across every composer surface — chat, [Brief](https://tryhamster.com/docs/hamster-studio/briefs) editor, and document editor all use the same logic.
* **Structured submission**: What you click in the composer is what gets submitted. The system uses a structured mention target rather than re-parsing your message text, so mentions can't drift between what you typed and what the system stored.
* **Sticky context**: After you mention someone, follow-up messages stay routed to them without re-mentioning. Per-thread, so switching threads resets the inferred mention.
* **Auto-add before notify**: Mentioned teammates are added to the thread as participants before the notification is sent, so the deep link in the notification always opens to a thread they have access to.
* **Full thread context in notifications**: Mention notifications include the surrounding conversation, not just the single message — so you can understand why you were mentioned before clicking through.
* **Deep links to chat threads**: Direct mentions in chat threads (not just inside [Briefs](https://tryhamster.com/docs/hamster-studio/briefs)) deep-link to the right thread item, not a generic dashboard view.
* **Deduplicated invite suggestions**: When the system suggests a teammate based on a connected app, all eligible billing managers see exactly one notification for it — not one per manager per suggestion.
* **In-app notification center**: Notifications accumulate in a popover accessible from the top navigation, with an unread count badge.
* **Read and dismiss separately**: Reading a notification clears the unread count but keeps it in the list for reference. Dismissing removes it entirely.
* **Account-scoped**: Each notification belongs to a specific workspace account. Switching accounts switches the notification surface.

## Notification Types

| Type    | When it appears                                                                                                                  |
| ------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Info    | Standard updates and mentions                                                                                                    |
| Warning | Situations that may need attention (e.g. [Brief](https://tryhamster.com/docs/hamster-studio/briefs) quota approaching the limit) |
| Error   | Actions that failed or require follow-up                                                                                         |

Notifications are delivered in-app by default. Real-time [Delivery](https://tryhamster.com/docs/concepts/delivery) (instant push to open browser sessions) is a separate workspace configuration.

## Workspace Configuration

Notifications can be turned on or off at the workspace level:

* **Notifications**: Controls whether the notification center appears. On by default.
* **Real-time notifications**: Controls whether notifications push instantly to open sessions. When disabled, notifications appear on the next page load.

Contact your workspace administrator to change these settings.

## Tips

* Mention `@hamster` to assign the AI a question or [Task](https://tryhamster.com/docs/hamster-studio/tasks) inline — useful when you want to flag something for AI follow-up without leaving the document.
* After you mention someone, you can keep replying to them in the thread without re-mentioning — context is sticky per thread.
* Dismissed notifications are gone permanently. To preserve a notification for later reference, mark it as read instead.
* Notifications expire after about 30 days. For long-lived action items, use a [Task](https://tryhamster.com/docs/hamster-studio/tasks) instead of relying on notifications.
* The mention picker only shows people in the current team account. To collaborate with someone outside your account, invite them as a team member first — see [Inviting Members](https://tryhamster.com/docs/hamster-studio/teams/inviting-members).

## Related

* [Real-Time Editing](https://tryhamster.com/docs/hamster-studio/collaboration/real-time-editing)
* [Team Members](https://tryhamster.com/docs/hamster-studio/teams/roles-permissions)
* [Conversations](https://tryhamster.com/docs/hamster-studio/chat)
* [Sharing Briefs](https://tryhamster.com/docs/hamster-studio/briefs/sharing-briefs)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Collaboration","item":"https://tryhamster.com/docs/hamster-studio/collaboration"},{"@type":"ListItem","position":5,"name":"Mentions Notifications","item":"https://tryhamster.com/docs/hamster-studio/collaboration/mentions-notifications"}]}
```
