# Session 3: Orchestrating Complex Work

How sub-agents coordinate to solve big problems.

---

## What You'll Learn

By the end of this session, you'll be able to:

1. **Explain** the golden rule: focus beats breadth
2. **Describe** the G/R/S/O cascade from you → Orchestrator → Architect → plan → Implementer
3. **Understand** the linear orchestration flow: Orchestrator → Architect → Implementer → Verification
4. **Write** effective G/R/S/O prompts to the Orchestrator
5. **Identify** when orchestration is needed vs. when a single conversation suffices

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
| [Orchestrator Prompt](assignments/README.md) | Writing G/R/S/O prompts to the Orchestrator | ✅ Available |

**Recommendation:** Complete the assignment before Session 4.

---

## Key Concepts

| Concept | Definition |
|---------|------------|
| **Golden Rule** | The more focused, specific, and fewer responsibilities → the better AI performs |
| **G/R/S/O Cascade** | G/R/S/O at every level until implementation, where it becomes literal |
| **Sub-agent** | Copilot takes your role — types a message to another copilot instance |
| **Orchestrator** | A specialized copilot that coordinates sub-agents |
| **Architect** | Planning sub-agent that produces designs and plans |
| **Implementer** | Execution sub-agent that follows the plan precisely |
| **Verification** | Optional sub-agent that confirms implementation matches plan |
| **Skills** | Sub-agents with shared context (same conversation continues) |
| **Task Decomposition** | Breaking complex work into focused pieces |
| **Context Isolation** | Each sub-agent sees only the context relevant to its task |
| **Terminal** | Where G/R/S/O stops and literal execution begins (the plan) |

---

## The Linear Orchestration Flow

```
You ──G/R/S/O──► Orchestrator
                      │
                      ▼
              ┌─────────────────┐
              │    Architect    │  ◄── produces plan
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │   Implementer   │  ◄── follows plan (literal)
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │  Verification   │  ◄── optional check
              └─────────────────┘
```

**Key insight:** You always talk to the Orchestrator. You don't write sub-agent prompts — the Orchestrator does that for you.

---

## The G/R/S/O Cascade

| Level | Who | Uses | Produces |
|-------|-----|------|----------|
| 1 | **You** | G/R/S/O | Orchestrator prompt |
| 2 | **Orchestrator** | G/R/S/O | Architect prompt |
| 3 | **Architect** | G/R/S/O | Design + Implementation Plan |
| 4 | **Implementer** | Literal | Working code |

The plan is the **terminal** — where G/R/S/O ends and literal execution begins.

---

## Connection to Kahuna

This session explains the orchestration patterns that Kahuna automates. When you give Kahuna a complex task, it:

1. Uses **Orchestrator mode** to coordinate the work
2. Delegates to **Architect mode** for planning
3. Delegates to **Code mode** (Implementer) for execution
4. Optionally runs **Verification** to confirm quality
5. Manages **context isolation** between sub-agents

Understanding these concepts helps you:
- Write better prompts to the Orchestrator
- Know when to intervene vs. let orchestration proceed
- Understand what the Orchestrator will delegate and why

---

## Before Session 4

- [ ] Complete the Orchestrator prompt assignment
- [ ] Practice writing G/R/S/O prompts at the coordination level
- [ ] Notice when tasks could benefit from orchestration

**Coming in Session 4:** Context Engineering at Scale — how to manage context as projects grow.

---

*Session 3 — AI Collaboration Course*
