---
marp: true
theme: default
paginate: true
---

# The Two Modes of Working

How Your Prompts Become Working Software

<!--
Welcome to Session 2. Last time we learned two ways to write prompts. Today we're going to understand something deeper: what makes these two methods fundamentally different, and how they work together.

We'll also see how Kahuna fits into this picture — but first, let's understand the concepts.
-->

---

# Recap: Two Ways to Write Prompts

| Method | What It Is | Character |
|--------|------------|-----------|
| **Literal Instructions** | Step-by-step enumeration | Clarity, execution |
| **G/R/S/O** | Goal, Rules, Strategies, Opening | Agency, exploration |

Session 1 taught you both approaches.

Now let's go deeper: **what makes them fundamentally different?**

<!--
Quick recap from last session. Literal instructions tell the AI exactly what to do step by step. G/R/S/O gives the AI room to make decisions within your boundaries.

Both are valid. But they're actually doing something very different.
-->

---

# What Makes Them Different

| | G/R/S/O (Generative) | Literal (Enumerative) |
|---|----------------------|----------------------|
| **Agency** | Enabled — AI makes decisions | Disabled — AI follows steps |
| **Clarity** | Flexible structure | Maximum constraint |
| **When to use** | Don't know the exact path | Know exactly what to do |

One enables **decision-making**. One enables **execution**.

<!--
The key difference is agency.

G/R/S/O gives the AI agency — room to explore, decide, figure out the approach. You define what success looks like; the AI figures out how to get there.

Literal instructions remove agency — the AI follows your steps exactly. No exploration, no decisions. Just execution.
-->

---

# They're Not Competing — They're Complementary

These aren't conflicting approaches. They're **two halves of a complete workflow**.

```
G/R/S/O enables agency    →    AI forms a meaningful design

Literal provides clarity  →    AI carries out that plan
```

You need both. But not at the same time.

<!--
Here's the key insight: these aren't competing methods where one is better than the other.

They're complementary. G/R/S/O lets the AI help you design something. Literal instructions let the AI execute what you designed.

Design, then execute. Think, then do.
-->

---

# The Natural Flow

```
┌─────────────────────────────────────────────────────┐
│   Your thoughts (vague, exploratory)                 │
│                │                                     │
│                ▼                                     │
│   G/R/S/O Prompt (exploration enabled)               │
│                │                                     │
│                ▼                                     │
│   AI generates design + plan                         │
│                │                                     │
│                ▼                                     │
│   You review and approve                             │
│                │                                     │
│                ▼                                     │
│   Code executes the plan (literal mode)              │
└─────────────────────────────────────────────────────┘
```

<!--
This is the natural flow of working with AI.

You start with vague thoughts. You write a G/R/S/O prompt to explore options. The AI generates a design and an implementation plan. You review it. Then execution happens in literal mode — following the plan step by step.

Think first, then do. We'll see later how this maps to tooling.
-->

---

# What G/R/S/O Produces

When you prompt with G/R/S/O, the AI explores options and makes decisions.

Those decisions get captured in:

| Artifact | What It Contains |
|----------|------------------|
| **Design Document** | What we're building and why |
| **Implementation Plan** | How to build it (step by step) |

The plan IS the literal instructions for the next phase.

<!--
When you give the AI a G/R/S/O prompt — like "build me a login system" with your goals and constraints — the AI doesn't just start coding.

It produces two things: a design document explaining the approach, and an implementation plan with concrete steps.

That plan? It's the literal instructions that will guide execution.
-->

---

# The Plan IS Literal Instructions

| G/R/S/O Prompt | Implementation Plan |
|----------------|---------------------|
| "Build a login system that handles email and social auth, must be secure, prefer simple solutions" | "1. Create users table with email field... 2. Add bcrypt password hashing... 3. Implement login endpoint... 4. Add OAuth integration..." |
| Agency enabled | Agency constrained |
| AI decides approach | AI follows steps |

G/R/S/O exploration **produces** literal instructions.

<!--
Look at the transformation.

The G/R/S/O prompt leaves room for decisions: what approach? What order? What libraries?

The implementation plan removes that room. It's step-by-step. The decisions have been made.

This is how the two methods connect. One produces the other.
-->

---

# Why This Matters

Without G/R/S/O, you'd have to know every step yourself.

Without the plan, you'd never reach execution.

The design document + plan is the **bridge** between thinking and doing.

<!--
Why does this matter?

If you only had literal instructions, you'd need to know every step of building a login system before you started. Most of us don't.

If you only had G/R/S/O, you'd explore forever without ever shipping.

The documents — the design and the plan — are the bridge. They capture decisions so execution can happen.
-->

---

# Why the Design Document Exists

Without an explicit design phase, AI often **skips straight to code**.

| What AI Thinks | What Actually Happens |
|----------------|----------------------|
| "I know what to build" | Skipped exploration → wrong approach |
| "Let me just write it" | No design to review → surprises later |
| "This is obvious" | Conflated thinking with doing |

The design document **forces** thinking to complete before execution begins.

<!--
Here's something critical to understand.

Without an explicit design phase, AI tends to skip straight to writing code. It thinks it knows what to build, so it just starts building.

But it often doesn't know — not really. It's conflating "having a vague idea" with "having a plan."

The design document forces the AI to complete the thinking work as Step 1. You get to review what it's proposing before it writes any code.
-->

---

# Your Job: Understand the Proposal

You don't need to understand every line of code.

You **do** need to understand the design proposal:

| Ask Yourself | Why It Matters |
|--------------|----------------|
| What is being built? | Catches misunderstandings early |
| How does it change things? | Reveals scope and impact |
| Does this match what I wanted? | Confirms alignment before execution |

This is the core skill of working with AI: **reviewing the design**, not the code.

<!--
Your job as the human is to understand the proposal — not the implementation details.

You don't need to read every line of code. You need to understand: what is the AI proposing to build? How will it change things? Does this match what you actually wanted?

This is abstract understanding. And it's THE core skill of working with AI copilots. You're learning to review designs, not debug code.

What "understanding the design" means is different for each situation. You learn it through practice.
-->

---

# But Here's the Catch

G/R/S/O and Literal are **opposite modes**:

| | G/R/S/O | Literal |
|---|---------|---------|
| Making decisions | ✓ | ✗ |
| Following decisions | ✗ | ✓ |
| Exploring options | ✓ | ✗ |
| Executing chosen option | ✗ | ✓ |

Like inhaling and exhaling — both necessary, but **not simultaneous**.

<!--
Here's the catch. You can't do both at the same time.

When you're exploring options, you're not executing. When you're executing, you're not exploring.

They're opposite modes. Complementary, but mutually exclusive.

This creates a problem.
-->

---

# The Handoff Problem

How do you get from "exploring" to "executing"?

You need something to **carry the decisions** from one mode to the other.

That's the document.

The design doc + plan is the **continuity artifact** — it carries context between modes.

<!--
If the modes can't coexist, how do you transition between them?

You need something that persists — something that captures what you decided during exploration, so it's available during execution.

That's the document. It's not just documentation. It's a continuity artifact. It carries your decisions across the mode boundary.
-->

---

# The Full Picture

```
┌─────────────────────────────────────────────────────┐
│   GENERATE (G/R/S/O mode)                            │
│   ───────────────────────                            │
│   • Exploration enabled                              │
│   • Agency: AI makes decisions                       │
│   • Output: Design decisions                         │
│                    │                                 │
│                    ▼ crystallizes into               │
│                                                      │
│   DOCUMENTS (Design + Plan)                          │
│   ─────────────────────────                          │
│   • Captures what was decided                        │
│   • Carries context between modes                    │
│   • Bridge from thinking to doing                    │
│                    │                                 │
│                    ▼ guides                          │
│                                                      │
│   EXECUTE (Literal mode)                             │
│   ──────────────────────                             │
│   • Implementation happens                           │
│   • Agency: AI follows the plan                      │
│   • Output: Working software                         │
└─────────────────────────────────────────────────────┘
```

<!--
Here's the full picture.

Part 1 — thinking work: exploration, agency, decisions being made.

Documents: the bridge that captures those decisions.

Part 2 — implementation: following the plan, decisions already made.

This is the fundamental structure of working with AI on anything complex: think first, then do.
-->

---

# Kahuna: Structuring This Workflow

This is exactly how Kahuna works:

| Phase | What Happens | Kahuna's Role |
|-------|--------------|---------------|
| **Design** | G/R/S/O exploration | Design subagent thinks through the approach |
| **Approval** | You review the plan | Kahuna waits for your go-ahead |
| **Implementation** | Literal execution | Implementer subagent follows the plan |

The workflow we just described? Kahuna structures it for you automatically.

*Keep this in mind for Lecture 3 — we'll go deeper into how this orchestration works.*

<!--
Here's something important: everything we just described — the design phase producing documents, waiting for approval, then execution following the plan — this is exactly what Kahuna does.

Kahuna has a design subagent that works in G/R/S/O mode. It explores, makes decisions, produces a design and plan. Then it waits for you to approve. Only then does the implementer subagent take over, following the plan in literal mode.

You don't need to understand the details of how this orchestration works yet. That's coming in Lecture 3. For now, just notice: the workflow we've been describing is the workflow Kahuna automates.

When you use Kahuna, you're using this exact pattern: think first, approve, then execute.
-->

---

# When Documents Accumulate

As you work, documents accumulate:

- Design decisions from past projects
- Plans (current and old)
- Notes, research, alternatives considered
- Code, configurations, dependencies

This is **documentation space** — it grows over time.

<!--
Now let's talk about what happens as you work.

Documents accumulate. Every design decision, every plan, every note. Over time, you build up a body of documentation.

This is good — it's your project's knowledge. But it also creates a challenge.
-->

---

# When Things Change

Projects evolve. What happens to old documents?

| Change | Problem |
|--------|---------|
| Requirements change | Old plans become wrong |
| Decisions get revised | Old designs become misleading |
| Code gets refactored | Old docs don't match reality |

This is **documentation time** — information ages and can become stale.

<!--
Projects change. Requirements evolve. You make different decisions.

But the old documents don't disappear. That plan from two weeks ago? Still there. That design decision you reversed? Still in your docs.

This is documentation time — the dimension where information ages.
-->

---

# Context Poisoning Revisited

Remember Session 1's context poisoning? The balloon animals problem?

There's a **deeper form**:

| Source | Problem |
|--------|---------|
| Old design alternatives | AI still considers abandoned approaches |
| Debugging tangents | Past confusion influences new work |
| Outdated plans | AI follows wrong instructions |

Old documents can **poison** new work.

<!--
Remember context poisoning from Session 1? Where irrelevant content — like balloon animals in a Python tutorial — pollutes the AI's attention?

There's a deeper form. Old documents. Abandoned approaches. Outdated plans.

If you give the AI your whole project history, the old stuff can poison the new work. The AI might follow an outdated plan or consider alternatives you already rejected.
-->

---

# The Need for Context Engineering

To work effectively across modes, you need to:

- Know what documents exist
- Keep them current (or mark them obsolete)
- Give the AI the **right context** at the right time

This is **context engineering** — managing what the AI sees.

<!--
This is why context engineering matters.

You can't just dump everything on the AI and hope for the best. You need to curate. What's current? What's obsolete? What's relevant to this specific task?

Managing what the AI sees is as important as what you ask it to do.
-->

---

# Practical Tips

**For your documents:**
- Keep design docs current — update when decisions change
- Mark obsolete plans clearly (don't just delete them)
- Separate "decided" from "exploring"

**For your AI:**
- Tell it what's current vs. historical
- When in doubt, ask it to summarize what it knows
- Start fresh if context gets too polluted

<!--
Some practical tips.

For your documents: keep them current, mark what's obsolete, separate what's decided from what you're still exploring.

For your AI: be explicit about what's current. Ask it to summarize its understanding. And if context gets too polluted, sometimes the best move is starting a fresh conversation with just the relevant artifacts.
-->

---

# Kahuna: Managing Context Automatically

Remember context poisoning? Kahuna helps prevent it:

| Problem | How Kahuna Helps |
|---------|------------------|
| Documents accumulate | Consolidates when information grows too large |
| Things change | Resolves inconsistencies or escalates to you |
| Wrong context loaded | Retrieves relevant information for each task |

You manage the content. Kahuna manages the context.

*This becomes even more important as projects grow — which we'll explore in Lecture 3.*

<!--
This is the second way Kahuna helps you.

Remember the context poisoning problem we just discussed? Old documents, outdated plans, abandoned approaches — all of that noise that can confuse new work.

Kahuna handles this. When documents accumulate too much, Kahuna consolidates them. When things change and create inconsistencies, Kahuna either resolves them automatically or asks you about them. When you start a new task, Kahuna retrieves the relevant context — not everything, just what matters.

You focus on what you're building. Kahuna focuses on managing the context around it.

As your projects grow, this becomes more and more valuable. We'll see how this scales in Lecture 3 when we talk about orchestration in more depth.
-->

---

# Optional Assignment

Practice what you've learned with a hands-on exercise:

**Two-Mode Workflow** — Walk through the G/R/S/O → Plan → Execute flow yourself

**Where to find it:**

📁 `outreach/courses/ai-collaboration/session-2/assignments/`

*Optional but recommended before Lecture 3.*


<!--
Before we wrap up, I want to point you to the optional assignments for this session.

These are hands-on exercises that let you practice what we covered today. The first assignment walks you through the two-mode workflow — writing a G/R/S/O prompt, reviewing the design it produces, then watching execution happen.

The second assignment focuses on document review — the skill of understanding what an AI is proposing without needing to understand every line of code.

The third assignment is about context curation — identifying what's relevant versus what's stale.

You can find all of these in the assignments folder. They're optional, but I recommend trying at least the first one before Lecture 3. It'll make the material much more concrete.
-->

---

# Putting It All Together

```
1. Write G/R/S/O prompt (exploration mode)
         │
         ▼
2. AI generates design + plan
         │
         ▼
3. You review and approve
         │
         ▼
4. Code mode implements (execution mode)
         │
         ▼
5. Documents capture what was decided
         │
         ▼
6. Kahuna maintains context for next time
```

This is the workflow. Two modes, documents bridging them, context managed.

<!--
Here's the complete workflow.

G/R/S/O exploration produces a design and plan. You review it. Code mode executes. Documents capture the decisions. Kahuna maintains context.

Two modes. Documents bridging them. Context managed automatically.
-->

---

# Key Takeaways

1. **Two modes exist:** G/R/S/O (generative) and Literal (enumerative)

2. **They're complementary:** One enables design, one enables execution

3. **Documents bridge them:** The plan carries decisions between modes

4. **Context accumulates:** Old documents can poison new work

5. **Tools help:** Kahuna structures the workflow and manages context

<!--
Let's recap.

Two modes — generative and enumerative. They're complementary, not competing.

Documents bridge the modes — they carry your decisions from exploration to execution.

Context accumulates and can cause problems. That's why tools like Kahuna exist — to help you manage the workflow and context automatically.
-->

---

# Next Steps & Lecture 3 Preview

**Before Next Session:**

- [ ] Try the optional assignments (especially Assignment 1)
- [ ] Notice the two modes in your own AI interactions
- [ ] Pay attention to when you're exploring vs. executing

**Coming in Lecture 3: The Generate-Critique Cycle**

Today: Linear flow (explore → document → execute)

Next: How to **cycle** between generating and critiquing for quality

- When to switch from exploring to evaluating
- How iteration improves output
- Deeper dive into Kahuna's orchestration

<!--
Here's what I recommend before next session.

First, try the optional assignments — especially the first one. Walking through the two-mode workflow yourself will make everything click.

Second, start noticing the two modes in your own AI interactions. When are you exploring options? When are you executing a plan? Pay attention to the shift.

In Lecture 3, we're going to build on this foundation. Today we covered the linear flow — from exploration to execution, with documents bridging the gap.

Next time, we'll learn how to cycle. Not just one pass through, but generate, critique, refine, repeat. That's how you get quality — through iteration, not perfection on the first try.

We'll also go deeper into how Kahuna orchestrates this cycle. Remember those subagents I mentioned? We'll understand them properly next time.
-->

---

# Questions?

```
Two modes.
Documents bridge them.
Context matters.
```

Remember:
- G/R/S/O for exploration
- Literal for execution
- The plan IS the bridge

<!--
Any questions before we wrap up?

The core message: two modes, documents bridge them, context matters.

G/R/S/O when you're exploring. Literal instructions when you're executing. The plan that comes out of exploration IS the literal instructions for execution.

See you next session for the generate-critique cycle.
-->
