# Poliglot RARS

## What is Poliglot?

Poliglot's mission is to **amplify human agency**. We build technology that puts _you_ in a position to have more control over your life or your business, and empowering you to take more intentional actions to achieve your goals.

For our first magic trick, we're tackling some of the biggest problems and blockers of AI adoption.

We've watched industries try to figure out how AI fits into existing organizations, systems, and workflows, and, well, it's been underwhelming.

### The Problem

Everything we do, for the most part, is some form of an assembly-line. Whether it be an actual manufacturing assembly-line, a software development workflow, a customer onboarding workflow, or financial portfolio management, all follow an assembly-line-like pattern.

Now, if you think about it from an even grander scale, our global organizations are basically just much bigger assembly-lines manufacturing business goals.

**It doesn't matter how efficient a single process is if the overall _system_ isn't.** The same organizational architectures that worked for human-driven processes won't work for AI.

We've watched organizations drop task-oriented AI solutions into existing processes, then complain about why they didn't see much efficiency gains. Your forgot the first rule!

### Our Solution is Simple

Rather than using AI to optimize individual processes, we're building the AI that optimizes the global _system_ by engineering **autonomous operating models that actually scale**.

We're building a cloud ecosystem to build and execute composable, autonomous operating models.

We'll provide the tools to **codify your business**, and an AI operating system through which to execute it.

## What is RARS?

We weren't convinced with the current approaches to AI-driven workflows. After evaluating concepts like agents, multi-agent systems, and observability and evaluation trends, and we determined there were several major problem areas: **trust**, **control**, **determinism**, and **verifiability**.

So we started from scratch, and **we rethought _everything_**.

RARS is the NeuroSymbolic AI architect and operating system of your business operations.

It is a symbiosis of the reasoning capabilities of probabilistic AI (eg. LLMs) and a symbolic programming runtime that grounds the AI in your codified operating models.

Basically, RARS is **the world's most powerful coding agent**.

### Verifiable

If you look at where AI has had the biggest impact, it's by far been in software engineering, specifically coding.

You might think this is because software engineers are already in the space, are more likely to use the tools early, or one of many other reasons, but we have a different take: it's because software has version control.

> Brandolini's law: The amount of energy needed to refute bullsh\*t is an order of magnitude bigger than that needed to produce it.

When you use AI to code, do you evaluate the output by going through the traces and reasoning processes of the AI every step of the way? Or do you just look at the GIT diff?

At Poliglot, we tend to just look at the PR showing the exact lines of code that were changed, and make a decision of whether if it solves our problem.

RARS exposes a **GIT diff for your business objects**. It's stateful execution layer provides a staging-ground for multi-step workflows that turns changes to your operating resources (contracts, project management issues, budgets, accounting statements, etc.) into a structured diff that can be reviewed, committed, or iterated on.

No more reviewing full traces, evals, and reasoning chains, but, our native observability system still provides it if you really need it.

Learn more: [Persistent Memory](https://www.poliglot.io/develop/architecture/runtime/persistent-memory) | [Provenance](https://www.poliglot.io/develop/guides/foundations/provenance)

### Trustworthy

When multiple agents, workflows, and human operators all contribute to the same business state, trust requires more than logs. It requires an **aligned world view**.

RARS aligns every actor and every action around a single, collaborative representation of your operational state. **Everything is a structured observation**: an attestation made by a specific agent, as part of a specific process. When an AI agent updates a record, a service syncs external data, or a human approves a change, they're all contributing observations to the same shared state. No actor operates in isolation. No data exists without attribution.

This shared world view is what makes collaboration between humans, AI, and automated systems actually work. Everyone sees the same state. Everyone's contributions are structured the same way. And every change, down to the individual field, carries a complete chain of attribution: who, why, when, and as part of what process. That's not a forensic investigation. It's a direct lookup.

Learn more: [The Collaborative Runtime](https://www.poliglot.io/develop/architecture/runtime/collaborative-runtime) | [Provenance](https://www.poliglot.io/develop/guides/foundations/provenance)

### Controllable

Static role-based access control is dangerous for AI. A role grants permissions unconditionally, regardless of whether the business context supports the action. An AI with "approver" access can approve anything its role allows, whether or not a risk assessment was completed, a budget was reviewed, or the request makes any sense at all.

RARS enforces **situational access control**: permissions that evaluate the live state of the business at the moment of execution. Authorization policies carry conditions that are evaluated against your operational state in real time. Not just "does this role have permission," but "does the current situation support this action."

For example: an AI agent tries to dispatch a $250,000 electrical work order. At execution time, the system evaluates: has the risk assessment been completed? Has a licensed electrical engineer signed off? Is the project budget sufficient to cover the cost? Has a manager with the appropriate authority approved it? If any condition isn't met, the operation is denied, regardless of the agent's role.

You grant broad operational capability while maintaining precise control over when that capability can and should be exercised.

Learn more: [Situational Access Control](https://www.poliglot.io/develop/architecture/trust-and-security/situational-access-control) | [The Identity Model](https://www.poliglot.io/develop/architecture/trust-and-security/identity-model) | [Security](https://www.poliglot.io/develop/guides/foundations/security)

### Deterministic Orchestration & Execution

The fundamental problem with AI workflows is the ReAct loop: reason, act, observe, reason again. Every step is a fresh inference. Multi-step plans drift. The execution is as non-deterministic as the reasoning.

RARS introduces **ProActive AI**: your AI manipulates your business through a concept-oriented programming runtime where your domain objects have types, behaviors, and inheritance hierarchies, just like classes in OOP. Actions are methods on concepts. Type-based dispatch provides object-level overloads for semantically distinct resources. The symbolic engine executes workflows deterministically against this typed graph.

The AI plans. The engine executes. The plan runs as written, not re-inferred at each step. Within a single script, deterministic API calls, AI reasoning steps, and human approvals compose into one executable plan with aligned I/O contracts.

Every action, whether a deterministic service call or an agentic reasoning task, has an explicit I/O contract validated against your business constraints. An AI sub-agent's output is held to the same validation as a direct API response. This is **Contractual AI**: the contract guarantees the output structure regardless of how the result was produced. Continuous validation acts as compiler diagnostics for your business state, catching violations in real time.

Learn more: [Contractual AI](https://www.poliglot.io/develop/architecture/trust-and-security/contractual-ai) | [The NeuroSymbolic Engine](https://www.poliglot.io/develop/architecture/runtime/neurosymbolic-engine) | [The Semantic Operating System](https://www.poliglot.io/develop/architecture/operating-model/semantic-os) | [Designing Actions](https://www.poliglot.io/develop/guides/actions)

## Key Concepts

Before diving in, here are the foundational concepts you'll see throughout the documentation:

- **Workspace**: an organizational environment where matrices are installed and your team collaborates.
- **Context**: a persistent working environment where RARS operates. Like a business context but in the digital world: you have information in front of you, you know which systems to use, you remember what happened before, and you pick up where you left off.
- **Matrix**: a codified operating model for a business domain. Defines the domain's concepts, rules, operations, and systems of record. Versioned, composable, installable.
- **Action**: a declared operation RARS can execute. Can be a deterministic API call, an orchestrated multi-step workflow, an AI reasoning task, or a human approval. All share the same verifiable I/O contract.
- **Observation**: every piece of data from your operations state, and every change RARS makes is recorded as an observation with full provenance: who, what, when, and why, and as part of which process. Your entire business becomes auditable through a unified system.
