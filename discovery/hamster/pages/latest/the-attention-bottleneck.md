---
description: Your best engineer is mass-producing code. Your team is shipping at the same speed as last year. The math doesn&#x27;t add up until you look at the way...
title: The Attention Bottleneck
image: https://pbs.twimg.com/media/G-PVng6XQAAnAsT?format=jpg&amp;name=large
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

# The Attention Bottleneck

## Your best engineer is mass-producing code. Your team is shipping at the same speed as last year. The math doesn't add up until you look at the way individuals and teams use AI.

![The Attention Bottleneck](https://pbs.twimg.com/media/G-PVng6XQAAnAsT?format=jpg&name=large)

Your best engineer is mass-producing code. Your team is shipping at the same speed as last year. The math doesn't add up until you look at the way individuals and teams use AI.

Traditionally, 10 people produce roughly _x_ units of work per week. Linear relationship between headcount and output. Need more output? Hire more people.

With AI tools, each of those 10 people can now produce **5x** to **10x** units of work individually. The output capacity per person multiplied. But when you put them together as a team, something strange happens.

They still only ship like a team of 10.

The individual gains are real. You can measure them. Your best engineer closes tickets faster than ever. But the team velocity barely moves. Sprint capacity stays flat. Cycle time doesn't improve.

Where did the gains go?

We lived this during early [@taskmasterai](https://x.com/taskmasterai) days. The tool helps developers break down work and ship faster, and the community exploded. Hundreds of PRs poured in, many of them generated with the help of Taskmaster itself. Our output capacity as maintainers was theoretically unlimited. Our attention capacity was three people.

We couldn't review fast enough. We couldn't verify that contributions aligned with the project's direction. We couldn't coordinate across parallel efforts that sometimes conflicted with each other. The PRs kept coming. Our attention stayed fixed.

There exists real whiplash when the review workflow is confronted with a volume of production that exceeds its capacity. We got all sorts of amazing PRs across all types of functionality. They were technically great, but our capacity to work out what needs to be merged, what needs to be deprioritized or rescoped, or outright rejected, was completely capped and at its limit. Engineering leads get PR review whiplash too. PMs get whiplash too when the speed at which direction can be set and work prioritized is dwarfed by the speed at which the work is delivered.

The gains disappear into the gap between individual output and team capacity. Each contributor can produce more. We just couldn't attend to more.

That experience is part of why we started building [Hamster](https://tryhamster.com/product/studio). Planning and generation were solved. Attention had become the bottleneck. It became obvious AI was a point of leverage to help us connect the dots and attend to more PRs than we otherwise could by piecing together context and direction on the go.

Our attention being fixed, it became clear that we could only benefit from the gains in delivery only if matching gains were made to our ability to piece together product strategy as fast as we could deliver against it.

## The Attention Constraint

In the old model, the constraint was production. How fast can people type, think, build? Hire more people, get more production. The math was linear and intuitive.

Now production is nearly free at the individual level. Agents can generate code, content, analysis, artifacts at a pace that would have seemed absurd three years ago. But teams are made of humans, and humans have fixed attention. The constraint shifted from how much individuals can produce to how much the team can attend to.

Consider what attention actually gets spent on with a team using AI.

**Direction** means defining what should be built, setting constraints, clarifying intent. You can't delegate "figuring out what we actually need" to an agent. The agent will happily build whatever you describe, including the wrong thing described confidently.

**Verification** means reviewing what agents produced, checking quality, catching errors, noticing when something technically works but subtly misses the point. This requires judgment, context, and understanding of what you were actually trying to achieve.

**Coordination** means ensuring different workstreams don't conflict, maintaining coherence across the product, resolving ambiguity when it surfaces, noticing that two features are being built on incompatible assumptions before they collide.

The actual production (writing the code, generating the content, producing the artifacts) is increasingly low-attention. Agents do it. Humans spot-check.

This inverts the traditional ratio. Most human attention used to go to production, with some going to planning and review. Now most human attention needs to go to direction, verification, and coordination, with little going to production. But the habits, processes, and org structures are still optimized for the old ratio.

## The Formula

This brings us to **leverage ratio** — what we call the [velocity gap](https://tryhamster.com/concepts/velocity-gap) — the relationship between human attention input and useful output (whether merged PRs or otherwise).

_Leverage Ratio = Output / Human Attention_

In the traditional model, this ratio was roughly 1:1\. One unit of attention produced one unit of output. A developer spent an hour writing code, got an hour's worth of code.

With AI tools, the theoretical ratio explodes. One unit of attention could direct ten units of output in parallel. But theoretical isn't actual.

The actual leverage ratio depends on what level of abstraction humans operate at.

**Low abstraction** means humans stay close to production. They write prompts for individual functions, review every line of generated code, manually verify each output. The attention cost stays high. Tab completion is powerful. Leverage ratio: maybe 2x.

**Medium abstraction** means humans direct at the feature level. They define what a component should do, review the integrated result, verify against acceptance criteria. Compiling context into a clear plan. Attention cost decreases. Leverage ratio: 4-5x.

**High abstraction** means humans direct at the outcome level. They define what success looks like, set constraints and boundaries, verify that outcomes were achieved. Attention focuses on direction and coordination, not production details. Leverage ratio: 8-10x.

Leverage doesn't mean working faster. It's a move up the control stack, away from execution and toward outcomes, so the same attention produces more output.

A senior engineer who can define a system architecture and verify outcomes operates at higher abstraction than a junior who reviews every generated function. Same attention input, dramatically different output.

It's the difference between Factorio and Civ: one focuses on systems implementation and resource management. The other is about strategy, coordination and long-term horizons.

Factorio rewards mastery of throughput, ratios, and execution details. Civ rewards choosing _what_ to pursue, _when_ to pursue it, and _how_ systems interact over time. Both require skill, but they operate at different layers. Human leverage emerges when we stop optimizing individual moves and instead shape the systems that produce them.

## The Limits

There's a ceiling. Humans can only compress their attention so far before quality degrades.

When leverage ratio exceeds sustainable limits, verification slips, reviews get rushed, edge cases get missed and bugs ship. Those bugs consume attention in the next cycle. Support tickets, debugging sessions, hotfixes, postmortems. Now there's even less attention available for the new work coming in. Verification slips further. More bugs ship.

The faster individuals produce, the faster this spiral spins. Each cycle leaves less attention for direction and coordination, which means more misalignment, which means more rework, which means less attention still.

You can't hire your way out of this. Adding people adds coordination overhead. More nodes in the network means more alignment conversations, more potential for conflict, more context that needs to be shared. Attention doesn't scale linearly with headcount. Past a certain point, it doesn't scale at all.

## The New Hiring Question

The traditional hiring question was _"How many people do we need to produce this much work?"_

The new question is: _"How many people do we need to direct and verify this much work, and at what level of abstraction can they operate?"_

Different question with a very different answer. Usually a smaller number, but a different kind of person.

In the old model, you hired for throughput. Need more features? Hire more engineers. Need more content? Hire more writers. Headcount equaled output.

Now you hire for abstraction capacity. You need people who can operate at higher levels, who can direct work well, verify output effectively, and maintain coherence across a larger surface area. One "junior" person operating at 8x leverage suddenly outperforms three seniors operating at 2x.

The teams that figure this out will look like 10 people doing the work of 50\. They've identified what humans should do (direction, verification, coordination) and what agents should do (production). They've learned to operate at the level of abstraction that maximizes leverage without exceeding sustainable limits.

The world we're building (and the agents to operate it) have a massive role to play in enabling us to graduate to higher order work.

The teams that don't commit will keep hiring like it's 2019, wondering why headcount isn't translating to output, burning attention on low-abstraction work that agents should handle while starving the high-abstraction work that only humans can do.

Individual productivity multiplied but team productivity didn't. The gap is leverage. Closing it is what the [Hamster Method](https://tryhamster.com/method) is about.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Latest","item":"https://tryhamster.com/latest"},{"@type":"ListItem","position":3,"name":"The Attention Bottleneck","item":"https://tryhamster.com/latest/the-attention-bottleneck"}]}
```
