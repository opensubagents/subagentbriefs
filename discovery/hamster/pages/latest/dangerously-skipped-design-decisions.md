---
description: The middle of software work used to absorb most of the time, attention, and craft. Now agents can produce working code from goals and context. The...
title: Dangerously Skipped Design Decisions
image: https://pbs.twimg.com/media/G-JoZCfWAAA2Uo7?format=jpg&amp;name=large
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

# Dangerously Skipped Design Decisions

## The middle of software work used to absorb most of the time, attention, and craft. Now agents can produce working code from goals and context. The middle is getting thinner. What matters is forming the right intent and verifying the outcome.

![Dangerously Skipped Design Decisions](https://pbs.twimg.com/media/G-JoZCfWAAA2Uo7?format=jpg&name=large)

I appreciated [@karrisaarinen](https://x.com/karrisaarinen)'s perspective: "The center of software work is moving."

His observation: the middle of software work (the actual coding) used to absorb most of the time, attention, and craft. Now agents can produce working code from goals and context. The middle is getting thinner. What matters is forming the right intent and verifying the outcome.

The middle did get thinner. But I've been thinking about what "the middle" actually is and I don't think it disappears. It transforms and relocates.

The middle used to absorb two different things: implementation effort and discovery.

Implementation effort is the mechanical work. Typing code, looking up syntax, debugging runtime errors, writing tests. This is genuinely compressing. Agents handle it well.

Discovery is different.

You'd start a feature with a rough spec. Halfway through, you'd hit an edge case nobody anticipated. You'd make a judgment call and keep going. You'd realize the API doesn't behave the way the docs suggested. You'd notice the design doesn't account for the empty state.

By the time you finished, you understood the problem better than when you started. The implementation process surfaced decisions that needed to be made.

When agents do the implementation, that discovery still happens. But now the agent is making those judgment calls. The edge cases still exist. The API still behaves unexpectedly. The empty state still needs handling.

The question is: who's making those decisions now?

This matters more than it used to. Agents are getting more autonomous. The default is shifting toward letting them run longer, with less supervision. The pressure to abdicate is increasing just as the cost of abdication compounds.

Over the last few months, I've seen three patterns emerge:

## Front-loading

Teams try to do all the thinking before execution. Anticipate every edge case, specify every behavior, constrain every choice. Make intent so precise that agents never need to make judgment calls.

In practice, this looks like week-long spec processes. PRDs that try to enumerate every state, every error, every interaction. Technical design docs that leave nothing ambiguous.

This works for well-understood problems. But it's exhausting, and it doesn't scale. You're trying to predict decisions you can only discover through building. The spec becomes a bottleneck. And the moment reality diverges from the document, you're back to improvising anyway.

## Abdication

Let agents iterate autonomously. Ship fast, fix later. Maybe not at all. The agent generates something, tests pass, you merge. You may not even care to know what the code does, only that it does it.

The agentic equivalent of `--dangerously-skip-permissions`, except what you're skipping isn't file access. It's design.

When you don't take control of discovery, the agent fills the empty spaces. It takes liberties. It makes design decisions based on patterns in its training data, based on whatever context fits in the window.

Not based on your product vision, your users, your constraints.

Each decision seems small. Handle this error with a modal. Store this state in local storage. Structure this component as a class. Use optimistic updates here, loading spinners there. None of them are wrong exactly. But none of them were chosen either.

You ship, something feels wrong, and you can't articulate why. Because the wrongness isn't a bug. It's the accumulation of a thousand small decisions that nobody made intentionally.

This is why vibecoding inevitably leads to not knowing your own codebase. It's the opposite of what [briefs](https://tryhamster.com/concepts/briefs-not-tickets) are designed to solve. You can generate 150k lines of sophisticated code with an agent running overnight. The results can be impressive. But the prospects for improvement or collaboration are bleak.

What you gain in velocity, you trade away in clarity. The codebase becomes a black box you generated rather than a system you understand. And the debt comes due when you need to change direction, onboard someone new, or debug something subtle.

## Captured discovery

Accept that discovery will happen during execution. But keep [humans in the decision loop](https://tryhamster.com/concepts/humans-and-agents) while removing them from the implementation loop.

In practice, this means building checkpoints into how you work with agents. When the agent hits an edge case, it surfaces the options rather than picking one. When there's a tradeoff between approaches, it pauses and asks. When an assumption is required, it makes the assumption explicit rather than burying it in implementation details.

The decisions that used to get made unconsciously during implementation become visible, explicit, owned.

This requires tooling and discipline. A simple version: require the agent to maintain a decision log as it works. Every judgment call, every assumption, every choice between alternatives. Review the log, not just the code. A more sophisticated version: agents that are architected to pause at decision points rather than defaulting to whatever pattern is most common in their training data.

This is slower than abdication in the short term. Dramatically faster in the long term, because the decisions compound rather than conflict. And because you actually understand what you've built.

Here's what's interesting: code itself can become a form of captured discovery.

Designers are skipping Figma sometimes, expressing interactions directly in code because agents make it fast. That code may never get merged. But if you share the prototype PR with your agent when building the real implementation, that code becomes context. The vibe-coded prototype becomes an alignment tool.

You can work like you vibe, provided there's amplification in the long run.

The driving question isn't whether to use agents aggressively. We want to do that at scale.

The question is whether the output feeds back into decisions you own or replaces decisions entirely. It's the difference between driving an F1 car at its limit around a circuit versus driving it headfirst into a wall on the first corner out of sheer horsepower.

The craft here isn't "directing agent work" in the sense of giving better prompts. It's creating the conditions where humans own decisions while agents own implementation. A structural challenge, not a prompting challenge.

The teams that figure this out won't just ship faster. They'll ship coherently. Each thing they build reinforces the last because the decisions are intentional and aligned.

The teams stuck on abdication will move fast and go nowhere. Generating code that technically works but doesn't add up to anything. Building products they can't explain, codebases they can't navigate, systems they can't evolve.

The middle didn't disappear. The implementation part compressed. The discovery part is still there, waiting for someone to own it.

If you don't, your agents will. And they won't tell you what they decided.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Latest","item":"https://tryhamster.com/latest"},{"@type":"ListItem","position":3,"name":"Dangerously Skipped Design Decisions","item":"https://tryhamster.com/latest/dangerously-skipped-design-decisions"}]}
```
