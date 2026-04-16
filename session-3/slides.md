---
marp: true
theme: default
paginate: true
---

# Orchestrating Complex Work

How Sub-Agents Coordinate to Solve Big Problems

<!--
Welcome back. You've learned about prompting in Session 1 and the two modes of working in Session 2. Today we're going to understand something that ties it all together — and by the end, you'll see that everything we've covered has been building toward one simple idea.
-->

---

# Recap from Session 2

| Mode | Character | Output |
|------|-----------|--------|
| **G/R/S/O (Generative)** | Exploration, agency | Design + Plan |
| **Literal (Enumerative)** | Execution, clarity | Working code |

- Documents bridge the modes
- Linear flow: explore → document → execute

<!--
Quick recap. G/R/S/O enables exploration and decision-making. Literal instructions enable execution. Documents — the design and plan — bridge them. This was a linear flow: think, then do. Today we're going to see why this matters at a larger scale.
-->

---

# The Golden Rule

> **The more focused, more specific, and with fewer additional responsibilities, the better the AI performs.**

This applies to every AI interaction — prompts, modes, sub-agents, everything.

<!--
Let me start with the most important principle in all of AI collaboration. The more focused, more specific, and with fewer additional responsibilities, the better the AI performs. You've probably already experienced this. A specific request gets better results than a vague one. This isn't just a tip — it's the foundation of everything we're learning.
-->

---

# Focus Beats Breadth

| Request Type | What Happens |
|--------------|--------------|
| "Build me a web app with user accounts, email, payments, and reporting" | AI juggles too many concerns at once |
| "Design the user account system. Just the account system." | AI focuses deeply on one thing |

**The same AI performs differently based on how focused the task is.**

<!--
Compare these two requests. The first asks the AI to think about five things simultaneously — accounts, email, payments, reporting, and how they connect. The second asks about one thing. The same AI will perform better on the focused task. Not because it can't handle complexity — but because focus enables depth.
-->

---

# The Tension

Complex work requires:
- Multiple considerations
- Different phases
- Various kinds of thinking

But AI performs best with:
- Single focus
- Clear boundaries
- Specific deliverable

**How do you handle complex work with a tool that performs best on focused work?**

<!--
This creates a tension. Real projects involve many considerations — research, design, implementation, testing. But we just said AI performs best with focused tasks. How do you reconcile this? How do you handle complex work with a tool that performs best on simple work? This tension is the core problem Session 3 solves.
-->

---

# The Answer: Break It Down

The solution to this tension has a name: **task decomposition**.

Break complex work into focused pieces, each handled with full attention.

**And here's the insight: you've already been doing this.**

<!--
The answer is task decomposition. Break complex work into focused pieces. Each piece gets full attention. The golden rule is satisfied for each piece. But here's what you might not have noticed: you've already been doing this. Let me show you.
-->

---

# Session 1 Was Task Decomposition

**At the prompt level:**

| Before (Vague) | After (Decomposed into G/R/S/O) |
|----------------|--------------------------------|
| "Help me with this" | **Goal:** What success looks like |
| | **Rules:** Hard constraints |
| | **Strategies:** Soft preferences |
| | **Opening:** How to begin |

One vague request → Four focused components.

<!--
In Session 1, you learned G/R/S/O. What was that really? It was task decomposition at the prompt level. Instead of one vague request, you decompose your intent into four focused parts — goal, rules, strategies, opening. Each part is specific. The AI handles each with clarity.
-->

---

# Session 2 Was Task Decomposition

**At the workflow level:**

| Before (Monolithic) | After (Decomposed into Phases) |
|---------------------|-------------------------------|
| "Build the login system" | **Phase 1:** Explore options (G/R/S/O) |
| | **Phase 2:** Document the design |
| | **Phase 3:** Execute the plan (Literal) |

One monolithic task → Exploration phase + Execution phase.

Documents bridged the phases.

<!--
In Session 2, you learned the two modes — generative and enumerative. What was that really? Task decomposition at the workflow level. Instead of one monolithic "build this" task, you decomposed into an exploration phase and an execution phase. Documents bridged them.
-->

---

# Session 3 Is Task Decomposition

**At the coordination level:**

| Session | Decomposition Level | What Gets Decomposed |
|---------|--------------------|-----------------------|
| Session 1 | Prompt | Vague request → G/R/S/O structure |
| Session 2 | Workflow | Monolithic work → Explore + Execute |
| **Session 3** | **Coordination** | **Your coordination → Copilot's coordination** |

**The entire course is about task decomposition at increasing levels.**

<!--
Session 3 is task decomposition at the coordination level. In Session 2, YOU coordinated the phases — you decided when to move from exploration to execution. Session 3 is about letting the copilot do that coordination. The entire course has been about task decomposition at increasing levels. Today we complete the pattern.
-->

---

# Decomposition Creates Multiple Context Windows

When you decompose work:
- Each focused piece needs its own conversation
- Each conversation has its own context window
- Information must flow BETWEEN these contexts

```
Task 1: Research    Task 2: Design    Task 3: Implement
   ↓                    ↓                  ↓
Context A           Context B          Context C
   └───────────────────┴──────────────────┘
              Information must flow
```

<!--
Here's what task decomposition creates. When you break work into focused pieces, each piece needs its own context — its own conversation. But these pieces aren't independent. The research informs the design. The design guides the implementation. Information has to flow between these separate contexts.
-->

---

# Remember Context Poisoning?

From Session 1: The balloon animals problem.

| Phase | What Gets Generated | What You Actually Need |
|-------|--------------------|-----------------------|
| Research | Notes, articles, comparisons | → The findings document |
| Design exploration | Alternatives, discussions | → The final design |
| Review cycles | Back-and-forth critique | → The verified artifact |

**Old context becomes noise** — but now multiply this across multiple contexts.

<!--
Remember context poisoning from Session 1? The balloon animals problem? Each phase generates context that becomes irrelevant once the phase completes. You don't need the research notes — you need the findings. You don't need the design exploration — you need the final design. Now multiply this problem across multiple contexts, each one potentially poisoning the next.
-->

---

# The Context Engineering Challenge

When you decompose tasks, you need to manage:

| Challenge | What It Means |
|-----------|---------------|
| **Context isolation** | Each task sees only what it needs |
| **Context handoffs** | Results flow between tasks cleanly |
| **Context coherence** | All tasks work toward the same goal |
| **Context freshness** | No stale information from old phases |

**This is the context engineering challenge of orchestration.**

<!--
This is the context engineering challenge. Each task needs to see only what's relevant — that's isolation. Results need to flow cleanly between tasks — that's handoffs. All tasks need to work toward the same goal — that's coherence. And no task should be confused by old, stale information — that's freshness. Managing all of this is context engineering. And it's why orchestration exists.
-->

---

# Orchestration Manages Context

**Orchestration** = Coordinating decomposed tasks while managing their contexts.

The Orchestrator:
- Breaks complex goals into focused sub-agents
- Gives each sub-agent exactly the context it needs
- Passes results (not working noise) between tasks
- Maintains the big picture while sub-agents focus narrowly

<!--
Orchestration is the solution to the context engineering challenge. An Orchestrator breaks complex goals into focused sub-agents. It gives each sub-agent exactly the context it needs — no more, no less. It passes results between tasks — the deliverables, not all the working noise. And it maintains the big picture so each sub-agent can focus narrowly.
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
Remember how documents bridge the exploration and execution modes in Session 2? In orchestration, documents play the same role between sub-agents. The research sub-agent produces a findings document. That document — not all the research noise — becomes context for the design sub-agent. Clean handoffs. Filtered context.
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
Here's the progression. Before AI, you did everything. In Session 1, the copilot started doing work. In Session 2, you learned to coordinate multiple phases. Now in Session 3, the copilot takes over coordination too. Improvement with AI copilots means progressively replacing what you're doing with what the copilot can do.
-->

---

# The Human→Copilot Relationship

When you work with a coding copilot, there's a relationship:

```
┌─────────────────────────────────────────────────┐
│                                                 │
│   Human ────────────► Coding Copilot            │
│          types message                          │
│                                                 │
└─────────────────────────────────────────────────┘
```

You type a message. The copilot responds. That's the fundamental interaction.

<!--
Now let's understand exactly how orchestration works. Start with the basic relationship. You type a message to the copilot. The copilot responds. That's the fundamental interaction. You're on one side, the copilot is on the other.
-->

---

# The Copilot Can Take Your Role

Here's the key insight:

**The copilot can do what you do — type a message to a copilot.**

```
┌─────────────────────────────────────────────────┐
│                                                 │
│   Human ──────► Orchestrator Copilot            │
│                        │                        │
│                        ▼ types message          │
│                 Sub-Agent Copilot               │
│                                                 │
└─────────────────────────────────────────────────┘
```

<!--
Here's the fundamental insight. What do you do when you work with a copilot? You type a message. What can the copilot do? Type a message. So the copilot can take YOUR role in that relationship. You talk to an Orchestrator Copilot. The Orchestrator Copilot talks to a Sub-Agent Copilot. It's the same interaction — just with the copilot playing your role.
-->

---

# Before: You Coordinate Everything

```
┌─────────────────────────────────────────────────┐
│                                                 │
│   Human ────────────► Coding Copilot            │
│          types message                          │
│                                                 │
│   You decide what to do next.                   │
│   You manage context between tasks.             │
│   You coordinate the workflow.                  │
│                                                 │
└─────────────────────────────────────────────────┘
```

<!--
This is where you started. You type messages. You decide what to do next. You manage context. You coordinate everything. The copilot helps, but YOU are doing the coordination work.
-->

---

# After: Orchestrator Coordinates for You

A **sub-agent** is what happens when the copilot takes the human's role:

*(You may also hear these called "subtasks" — same concept.)*

```
┌─────────────────────────────────────────────────┐
│                                                 │
│    Human ──────► Orchestrator ──────► Sub-Agent │
│      │               │                    │     │
│   approves       types message        responds  │
│  decisions      (like you did)                  │
│                                                 │
│   You approve. Orchestrator coordinates.        │
│                                                 │
└─────────────────────────────────────────────────┘
```

<!--
After: The Orchestrator takes YOUR role — typing messages, deciding what's next, managing context. The sub-agent takes the copilot's role — doing focused work. You move up a level. You approve decisions instead of making every one yourself.

This isn't a metaphor. The Orchestrator literally types messages to sub-agents.

**Important:** This pattern — the copilot talking to itself in a structured way — works with any AI coding assistant. Sub-agents aren't a feature of one specific tool. They're a pattern that any copilot can implement. Kahuna is one implementation for Claude Code, but the concept is universal.
-->

---

# Why Fresh Conversations?

Each sub-agent gets a **fresh conversation**:

| Same Conversation | Fresh Sub-Agent Conversation |
|-------------------|------------------------------|
| All accumulated context | Only the context it needs |
| May include irrelevant tangents | Focused on one task |
| Growing complexity | Clean slate |

**Key insight:** The Orchestrator chooses what context to include.

This is how context engineering happens — the Orchestrator curates context for each sub-agent.

<!--
Why does each sub-agent get a fresh conversation? Remember the context engineering challenge? A fresh conversation means the sub-agent sees only what the Orchestrator chooses to include. No accumulated noise. No irrelevant tangents. Just the context needed for that specific task. The Orchestrator is doing context engineering — curating what each sub-agent sees.
-->

---

# Sub-Agents Are Defined by Deliverables

| Sub-Agent Type | Deliverable |
|---------------|-------------|
| Research | Report with findings and citations |
| Design | Design document |
| Planning | Implementation plan with phases |
| Review | Assessment with findings |
| Implementation | Working, tested code |

**Key principle:** Sub-agents are defined by their **output**, not their activity.

<!--
Now let's get specific about how orchestration works. Sub-agents are defined by what they produce, not by what they do. A research sub-agent produces a findings report. A design sub-agent produces a design document. This output focus keeps the work concrete and verifiable.
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
│  │ Research │   │  Design  │   │  Review  │     │
│  │ sub-agent│   │ sub-agent│   │ sub-agent│     │
│  └────┬─────┘   └────┬─────┘   └────┬─────┘     │
│       │              │              │           │
│       ▼              ▼              ▼           │
│    Findings       Design        Assessment      │
│     Report       Document                       │
└──────────────────────────────────────────────────┘
```

Each sub-agent sees only what it needs. No cross-contamination.

<!--
This is context isolation in action. Each sub-agent gets only the context relevant to its task. The research sub-agent doesn't see the review discussions. The implementation sub-agent doesn't see the abandoned design alternatives. The Orchestrator passes along only what's needed — typically the deliverables from prior phases, not all the work that produced them.
-->

---

# The Core Triad

Three roles form the cognitive decision-making unit:

| Role | Function | When to Use |
|------|----------|-------------|
| **Orchestrator** | Coordinates sub-agents | Complex, multi-phase work |
| **Architect** | Creates plans and designs | "What should we build?" |
| **Implementer** | Executes plans as code | "Build it according to plan" |

Different copilots may name these differently — Kahuna uses these names in Claude Code.

<!--
These three roles appear in various forms across AI systems. The names might differ — "Architect" might be called "Designer" or "Planner," "Implementer" might be "Code" or "Builder." The pattern is what matters: coordination, creation, and execution.

Kahuna uses Orchestrator, Architect, and Implementer. The next slide shows exactly how this looks in Claude Code.
-->

---

# Kahuna: The Triad in Claude Code

In Claude Code, Kahuna implements the triad like this:

```
.claude/
├── CLAUDE.md            ← Orchestrator (you talk to this)
└── agents/
    ├── architect.md     ← Architect sub-agent
    └── implementer.md   ← Implementer sub-agent
```

**You always talk to the Orchestrator.** It coordinates the sub-agents.

<!--
This is how Kahuna structures the triad for Claude Code. The CLAUDE.md file IS the Orchestrator — it's what you actually talk to. It has access to sub-agents defined in the agents/ folder.

When you give it a complex task, the Orchestrator:
1. Breaks it into focused pieces
2. Delegates to the appropriate sub-agent (Architect for design, Implementer for code)
3. Manages context between them
4. Synthesizes results

The Orchestrator is "the conductor, not the performer."
-->

---

# Orchestrator — The Coordinator

**What it does:**

- Breaks complex goals into sub-agent tasks
- Assigns the right mode to each task
- Writes focused prompts for each sub-agent
- Synthesizes results

**Trigger:** "This is too complex for one conversation"

<!--
The Orchestrator is the coordinator. When you have a complex goal that involves multiple phases or needs different kinds of thinking, the Orchestrator breaks it down. It assigns the right mode to each piece and writes the prompts that give each sub-agent exactly the context it needs.
-->

---

# Architect — The Creator

**What it does:**

- Explores options and makes decisions
- Produces designs and plans
- Defines success criteria

**Trigger:** "What should we build? How should we approach this?"

**Example outputs:** Design documents, implementation plans, technical decisions

<!--
The Architect creates. When you need to figure out what to build or how to approach a problem, Architect mode explores options, makes decisions, and produces the documents that capture those decisions.

Remember G/R/S/O from Session 1? That's the prompt structure. Architect mode *emphasizes* exploration and planning — it's where G/R/S/O prompts are most useful. By contrast, Implementer mode emphasizes execution — less exploration, more following the plan.

G/R/S/O = how you structure prompts (Session 1)
Architect = a role that emphasizes exploration (uses G/R/S/O heavily)
Implementer = a role that emphasizes execution (uses G/R/S/O less)
-->

---

# Implementer — The Executor

**What it does:**

- Executes plans as working code
- Follows designs precisely
- Handles implementation details

**Trigger:** "Build it according to the plan"

**Example outputs:** Working code, tests, documentation

<!--
The Implementer executes. When you have a plan and need it built, Implementer mode follows the design precisely and handles all the implementation details. It emphasizes execution over exploration — less G/R/S/O exploration, more focused building.
-->

---

# Why the Triad Works

| Without Orchestrator | Without Architect | Without Implementer |
|---------------------|-------------------|---------------------|
| Can't coordinate complexity | Can't create new designs | Can't execute plans |
| Context accumulates | No forward momentum | Ideas stay abstract |
| Manual tracking burden | Just executing old ideas | Nothing gets built |

**All three are necessary.** Orchestrator enables Architect and Implementer to work together without coordination overhead.

<!--
Why do we need all three? Without the Orchestrator, you can't handle complexity — context accumulates and you lose track. Without the Architect, nothing new gets created. Without the Implementer, designs never become working code. The Orchestrator enables Architect and Implementer to work together effectively.

Note: Some copilots also have Analysis/Review modes for critiquing work — these are additional specialized modes beyond the core triad.
-->

---

# The Generate-Critique Cycle

Remember Session 2's "inhaling and exhaling"?

```
┌──────────────────────────────────────────────┐
│                                              │
│    Architect ──────► Analysis                │
│        ▲                 │                   │
│        │     critique    │                   │
│        └─────────────────┘                   │
│                                              │
│    Generate → Critique → Revise → Verify     │
│                                              │
└──────────────────────────────────────────────┘
```

<!--
Remember how we described generating and executing as "inhaling and exhaling" — complementary but not simultaneous? The generate-critique cycle is how iteration happens. You generate something, critique it, revise based on the critique, then verify the revision.
-->

---

# How the Cycle Works

1. **Architect** produces design/plan with success criteria
2. **Analysis** reviews against criteria, finds problems
3. If issues found → **Architect** incorporates critique, revises
4. **Analysis** verifies revision meets criteria
5. Proceed to implementation (or next phase)

**Key insight:** Neither generating alone (uncritical) nor critiquing alone (paralysis) produces quality. **Cycling between them does.**

<!--
Here's how the cycle works step by step. Architect produces a design with explicit success criteria. Analysis reviews against those criteria and finds problems. If there are issues, Architect incorporates the critique and revises. Analysis verifies the revision. Then you proceed. Neither mode alone is sufficient — you need the cycle.
-->

---

# Why This Improves Quality

| Just Generating | Just Critiquing | The Cycle |
|-----------------|-----------------|-----------|
| Produces something | Produces nothing | Produces something good |
| No quality check | No forward motion | Quality through iteration |
| "Ship it and see" | "Analysis paralysis" | Confident progress |

**The cycle captures both momentum and quality.**

<!--
Why does the cycle improve quality? Just generating produces something but no quality check. Just critiquing produces nothing. The cycle gives you both: forward momentum AND quality verification. You ship with confidence.
-->

---

# When to Use the Cycle

| Use the Cycle | Skip the Cycle |
|---------------|----------------|
| Important decisions | Quick fixes |
| Complex designs | Well-understood tasks |
| High-stakes work | Time-constrained work |
| Unfamiliar territory | Routine patterns |

**Heuristic:** If you'd regret getting it wrong, use the cycle.

<!--
When should you use the cycle versus skip it? Use it for important work — complex designs, high stakes, unfamiliar territory. Skip it for quick fixes and routine patterns. The heuristic: if you'd regret getting it wrong, use the cycle.
-->

---

# Task Decomposition in Practice

Complex tasks require decomposition:

```
Big Goal
    │
    ├── Sub-agent 1: Research options
    │       └── Deliverable: Findings report
    │
    ├── Sub-agent 2: Design approach
    │       └── Deliverable: Design document
    │
    ├── Sub-agent 3: Review design
    │       └── Deliverable: Assessment
    │
    └── Sub-agent 4: Implement
            └── Deliverable: Working code
```

<!--
Task decomposition is how you break a big goal into sub-agent tasks. Each sub-agent has a specific focus and produces a specific deliverable. The Orchestrator manages the flow from one to the next.
-->

---

# Abstract to Concrete

Work progresses from abstract to concrete:

| Phase | What Happens | Example |
|-------|--------------|---------|
| 1. Foundation | Understand the domain | "What tools exist?" |
| 2. Exploration | Research options | "What are our choices?" |
| 3. Decision | Design/select approach | "Here's what we'll do" |
| 4. Verification | Analyze the design | "Is this sound?" |
| 5. Planning | Create implementation plan | "Here are the steps" |
| 6. Execution | Implement phase by phase | "Build it" |

<!--
There's a natural progression. You start abstract — understanding the domain, researching options. Then you make decisions — choosing an approach. Then you verify — is this approach sound? Then you plan and execute. Each phase gets more concrete.
-->

---

# Choosing the Right Mode

The specificity spectrum:

| Mode Type | Trigger | Examples |
|-----------|---------|----------|
| **Specific** (narrow) | Clear, well-defined task | Research, Debug, Code |
| **Versatile** (broad) | Abstract thinking, judgment | Architect, Analysis |

**Selection question:** Is the trigger clear and narrow (specific mode) or does it require judgment (versatile mode)?

<!--
How do you choose which mode for each sub-agent? Think about specificity. Some modes have narrow triggers — Research is for gathering information, Debug is for finding bugs, Code is for implementing. Others are versatile — Architect handles any design or planning work, Analysis handles any critique or verification. Check specific modes first; fall back to versatile modes.
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
The core roles — Architect and Implementer — handle most work. Specialized modes like Research, Analysis, and Debug exist in some copilots for specific tasks. If your copilot doesn't have a specialized mode, the Architect can often handle research and analysis as part of its exploration work.
-->

---

# Writing Sub-Agent Prompts

A good sub-agent prompt includes:

1. **Context:** What the sub-agent needs to know
2. **Task:** What specifically to do
3. **Deliverable:** What to produce
4. **Success criteria:** How to know it's done

<!--
When writing a sub-agent prompt — or when the Orchestrator writes one — it needs four things. Context: what does this sub-agent need to know? Task: what specifically should it do? Deliverable: what should it produce? Success criteria: how will we know it's done?
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
Here's what a sub-agent prompt looks like in practice. Notice the structure: context gives background, task says what to do, deliverable says what to produce, and success criteria tell us how to verify quality. This structure enables focus.
-->

---

# Kahuna: Sub-Agents in Action

When you give Kahuna a complex task, the Orchestrator:

1. **Breaks it down** into focused sub-agent tasks
2. **Selects the right role** for each (Architect or Implementer)
3. **Manages context** between sub-agents
4. **Synthesizes results** into a coherent whole

You see the results; Kahuna handles the coordination.

<!--
This is how Kahuna works under the hood. When you give it a complex task, the Orchestrator breaks it down into sub-agents. It selects the right role for each — Architect for design work, Implementer for code — writes the prompts, and manages the context. You see the results; Kahuna handles the coordination.
-->

---

# Your Role — Approval Gates

The human stays at strategic decision points:

| What Orchestrator Does | What You Do |
|------------------------|-------------|
| Breaks down the work | Approve the decomposition |
| Assigns modes | Verify the assignments make sense |
| Manages sub-agents | Review sub-agent outputs |
| Synthesizes results | Make final decisions |

**You don't coordinate. You decide.**

<!--
What's your role in all this? You stay at the strategic level. The Orchestrator proposes how to break down the work — you approve it. It assigns modes — you verify that makes sense. It manages sub-agents — you review what they produce. You don't do the coordination. You make the decisions.
-->

---

# Session 3 Cheat Sheet

| Concept | One-Liner |
|---------|-----------|
| **Golden Rule** | More focus = better AI performance |
| **Task Decomposition** | Break complex work into focused pieces |
| **Context Engineering** | Managing what each piece sees |
| **Orchestration** | Copilot coordinates decomposed tasks |
| **Sub-agent** | Copilot takes your role (types message to copilot) |
| **Core Triad** | Orchestrator + Architect + Implementer |

<!--
Here's your cheat sheet. The golden rule: focus improves performance. Task decomposition: break complex into focused. Context engineering: manage what each piece sees. Orchestration: copilot coordinates. Sub-agents: copilot takes your role. Core Triad: Orchestrator, Architect, Implementer.
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
This is the complete arc. Session 1 taught you how to structure individual prompts. Session 2 taught you how to phase your work between exploration and execution. Session 3 taught you how to let the copilot handle that coordination for you.

The underlying theme: task decomposition. Break big things into focused pieces. The better you get at this, the more effectively you work with AI.
-->

---

# Questions?

```
Golden rule: focus beats breadth.
All three sessions: task decomposition at increasing levels.
Orchestration: copilot coordinates so you decide.
```

Remember:
- Architect mode emphasizes exploration (uses G/R/S/O heavily)
- Implementer mode emphasizes execution
- Documents handoff between sub-agents
- Sub-agent = copilot replacing you in the human→copilot relationship

<!--
Any questions before we wrap up? The core message: focus beats breadth, all three sessions have been about task decomposition at increasing levels, and orchestration means the copilot coordinates so you can focus on decisions.
-->
