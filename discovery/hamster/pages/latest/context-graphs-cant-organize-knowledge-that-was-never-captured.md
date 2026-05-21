---
description: The whole conversation assumes organizational knowledge exists somewhere and just needs better organization. But the most valuable organizational...
title: Context Graphs Can&#x27;t Organize Knowledge That Was Never...
image: https://pbs.twimg.com/media/G-FGlN7WsAExhuL?format=jpg&amp;name=large
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

# Context Graphs Can't Organize Knowledge That Was Never Captured

## The whole conversation assumes organizational knowledge exists somewhere and just needs better organization. But the most valuable organizational knowledge evaporates at the moment of creation.

![Context Graphs Can't Organize Knowledge That Was Never Captured](https://pbs.twimg.com/media/G-FGlN7WsAExhuL?format=jpg&name=large)

Lots of debate about ontologies lately. Prescribed vs learned. Palantir's expensive consultants vs structure that emerges from agent trajectories.

Watching the debate, I can't help but think we're missing a nuance that changes a lot.

The whole conversation assumes organizational knowledge exists somewhere and just needs better organization. Better schemas. Better learning algorithms. Better graph structures. As if the knowledge is sitting in systems, waiting to be properly arranged.

But watch what actually happens when a feature ships:

* A PM writes a spec.
* Engineers ask clarifying questions in Slack.
* Someone realizes the spec conflicts with a technical constraint.
* There's a 15-minute call where a tradeoff gets made.
* The scope narrows. The approach changes.
* The implementation diverges from the original spec based on what's actually possible. These new changes are captured with varying degrees across the org.
* The feature ships.

Where does the reasoning live now?

The spec is more than likely stale. It describes the original intent, not what shipped. The Slack thread is buried. The call wasn't recorded. The PR description says "implements feature X." The commit messages are technical, not contextual.

The decision that actually shaped the shipped product exists in the heads of the three people who were on that call. The constraint that forced the tradeoff. The alternative they rejected. The reason they chose this approach over that one.

In six months, one of them will have left the company. The reasoning leaves with them.

This happens thousands of times a day in every software organization. The decisions that govern how products actually get built are made in conversations, not systems.

In Slack threads that scroll away. In Zoom calls that end and vanish. In hallway conversations that never existed digitally at all.

No ontology, prescribed or learned, can organize knowledge that was never recorded.

[@kirkmarple](https://x.com/kirkmarple) made a valuable point in his response to this debate: the entity modeling problem is largely solved. [Schema.org](https://schema.org/) defines Person, Organization, Event. Microsoft's Common Data Model defines Account, Contact, Opportunity. Healthcare has FHIR. Finance has FIBO.

The nouns are known. We don't need to learn that "Account" is an entity or discover that "Contact" relates to "Organization." That work was done years ago.

So why are we still debating ontologies?

I think it's because the conversation is stuck on the wrong layer. We know what types of things exist. What happened and why remains unsolved.

Palantir's approach is expensive, but not because prescribed ontologies are inherently hard. It's expensive because forward deployed engineers have to sit in rooms and manually reconstruct context that was never captured in the first place. They interview people. They read old documents. They piece together what happened from fragments.

They're doing archaeology.

The ontology part is straightforward. The reconstruction is what takes months.

The "learned ontology" vision has a different problem. It assumes agent trajectories will reveal organizational structure. Let agents run, watch what they access, learn what matters.

But agent trajectories can only reveal patterns in data that already exists. If the reasoning happened in a Slack thread that the agent can't access, or a Zoom call that wasn't transcribed, or someone's head, it won't show up in the trajectory.

You can't learn structure from information that was never recorded.

There's also a bootstrap problem lurking here. You can't learn from agent trajectories until agents are running effectively. But agents can't run effectively without foundational context. "Run agents and let structure emerge" assumes you have something to run agents over.

The graph has to exist before you can walk it.

So both approaches are trying to solve the problem after the fact. One reconstructs through human effort. The other hopes to infer through machine learning. Neither addresses the core issue: the most valuable organizational knowledge evaporates at the moment of creation.

[@jayagup10](https://x.com/jayagup10)'s piece on decision traces offered something important: "The reasoning that connects data to action has never been captured as data."

We keep asking how to organize organizational knowledge. But maybe the better question is how we capture the reasoning before it disappears.

Once you see it that way, something interesting emerges about how the Context Graph debate is framed.

It's framed as an infrastructure problem. How do we build better databases? Better query layers? Better temporal models? How do we instrument existing workflows to capture what's happening? Build faster horses in an automobile age?

But instrumentation can only capture what flows through systems. The most important reasoning doesn't flow through systems. It happens in the gaps between them.

The PM's spec could be in Notion. The engineer's questions in Slack. The tradeoff discussion may have happened on Zoom. The decision was made verbally and never written down. The implementation is in GitHub. The UI/UX is somewhere in Figma. The outcome is in the analytics dashboard.

You can build the most sophisticated context infrastructure in the world, connect every system, instrument every workflow. You'll still miss the reasoning, because the reasoning happened in the spaces your infrastructure can't see.

This is what makes us believe context capture is fundamentally about workflow, not infrastructure.

You don't solve it by building better pipes between existing systems. You solve it by changing where the work happens in the first place.

Consider why developers using [@cursor\_ai](https://x.com/cursor%5Fai) or [@claudeai](https://x.com/claudeai) have better context than developers using ChatGPT in one-off threads. They don't have better integrations. But it is where the work happens. The code is there. The files are there. The context isn't assembled from external systems. It's native to the environment.

The same principle applies to organizational knowledge. If the alignment conversation happens in Slack, the reasoning scatters across threads and vanishes. If the alignment conversation happens in a system designed to capture alignment, the reasoning persists as a natural byproduct.

The [Context Graph](https://tryhamster.com/concepts/context-graph) opportunity might not be about building infrastructure to observe and organize what happens elsewhere. It might be about building the surfaces where the important work actually happens. Where intent gets clarified. Where tradeoffs get made. Where alignment gets reached.

If you're the place where decisions happen, you don't need to reconstruct the decision trace. You emit it as exhaust.

This reframes what needs to be built.

The infrastructure play focuses on the read path. How do we query organizational knowledge? How do we give agents the context they need? Those are real problems, but they're downstream of a harder one.

The opportunity is the write path. Where does organizational knowledge get created? If you are that place, the read path solves itself. The context exists because it was born in your system, not reconstructed from fragments elsewhere.

There's a reason the [velocity gap](https://tryhamster.com/concepts/velocity-gap) exists in software teams. Individuals ship in hours with AI. Teams still ship in weeks. The bottleneck moved from implementation to alignment. The scattered, unrecorded process of figuring out what to build and making sure everyone agrees.

That alignment process is where organizational knowledge gets created. Every time a team aligns on what to build, they're generating context: the intent, the constraints, the tradeoffs, the decisions. Currently, that context evaporates into Slack and Zoom and documents that nobody updates.

The ontology debate is arguing about how to organize the museum. The opportunity is being present in the studio where the art gets made.

What needs to be built goes beyond better ontology, prescribed or learned. Beyond better temporal databases or decision trace infrastructure, though those matter.

The key is the surfaces where teams do the work that generates context in the first place.

The prescribed vs learned framing will keep circling because both are trying to solve capture through observation. The alternative is to stop observing and start hosting.

Be where the decisions happen. The Context Graph fills itself.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Latest","item":"https://tryhamster.com/latest"},{"@type":"ListItem","position":3,"name":"Context Graphs Cant Organize Knowledge That Was Never Captured","item":"https://tryhamster.com/latest/context-graphs-cant-organize-knowledge-that-was-never-captured"}]}
```
