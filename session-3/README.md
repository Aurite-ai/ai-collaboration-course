# Session 3: Orchestrating Complex Work

How to coordinate multiple AI agents working together on complex tasks.

---

## What You'll Learn

By the end of this session, you'll be able to:

1. **Explain** when orchestration is needed vs. when a single conversation suffices
2. **Identify** the roles of Orchestrator, Architect, and Analysis modes in complex work
3. **Describe** the generate-critique cycle and when to apply it
4. **Decompose** a complex goal into sub-agent tasks with clear deliverables
5. **Select** the appropriate mode for a given sub-agent task

---

## Prerequisites

**From Session 1:**
- G/R/S/O framework for decision-making prompts
- Context poisoning concept (the "balloon animals" problem)

**From Session 2:**
- Two modes: generative (exploration) and enumerative (execution)
- Documents as bridges between modes
- Context engineering basics

---

## Materials

### 📊 Slides

[`slides.md`](slides.md)

These slides are in Marp format. You can:
- Read the markdown directly (the content is all there)
- Use the Marp VS Code extension to view as slides

Speaker notes are in `<!-- comment -->` blocks — they contain additional explanations.

### 📝 Assignments

Practice assignments for this session:

| Assignment | Focus | Status |
|------------|-------|--------|
| [Orchestration Plan](assignments/README.md) | Task decomposition and mode selection | ✅ Available |

**Recommendation:** Complete the assignment before Session 4.

---

## Key Concepts

| Concept | Definition |
|---------|------------|
| **Orchestrator** | Mode that coordinates multi-phase work through sub-agents |
| **Sub-agent** | A focused conversation with specific context and deliverable |
| **Core Triad** | Orchestrator + Architect + Analysis modes working together |
| **Architect** | Mode that creates plans, designs, and decisions |
| **Analysis** | Mode that critiques and verifies artifacts |
| **Generate-Critique Cycle** | Iterative pattern: Architect → Analysis → revise → verify |
| **Task Decomposition** | Breaking a complex goal into sequential sub-agent tasks |
| **Context Isolation** | Each sub-agent sees only the context relevant to its task |
| **Mode Selection** | Choosing which mode to assign to each sub-agent task |

---

## The Core Triad

| Mode | Function | When to Use |
|------|----------|-------------|
| **Orchestrator** | Coordinates sub-agents | Complex, multi-phase work |
| **Architect** | Creates plans and designs | "What should we build?" |
| **Analysis** | Critiques and verifies | "Is this correct?" |

---

## The Generate-Critique Cycle

```
Architect → Analysis → Architect (revise) → Analysis (verify) → proceed
```

Use the cycle when:
- Important decisions are at stake
- Complex designs need validation
- You'd regret getting it wrong

Skip the cycle for:
- Quick fixes
- Well-understood tasks
- Routine patterns

---

## Connection to Kahuna

This session explains the orchestration patterns that Kahuna automates. When you give Kahuna a complex task, it:

1. Uses **Orchestrator mode** to decompose the work
2. Assigns **Architect mode** to design phases
3. Assigns **Analysis mode** to review phases
4. Manages **context isolation** between sub-agents
5. Handles the **generate-critique cycle** automatically

Understanding these concepts helps you:
- Work more effectively with Kahuna
- Know when to intervene vs. let orchestration proceed
- Debug issues when sub-agents produce unexpected results

---

## Before Session 4

- [ ] Complete the orchestration assignment
- [ ] Notice when you're dealing with single-phase vs. multi-phase tasks
- [ ] Practice identifying which mode fits each sub-task

**Coming in Session 4:** Context Engineering at Scale — how to manage context as projects grow.

---

*Session 3 — AI Collaboration Course*
