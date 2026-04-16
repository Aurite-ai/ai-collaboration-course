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

*(You may also hear these called "subtasks" or "modes" —same concept.)*

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
│  ┌──────────┐   ┌──────────┐   ┌──────────┐      │
│  │ Research │   │  Design  │   │ Implement│      │
│  │ sub-agent│   │ sub-agent│   │ sub-agent│      │
│  └────┬─────┘   └────┬─────┘   └────┬─────┘      │
│       ▼              ▼              ▼            │
│    Findings       Design         Working         │
│     Report       Document          Code          │
└──────────────────────────────────────────────────┘
```

Each sub-agent sees only what it needs. No cross-contamination.

<!--
Each sub-agent gets only the context relevant to its task. The research sub-agent doesn't see abandoned design alternatives. The Orchestrator passes along only what's needed—deliverables from prior phases, not all the work that produced them.
-->

---

# The Golden Rule

> **The more focused, more specific, and with fewer additional responsibilities, the better the AI performs.**

This applies to every AI interaction—prompts, sub-agents, skills, everything.

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

# Meet the Orchestrator

| What It Is | What It Does |
|------------|--------------|
| A specialized Copilot | Coordinates sub-copilots (called sub-agents) |
| Your single point of contact | Breaks your request into focused tasks |
| The coordinator, not the doer | Delegates to Architect, Implementer, etc. |

**Think of it as:** A project manager for your AI workflow.

The Orchestrator maintains the big picture while sub-agents handle the details.

<!--
Remember Session 2? You coordinated the flow: exploration, then design review, then execution. The Orchestrator does that coordination FOR you. It's still Copilot talking to Copilot — the Orchestrator is a Copilot instance that takes YOUR coordination role.

The Orchestrator doesn't do the work itself. It breaks down your request and delegates to focused sub-agents. This is the Copilot takes your role concept in action — at the coordination level.

Next we'll see how you actually interact with it.
-->

---

# You Always Talk to the Orchestrator

```
┌─────────────────────────────────────────────────┐
│                                                 │
│   You ──────────► Orchestrator                  │
│        prompt           │                       │
│                         │ handles everything    │
│                         ▼                       │
│                    Sub-Agents                   │
│                                                 │
└─────────────────────────────────────────────────┘
```

**Key point:** You don't write sub-agent prompts. The Orchestrator does.

Your job: Write effective prompts **to** the Orchestrator.

<!--
Here's the crucial insight: you always talk to the Orchestrator. You don't write prompts for sub-agents directly — the Orchestrator handles that. Your job is simpler: write effective prompts to the Orchestrator, and let it coordinate the sub-agents for you.
-->

---

# The Linear Orchestration Flow

```
┌──────────────────────────────────────────────────────────────┐
│                                                              │
│   Your Prompt ──► Orchestrator                               │
│                        │                                     │
│                        ▼                                     │
│              ┌─────────────────┐                             │
│              │    Architect    │  ◄── Planning sub-agent     │
│              │  produces plan  │                             │
│              └────────┬────────┘                             │
│                       │                                      │
│                       ▼                                      │
│              ┌─────────────────┐                             │
│              │   Implementer   │  ◄── Execution sub-agent    │
│              │  produces code  │                             │
│              └────────┬────────┘                             │
│                       │                                      │
│                       ▼                                      │
│              ┌─────────────────┐                             │
│              │  Verification   │  ◄── Optional check         │
│              │  confirms work  │                             │
│              └─────────────────┘                             │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

<!--
This is the linear orchestration flow. You prompt the Orchestrator. It delegates to Architect for planning, then to Implementer for code, then optionally to Verification to check the work. Each phase produces something concrete before moving to the next.
-->

---

# Architect: Plan Before You Build

| Architect Sub-Agent | Details |
|---------------------|---------|
| **Purpose** | Creates designs and plans before any code is written |
| **Produces** | Design documents, implementation plans, architecture decisions |
| **When used** | Always first — before any implementation |

**Why plan first?**
- Catches problems early (cheaper to fix a plan than code)
- Creates shared understanding
- Enables better implementation (Implementer knows what to build)

<!--
The Architect sub-agent handles all planning work. It produces designs and implementation plans before any code is written. Why plan first? Problems caught in a plan are much cheaper to fix than problems caught in code. The plan also gives the Implementer clarity about what to build.
-->

---

# Implementer: Execute the Plan

| Implementer Sub-Agent | Details |
|-----------------------|---------|
| **Purpose** | Writes code based on the plan |
| **Receives** | Design document or implementation plan from Architect |
| **Produces** | Working, tested code |

**Key principle:** Implementer follows the plan — it doesn't redesign.

```
Architect's Plan ──► Implementer ──► Working Code
                         │
                         └── Follows plan precisely
```

<!--
The Implementer sub-agent writes the actual code. It receives the plan from the Architect and executes it. The key principle: Implementer follows the plan. It doesn't redesign — that would undo the Architect's work. This separation keeps each sub-agent focused.
-->

---

# Verification: Check the Work

| Verification | Details |
|--------------|---------|
| **Purpose** | Confirms the implementation matches the plan |
| **When used** | Optionally, after implementation |
| **Produces** | Confirmation or list of issues |

**Not always needed:**
- Simple tasks may skip verification
- Complex or high-stakes work benefits from it
- The Orchestrator decides based on context

<!--
Verification is optional. It checks that the implementation matches the plan. Not every task needs it — simple work can skip verification. But for complex or high-stakes work, having a verification step catches problems before you move on. The Orchestrator decides whether to include it.
-->

---

# Skills: Sub-Agents with Shared Context

| Regular Sub-Agent | Skill |
|-------------------|-------|
| Fresh conversation | Same conversation continues |
| Orchestrator passes context explicitly | Context already available |
| Full isolation | Shared memory |

**Skills are like sub-agents, but they keep the same context window.**

The Orchestrator loads different rules/instructions without starting a new conversation.

**Example:** Verification can run as a skill — it sees everything that happened without needing a handoff document.

<!--
Quick concept: Skills. They're like sub-agents but keep the same context window. Instead of starting a fresh conversation, the Orchestrator just loads different rules. This is useful when the sub-agent needs to see everything that happened — like Verification reviewing the implementation without needing explicit handoffs.
-->

---

# Orchestrator Usage

**The question:** How do you prompt the Orchestrator?

You're not telling it what to code. You're telling it what to **coordinate**.

**The answer:** More G/R/S/O!

Same structure. Same elements. Higher level of abstraction.

<!--
Here's the natural question: how do you actually prompt the Orchestrator? It feels different because you're not asking for code — you're asking for coordination. But the answer is familiar: more G/R/S/O! The same structure you already know, just applied to coordination instead of implementation. Let's break that down.
-->

---

# G/R/S/O at the Orchestrator Level

**Remember Session 1?** You learned G/R/S/O for structuring prompts:

| Element | What It Does | At Orchestrator Level |
|---------|--------------|----------------------|
| **Goal** | What success looks like | What the coordinated work should achieve |
| **Rules** | Hard constraints | Boundaries on how work is decomposed |
| **Strategies** | Suggested approaches | How to phase or structure the work |
| **Opening** | Current state and context | What exists, what's available |

**Same structure.** You're just describing work to be coordinated, not code to be written.

<!--
Same G/R/S/O elements, but applied at a coordination level. Goal: what the overall work should achieve. Rules: constraints on how work can be broken down. Strategies: suggested phasing or approaches. Opening: current system state. Let's see what this looks like in practice.
-->

---

# Example: G/R/S/O for the Orchestrator

```markdown
## Goal (G)
Add a password reset feature to the user authentication system.

## Rules (R)
- Reset tokens must expire in 1 hour
- Must work with existing user table schema
- No new dependencies if possible

## Strategies (S)
- Reuse the existing email service (SendGrid)
- Follow the same pattern as email verification

## Opening (O)
- Using Express.js with PostgreSQL
- Email service already configured
- Current auth uses JWT tokens
```

**Same structure as Session 1 — now at coordination level.**

<!--
Look familiar? This is the same G/R/S/O structure from Session 1, but now you're prompting the Orchestrator, not writing code. Goal: what to achieve. Rules: hard constraints. Strategies: suggested approaches. Opening: current state. Same pattern, higher abstraction.
-->

---

# It's G/R/S/O All the Way Down

Now here's the insight: YOUR G/R/S/O prompt cascades through the system.

```
You ──G/R/S/O──► Orchestrator
                      │
                      └──G/R/S/O──► Architect
                                        │
                                        └──G/R/S/O──► Design + Plan
                                                           │
                                                           └──Literal──► Implementer
                                                                              │
                                                                              ▼
                                                                        Working Code
```

**Each level uses G/R/S/O until you reach implementation, where it becomes literal execution.**

<!--
Here's what makes this powerful: G/R/S/O cascades through the entire chain. Your prompt guides the Orchestrator. The Orchestrator prompts the Architect with G/R/S/O. The Architect produces a design using G/R/S/O thinking. Then the Implementer receives literal instructions — the plan itself. That's where the cascade ends.
-->

---

# Where G/R/S/O Stops

| Level | Who | Uses | Produces |
|-------|-----|------|----------|
| 1 | **You** | G/R/S/O | Orchestrator prompt |
| 2 | **Orchestrator** | G/R/S/O | Architect prompt |
| 3 | **Architect** | G/R/S/O | Design + Implementation Plan |
| 4 | **Implementer** | Literal | Working code |

**The plan is the terminal.** The Architect's plan becomes literal instructions for the Implementer.

G/R/S/O enables exploration (brainstorming and decision-making). When exploration is done, literal execution takes over.

<!--
Notice where G/R/S/O stops. The Implementer doesn't get a G/R/S/O prompt — it gets a plan. The plan is literal: do this, then this, then this. That's the boundary between exploration and execution. The Architect explores; the Implementer executes.
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
| **G/R/S/O Cascade** | G/R/S/O at every level until implementation |
| **Sub-agent** | Copilot takes your role — types message to copilot |
| **Task Decomposition** | Break complex work into focused pieces |
| **Context Engineering** | Managing what each piece sees |
| **Orchestration** | Copilot coordinates decomposed tasks |
| **Linear Flow** | Orchestrator → Architect → Implementer → Verification |
| **Terminal** | Where G/R/S/O ends and literal execution begins |

<!--
Your cheat sheet. Golden rule: focus improves performance. G/R/S/O cascade: same structure at every level until implementation. Sub-agents: copilot takes your role. Task decomposition: break complex into focused. Context engineering: manage what each piece sees. Orchestration: copilot coordinates. Linear flow: Orchestrator coordinates Architect (plan), Implementer (build), and optional Verification. Terminal: the plan becomes literal instructions.
-->

---

# Putting It All Together

You now have the complete picture:

| Session | What You Learned | Core Skill |
|---------|------------------|------------|
| **Session 1** | G/R/S/O prompts | Structuring your requests |
| **Session 2** | Two modes of working | Exploring vs. executing |
| **Session 3** | G/R/S/O at every level | Letting the copilot coordinate |

**The pattern:** G/R/S/O cascades through orchestration until it becomes literal execution.

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
Linear flow: Orchestrator → Architect → Implementer → Verification
```

Remember:
- You always prompt the Orchestrator
- Architect plans before building
- Implementer follows the plan precisely
- Verification is optional but valuable for complex work
- Sub-agent = copilot replacing you in the human→copilot relationship

<!--
Any questions? The core message: focus beats breadth, task decomposition at increasing levels. The linear flow: you prompt the Orchestrator, which coordinates Architect (plan), Implementer (build), and optional Verification (check).
-->
