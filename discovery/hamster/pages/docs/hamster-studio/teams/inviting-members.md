---
description: Invite colleagues to your Team workspace with email invitations they can accept in one click.
title: Inviting Members | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Inviting Members

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
   * [Creating a Team](https://tryhamster.com/docs/hamster-studio/teams/creating-teams "Creating a Team")  
   * [Inviting Members](https://tryhamster.com/docs/hamster-studio/teams/inviting-members "Inviting Members")  
   * [Roles & Permissions](https://tryhamster.com/docs/hamster-studio/teams/roles-permissions "Roles & Permissions")  
   * [Team Profile](https://tryhamster.com/docs/hamster-studio/teams/team-profile "Team Profile")

* Collaboration

* Account Settings

# Inviting Members

Add colleagues to your team workspace by sending them an email invitation they can accept in one click.

## Overview

Team members join Hamster Studio through email invitations. When you invite someone you select the role they will have when they join. They receive an email with a link that takes them directly into the workspace — or through sign-up first if they do not yet have an account.

![Team members list showing workspace members with their roles and a pending invites section](https://tryhamster.com/_site/images/features/teams/inviting-members/members-list-desktop-light.webp?v=6)![Team members list showing workspace members with their roles and a pending invites section](https://tryhamster.com/_site/images/features/teams/inviting-members/members-list-desktop-dark.webp?v=6) 

Only owners and admins can send invitations (they have the `invites.manage` permission).

## How It Works

1. Go to the Members page — Open your team workspace and select **Members** in the sidebar.
2. Select "Invite Members" — A dialog opens. This button is only visible if you have permission to send invitations.
3. Add email addresses and roles — Enter the email address of the person you want to invite and select their role (Admin, Creator, or Reviewer). You can add up to 25 invitations at once by selecting "Add another". A hint appears when you've reached the maximum.
4. Send the invitations — Select the send button. Each person receives an email with an invitation link.
5. Track pending invites — Invitations that have not yet been accepted appear in the **Pending Invites** section below the members table. You can update the role on a pending invitation or remove it before it is accepted.

## The Invitation Flow for Recipients

When someone receives an invitation:

1. They click the link in the email. The link includes a unique token tied to their email address.
2. If they already have a Hamster Studio account, they are taken to an acceptance page that shows the team name and logo. They select **Join** to become a member.
3. If they do not have an account, they are redirected to the sign-up page. After completing sign-up they are taken back to the invitation acceptance page automatically.
4. Once they accept, they are added to the team with the role that was selected when the invitation was sent, and they land directly in the team workspace.

Invitations are tied to a specific email address. If someone tries to accept an invitation from a different account, it will not work — they need to sign in with the invited address or sign up using it.

## Managing Pending Invitations

Invitations that have not been accepted remain visible in the **Pending Invites** table. From there you can:

* Update the role — Change the role assigned to the invitation before it is accepted. This is useful if someone's responsibilities change between when you sent the invite and when they join.
* Remove an invitation — Delete an invitation to prevent it from being accepted. The link in the invitation email will stop working immediately.
* Renew an invitation — If an invitation has expired you can renew it, which sends a fresh link to the same address.

## Key Capabilities

* **Batch invites**: Send up to 25 invitations in a single action.
* **Role assignment at invite time**: Choose the role someone will have when they join — Admin, Creator, or Reviewer.
* **Pending invite management**: Update or cancel invitations at any time before acceptance.
* **New user onboarding**: Invitees who do not have accounts are guided through sign-up and arrive in the workspace automatically.

## Tips

* If an invitee does not receive the email, ask them to check their spam folder. You can also remove the invitation and send a new one to trigger a fresh email.
* You can only assign roles at or below your own level. An owner can invite as Admin, Creator, or Reviewer; an admin can invite as Admin, Creator, or Reviewer. Creators and reviewers cannot send invitations.
* Accepted invitations are not visible in the pending table — once someone joins they appear in the main **Members** list.

## Related

* [Roles and Permissions](https://tryhamster.com/docs/hamster-studio/teams/roles-permissions)
* [Creating a Team](https://tryhamster.com/docs/hamster-studio/teams/creating-teams)
* [Team Profile](https://tryhamster.com/docs/hamster-studio/teams/team-profile)
* [Getting Started](https://tryhamster.com/docs/hamster-studio/getting-started)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Teams","item":"https://tryhamster.com/docs/hamster-studio/teams"},{"@type":"ListItem","position":5,"name":"Inviting Members","item":"https://tryhamster.com/docs/hamster-studio/teams/inviting-members"}]}
```
