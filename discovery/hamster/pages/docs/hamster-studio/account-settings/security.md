---
description: Control how you sign in, protect your account with a second factor, and manage connected sign-in methods.
title: Security | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Security

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
   * [Personal Profile](https://tryhamster.com/docs/hamster-studio/account-settings/personal-profile "Personal Profile")  
   * [Security](https://tryhamster.com/docs/hamster-studio/account-settings/security "Security")  
   * [Preferences](https://tryhamster.com/docs/hamster-studio/account-settings/preferences "Preferences")  
   * [Billing](https://tryhamster.com/docs/hamster-studio/account-settings/billing "Billing")  
   * [Plan limits and upgrades](https://tryhamster.com/docs/hamster-studio/account-settings/billing/plan-limits "Plan limits and upgrades")  
   * [Brief Quota Notifications](https://tryhamster.com/docs/hamster-studio/account-settings/billing/quota-notifications "Brief Quota Notifications")

# Security

_Control how you sign in, protect your account with a second factor, and manage connected sign-in methods._

## Overview

The Security section gives you control over your authentication credentials. From here you can sign in with Google, set or change a password, enroll in multi-factor authentication (MFA) using a TOTP authenticator app, and link or unlink social sign-in providers like Google, GitHub, or Microsoft. These settings apply to your personal account and do not affect other team members.

![Security settings page showing password change, multi-factor authentication, and connected sign-in providers](https://tryhamster.com/_site/images/features/account-settings/security/security-settings-desktop-light.webp?v=6)![Security settings page showing password change, multi-factor authentication, and connected sign-in providers](https://tryhamster.com/_site/images/features/account-settings/security/security-settings-desktop-dark.webp?v=6) 

## How It Works

1. Open security settings — Navigate to Personal Profile in your settings menu, then select Security. The URL pattern is `/home/[your-team]/personal-settings/security`.
2. Change your password — If you signed up with email and password, the Update Password section appears. Enter a new password and confirm it. A verification email is sent, and your password updates after you follow the link.
3. Set up multi-factor authentication — In the Multi-Factor Authentication section, click "Set up MFA". Give the factor a name (e.g., "Work phone"), then scan the QR code with your authenticator app (Google Authenticator, Authy, 1Password, or any TOTP-compatible app). Enter the six-digit code from your app to verify and activate the factor.
4. Manage MFA factors — Your enrolled factors appear in a table showing the factor name, type (TOTP), and verification status. To remove a factor, click the remove button on its row and confirm. You must have at least one sign-in [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) remaining after removing a factor.
5. Link or unlink social accounts — If identity linking is enabled on your workspace, the Linked Accounts section shows which providers are connected to your account (email, Google, GitHub, Microsoft). You can link additional providers or unlink ones you no longer use, as long as you keep at least one active sign-in method.

## Sign-In Methods

You can sign in to Hamster Studio in several ways:

* **Email and password.** Standard email-based sign-in. Set or update your password from this page.
* **Sign in with Google.** Available on the sign-in and sign-up pages, plus Google One Tap on marketing pages for one-click access. Use the Linked Accounts section to add Google to an existing email account, or to remove it.
* **Other social providers.** GitHub and Microsoft sign-in are gated by per-workspace flags. If your workspace has them enabled, they appear on the sign-in screen and in Linked Accounts.

If you signed up with Google and want the option to also use email and password (for example, when an authenticator app is your primary security key), use the "Link email/password" option in Linked Accounts to add password-based sign-in to the same account.

## Key Capabilities

* **Password update**: Change the password associated with your email sign-in. Only available if you use password-based authentication.
* **TOTP multi-factor authentication**: Add a time-based one-time password factor using any TOTP authenticator app. You can register multiple named factors (e.g., one per device).
* **MFA factor management**: View all enrolled factors, see their verification status, and remove factors you no longer need.
* **Linked accounts**: Connect or disconnect social sign-in providers (Google, GitHub, Microsoft) from your account, giving you flexibility in how you sign in.
* **Safari-friendly MFA**: MFA verification works reliably in Safari. After you submit your code, the page commits the new session and routes you forward without getting stuck on the verification screen.

## MFA Enrollment in Detail

When you add a new MFA factor:

1. You give the factor a friendly name so you can identify it later (e.g., "iPhone Authenticator").
2. Hamster displays a QR code. Open your authenticator app, add a new entry, and scan the code.
3. Your app generates a six-digit rotating code. Enter it in the verification field.
4. Once verified, the factor is marked as active and required at future sign-ins.

Your authenticator app stores a secret linked to this code. If you lose access to your device, you will need to use an alternative sign-in [Method](https://tryhamster.com/docs/hamster-studio/skills-methods) or contact your workspace administrator.

## Password Recovery

If you forget your password, use the "Forgot password" link on the sign-in page. Enter the email address on your account and Hamster sends a recovery link.

For privacy, the recovery flow always responds with the same generic confirmation regardless of whether the email is on file — this prevents anyone from probing the system to discover which addresses have accounts. If you don't receive an email within a few minutes, double-check the address and try again, or reach out to your workspace admin.

## Connecting Third-Party Tools

Connecting integrations like Slack, Linear, Figma, Notion, Jira, and Google Drive happens in Workspace Settings → [Connections](https://tryhamster.com/docs/hamster-studio/connections), not in this page. Those flows open in a popup window so you don't lose your place in the [Brief](https://tryhamster.com/docs/hamster-studio/briefs) or document you were editing — the popup completes the auth, posts back to Hamster, and closes itself. If popups are blocked, the flow falls back to a same-window redirect.

If a connect attempt fails (the popup closes early, a browser extension blocks the redirect, etc.), the dialog asks you to try again. The retry succeeds in the vast majority of cases.

## Tips

* Name each MFA factor after the device it's on (e.g., "Personal phone", "Work laptop Authy"). This makes it easy to identify and remove factors when a device is lost or replaced.
* If you sign in with Google or GitHub and want to also be able to sign in with email and password, use the "Link email/password" option in the Linked Accounts section to add that method.
* Keep at least two sign-in [Methods](https://tryhamster.com/docs/hamster-studio/skills-methods) connected to your account so you're not locked out if one becomes unavailable.
* If MFA verification ever appears to hang in Safari, give it a couple of seconds — Safari is slower than other browsers to commit the post-verification session, and Hamster auto-routes you forward when the session lands.

## Related

* [Personal Profile](https://tryhamster.com/docs/hamster-studio/account-settings/personal-profile)
* [Getting Started](https://tryhamster.com/docs/hamster-studio/getting-started)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Hamster Studio","item":"https://tryhamster.com/docs/hamster-studio"},{"@type":"ListItem","position":4,"name":"Account Settings","item":"https://tryhamster.com/docs/hamster-studio/account-settings"},{"@type":"ListItem","position":5,"name":"Security","item":"https://tryhamster.com/docs/hamster-studio/account-settings/security"}]}
```
