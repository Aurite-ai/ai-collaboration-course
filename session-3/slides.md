---
marp: true
theme: default
paginate: true
---

# Orchestrating Complex Work

How Sub-Agents Coordinate to Solve Big Problems

<!--
Welcome back. Session 2 ended with you coordinating phases—exploration then execution. Today we answer: what if the copilot could handle that coordination for you?
-->

---

# Session 2 Recap + The Next Question

| Session 2 | What You Did |
|-----------|--------------|
| Explore with G/R/S/O | You chose when and how to explore |
| Document the design | You reviewed and approved |
| Execute literal instructions | You decided when to switch |

**You coordinated.** But what if the copilot could coordinate for you?

<!--
Quick recap. In Session 2, you did the coordination—deciding when to explore, when to document, when to execute. Today we see what happens when the copilot takes over that coordination role.
-->

---

# When Copilot Takes Your Role

The copilot can do what you do—type a message to a copilot.

```
BEFORE:
Human types message → Copilot responds.

AFTER:
Human makes decisions (approve/deny) → Copilot types message → Sub-Agent responds
```

When the copilot takes your role in the human→copilot relationship, that's a **sub-agent**.

*(You may also hear these called "subtasks"—same concept.)*

<!--
Here's the core insight. What do you do with a copilot? Type messages. What can the copilot do? Type messages. So it can take YOUR role—talking to another instance of itself. That's a sub-agent. The Orchestrator coordinates; the sub-agent does focused work.
-->

---

# Why Fresh Conversations?

| Same Conversation | Fresh Sub-Agent Conversation |
|-------------------|------------------------------|
| All accumulated context | Only the context it needs |
| May include irrelevant tangents | Focused on one task |
| Growing complexity | Clean slate |

**The Orchestrator chooses what context to include.**

This is context engineering in action—curating what each sub-agent sees.

<!--
Why fresh conversations? Remember context poisoning? A fresh conversation means the sub-agent sees only what the Orchestrator includes. No noise, no tangents. This pattern works with any AI coding assistant—it's not a feature of one tool, but a pattern any copilot can implement.
-->

---

# Sub-Agents Are Defined by Deliverables

| Sub-Agent Type | Deliverable |
|----------------|-------------|
| Research | Findings report with citations |
| Design | Design document |
| Planning | Implementation plan |
| Review | Assessment with findings |
| Implementation | Working, tested code |

**Sub-agents are defined by their output, not their activity.**

<!--
Sub-agents are defined by what they produce. A research sub-agent produces findings. A design sub-agent produces a design document. This output focus keeps work concrete and verifiable.
-->

---

# Context Isolation in Action

```
┌──────────────────────────────────────────────────┐
│  ORCHESTRATOR                                    │
│  (maintains big picture, coordinates)            │
├──────────────────────────────────────────────────┤
│         │              │              │          │
│         ▼              ▼              ▼          │
│  ┌──────────┐   ┌──────────┐   ┌──────────┐     │
│  │ Research │   │  Design  │   │ Implement│     │
│  │ sub-agent│   │ sub-agent│   │ sub-agent│     │
│  └────┬─────┘   └────┬─────┘   └────┬─────┘     │
│       ▼              ▼              ▼           │
│    Findings       Design         Working        │
│     Report       Document          Code         │
└──────────────────────────────────────────────────┘
```

Each sub-agent sees only what it needs. No cross-contamination.

<!--
Each sub-agent gets only the context relevant to its task. The research sub-agent doesn't see abandoned design alternatives. The Orchestrator passes along only what's needed—deliverables from prior phases, not all the work that produced them.
-->

---

# The Golden Rule

> **The more focused, more specific, and with fewer additional responsibilities, the better the AI performs.**

This applies to every AI interaction—prompts, modes, sub-agents, everything.

<!--
This is the most important principle in AI collaboration. You've experienced this—specific requests get better results. This isn't just a tip—it's the foundation of everything we're learning. Sub-agents work BECAUSE of this rule.
-->

---

# Focus Beats Breadth

| Request Type | What Happens |
|--------------|--------------|
| "Build me a web app with user accounts, email, payments, and reporting" | AI juggles too many concerns at once |
| "Design the user account system. Just the account system." | AI focuses deeply on one thing |

**The same AI performs differently based on how focused the task is.**

<!--
Compare these. The first asks the AI to think about five things simultaneously. The second asks about one thing. The same AI performs better on the focused task—not because it can't handle complexity, but because focus enables depth. This is why sub-agents work.
-->

---

# The Tension and Solution

**Complex work requires:**
- Multiple considerations
- Different phases
- Various kinds of thinking

**But AI performs best with:**
- Single focus
- Clear boundaries
- Specific deliverable

**Solution:** Break complex work into focused pieces. Each piece handled by a sub-agent.

<!--
This is the tension. Real projects involve many considerations. But AI performs best with focus. The answer is task decomposition—break complex work into focused pieces, each handled by a sub-agent. The golden rule is satisfied for each piece.
-->

---

# The Context Engineering Challenge

When you decompose tasks, you need to manage:

| Challenge | What It Means |
|-----------|---------------|
| **Context isolation** | Each sub-agent sees only what it needs |
| **Context handoffs** | Results flow between sub-agents cleanly |
| **Context coherence** | All sub-agents work toward the same goal |
| **Context freshness** | No stale information from old phases |

**This is why orchestration exists.**

<!--
Decomposition creates a challenge: managing context across multiple conversations. Isolation, handoffs, coherence, freshness—all of this is context engineering. Orchestration is the solution.
-->

---

# Documents Become Handoffs

Remember Session 2: documents bridge the modes.

In orchestration, documents serve as:
- **Handoffs** between sub-agents (clean context transfer)
- **Accumulated decisions** (what's been decided so far)
- **Filtered context** (no exploration noise)

```
Sub-agent 1 → Deliverable → Sub-agent 2 → Deliverable → Sub-agent 3
```

<!--
Remember how documents bridge exploration and execution in Session 2? Same role between sub-agents. The research sub-agent produces findings. That document—not all the research noise—becomes context for the design sub-agent. Clean handoffs.
-->

---

# The Core Triad

Three roles form the cognitive decision-making unit:

| Role | Function | When to Use |
|------|----------|-------------|
| **Orchestrator** | Coordinates and delegates | Complex, multi-phase work |
| **Architect** | Generates designs and plans | "What should we build?" |
| **Analysis** | Critiques and verifies | "Is this design right?" |

The triad produces **verified decisions** through iteration. Implementer comes after.

<!--
The Core Triad is the decision-making unit. Orchestrator coordinates. Architect generates designs. Analysis critiques and verifies. They cycle until agreement—then Implementer executes the agreed plan. The triad makes decisions; Implementer executes them.
-->

---

# The Architect Role — Generation

**What Architect does:**
- Explores options and possibilities
- Makes design decisions
- Creates plans with success criteria
- Proposes approaches to problems

**Key characteristic:** Architect *generates*—it creates new designs, new plans, new solutions.

**Trigger:** "What should we build?" or "Design the approach"

<!--
Architect is the generative force in the triad. It explores possibilities, makes design choices, and produces concrete plans. The key word is "generates"—Architect creates things that didn't exist before: designs, plans, decisions.
-->

---

# The Analysis Role — Critique

**What Analysis does:**
- Reviews designs against success criteria
- Finds problems and gaps
- Verifies quality before proceeding
- Challenges assumptions

**Key characteristic:** Analysis *critiques*—it finds what's wrong, missing, or unclear.

**Trigger:** "Is this design right?" or "Review this plan"

<!--
Analysis is the critical force in the triad. It reviews what Architect produced, compares it against success criteria, and finds problems. The key word is "critiques"—Analysis doesn't create, it evaluates. This separation is essential for quality.
-->

---

# The Generate-Critique Cycle

**This IS how the Core Triad works:**

```
┌──────────────────────────────────────────────────┐
│  Orchestrator delegates to Architect             │
│         │                                        │
│         ▼                                        │
│  Architect generates design ──► Analysis         │
│         ▲                          │             │
│         │      finds problems      │             │
│         └──────────────────────────┘             │
│                                                  │
│  Cycle continues until Analysis finds no flaws   │
└──────────────────────────────────────────────────┘
```

<!--
The generate-critique cycle isn't separate from the triad—it IS the triad in action. Architect generates, Analysis critiques, Architect revises, Analysis verifies. This continues until Analysis agrees the design is ready. The cycle IS the decision-making process.
-->

---

# How the Cycle Works

1. **Orchestrator** delegates design task to **Architect**
2. **Architect** produces design/plan with success criteria
3. **Orchestrator** delegates review to **Analysis**
4. **Analysis** reviews against criteria, finds problems
5. If issues found → back to **Architect** to revise
6. If no issues → **agreement reached**

**Key insight:** Neither generating alone (uncritical) nor critiquing alone (paralysis) produces quality. Cycling between them does.

<!--
Orchestrator coordinates the cycle—delegating to Architect, then Analysis, back to Architect if needed. The cycle ends when Analysis finds no problems. This is quality through iteration: generate, critique, revise, verify.
-->

---

# When Agreement Is Reached

| During the Cycle | After Agreement |
|------------------|-----------------|
| Design is evolving | Design is stable |
| Problems being found | No problems remain |
| Still deciding | Decision made |
| Not ready to build | Ready to build |

**Agreement means:** Analysis has verified the design. No remaining issues. Ready to execute.

<!--
Agreement is the cycle's exit condition. Analysis has reviewed the design and found no problems. The triad's work is done—the decision is made. Now execution can begin. This is why we separate decision-making from execution.
-->

---

# The Implementer — After Agreement

**Implementer is NOT part of the Core Triad.**

| Core Triad (decides) | Implementer (executes) |
|---------------------|------------------------|
| Makes design decisions | Follows the decided design |
| Generates and critiques | Compiles plan to code |
| Produces verified plans | Produces working code |

**Implementer:** Executes the agreed plan precisely. Follows designs without redesigning.

**Trigger:** "Build it according to the plan" (only after triad agreement)

<!--
Implementer comes after the triad agrees. It doesn't make design decisions—it executes the decisions the triad already made. This separation is crucial: deciding and executing are different activities requiring different modes of thinking. The triad decides; Implementer executes.
-->

---

# Writing Sub-Agent Prompts

A good sub-agent prompt includes:

1. **Context:** What the sub-agent needs to know
2. **Task:** What specifically to do
3. **Deliverable:** What to produce
4. **Success criteria:** How to know it's done

<!--
When writing a sub-agent prompt—or when the Orchestrator writes one—it needs four things. Context, task, deliverable, success criteria. This structure enables focus.
-->

---

# Example Sub-Agent Prompt

```markdown
## Context
We're building a quarterly sales report system.
Research findings attached below.

## Task
Design the data pipeline architecture.

## Deliverable
A design document explaining:
- Data sources and how to access them
- Transformation steps
- Output format

## Success Criteria
- All three data sources are addressed
- Transformations are specific enough to implement
- Output format matches stakeholder requirements
```

<!--
Notice the structure: context gives background, task says what to do, deliverable says what to produce, success criteria tell us how to verify quality. This is what the Orchestrator creates for each sub-agent.
-->

---

# Mode Selection Quick Reference

**Core roles (Kahuna's naming):**

| Task | Role | Why |
|------|------|-----|
| "Design the API structure" | **Architect** | Creating plans and designs |
| "Implement the login feature" | **Implementer** | Following a plan |

**Additional specialized modes (when available):**

| Task | Mode | Why |
|------|------|-----|
| "Find out what frameworks exist" | Research | Gathering information |
| "Is this design secure?" | Analysis/Review | Critiquing/verifying |
| "Why is this test failing?" | Debug | Finding problems |

<!--
The core roles—Architect and Implementer—handle most work. Specialized modes like Research, Analysis, and Debug exist in some copilots. If your copilot doesn't have a specialized mode, Architect can often handle research and analysis as part of its exploration.
-->

---

# Your Role — Approval Gates

| What Orchestrator Does | What You Do |
|------------------------|-------------|
| Breaks down the work | Approve the decomposition |
| Assigns roles | Verify the assignments make sense |
| Manages sub-agents | Review sub-agent outputs |
| Synthesizes results | Make final decisions |

**You don't coordinate. You decide.**

<!--
Your role is strategic. The Orchestrator proposes how to break down work—you approve. It assigns roles—you verify. It manages sub-agents—you review outputs. You don't coordinate; you decide.
-->

---

# The Progression

| Stage | Who Does the Work | Who Coordinates |
|-------|-------------------|-----------------|
| Before AI | You do the work | — |
| Session 1 | Copilot does the work | You coordinate (implicitly) |
| Session 2 | Copilot does phased work | You coordinate phases |
| **Session 3** | Copilot does decomposed work | **Copilot coordinates** |

**Improvement means replacing what YOU do with what the copilot can do.**

<!--
Here's the progression across all three sessions. Before AI, you did everything. Session 1, copilot started doing work. Session 2, you coordinated phases. Session 3, copilot takes over coordination. Improvement means progressively replacing your work with copilot's capabilities.
-->

---

# All Three Sessions Were Decomposition

| Session | Decomposition Level | What Gets Decomposed |
|---------|--------------------|-----------------------|
| Session 1 | Prompt | Vague request → G/R/S/O structure |
| Session 2 | Workflow | Monolithic work → Explore + Execute |
| **Session 3** | **Coordination** | **Your coordination → Copilot's coordination** |

**The entire course has been about task decomposition at increasing levels.**

<!--
Here's what you might not have noticed: all three sessions follow the same pattern. Session 1 decomposed prompts. Session 2 decomposed workflows. Session 3 decomposed coordination itself. Task decomposition at increasing levels—that's the entire arc.
-->

---

# Session 3 Cheat Sheet

| Concept | One-Liner |
|---------|-----------|
| **Golden Rule** | More focus = better AI performance |
| **Sub-agent** | Copilot takes your role (types message to copilot) |
| **Task Decomposition** | Break complex work into focused pieces |
| **Context Engineering** | Managing what each piece sees |
| **Orchestration** | Copilot coordinates decomposed tasks |
| **Core Triad** | Orchestrator + Architect + Analysis (decides) |
| **Implementer** | Executes after triad agreement |

<!--
Your cheat sheet. Golden rule: focus improves performance. Sub-agents: copilot takes your role. Task decomposition: break complex into focused. Context engineering: manage what each piece sees. Orchestration: copilot coordinates. Core Triad: Orchestrator, Architect, Analysis—the decision-making unit. Implementer executes after agreement.
-->

---

# Putting It All Together

You now have the complete picture:

| Session | What You Learned | Core Skill |
|---------|------------------|------------|
| **Session 1** | G/R/S/O prompts | Structuring your requests |
| **Session 2** | Two modes of working | Exploring vs. executing |
| **Session 3** | Orchestration | Letting the copilot coordinate |

**The pattern:** Task decomposition at increasing levels.

From structuring prompts → to phasing your work → to delegating coordination.

<!--
This is the complete arc. Session 1: structure prompts. Session 2: phase your work. Session 3: let the copilot coordinate. The underlying theme: task decomposition. Break big things into focused pieces. The better you get at this, the more effectively you work with AI.
-->

---

# What You Can Do Now

After this course, you can:

- Write G/R/S/O prompts that enable AI exploration
- Phase work between exploration and execution
- Review AI designs instead of debugging AI code
- Let orchestration handle coordination
- Focus on decisions, not details

<!--
This is what the course has equipped you to do. You've gone from "tell the AI what to do" to "give the AI goals and let it coordinate." That's the progression of skill.
-->

---

# Questions?

```
Golden rule: focus beats breadth.
All three sessions: task decomposition at increasing levels.
Core Triad: Orchestrator + Architect + Analysis (the decision-making unit)
```

Remember:
- Architect generates designs and plans
- Analysis critiques and verifies
- The triad cycles until agreement
- Implementer executes the agreed plan (after the triad)
- Sub-agent = copilot replacing you in the human→copilot relationship

<!--
Any questions? The core message: focus beats breadth, task decomposition at increasing levels, Core Triad makes verified decisions through generate-critique cycling, Implementer executes after agreement.
-->
