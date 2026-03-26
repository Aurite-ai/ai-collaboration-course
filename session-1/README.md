# Session 1: Effective Prompting

A practical guide to getting better results from AI coding assistants.

---

## What You'll Learn

By the end of this session, you'll understand:

1. **What an LLM actually is** — It's a text equation. Text in, text out.
2. **Why "everything is text" matters** — System prompts, files, tools — all just text in the input
3. **Context poisoning** — Why irrelevant content hurts output quality
4. **Two types of prompts:**
   - **Literal Instructions** — Step-by-step enumeration for simple tasks
   - **Decision-Making (G/R/S/O)** — Goal/Rules/Strategies/Opening for complex tasks

---

## Materials

### 📊 Slides

[`slides.md`](slides.md)

These slides are in Marp format. You can:
- Read the markdown directly (the content is all there)
- Use the Marp VS Code extension to view as slides

Speaker notes are in `<!-- comment -->` blocks — they contain additional explanations.

---

## Key Concepts

### The Core Equation

```
INPUT (text) ──────► LLM ──────► OUTPUT (text)
```

One word at a time. The entire conversation re-read for every word generated.

### Context Poisoning

Imagine watching a 30-minute Python tutorial, but you can only watch 1 minute at a time before starting over. That irrelevant 2-minute tangent about balloon animals? You watch it 29 times.

LLMs don't have selective attention. Everything gets processed, every time.

### G/R/S/O Framework

For tasks where the AI needs to make decisions:

| Component | What It Does |
|-----------|--------------|
| **Goal** | What success looks like |
| **Rules** | Hard constraints (must/must not) |
| **Strategies** | Soft preferences (prefer/avoid) |
| **Opening** | How to begin |

---

## Assignments

Session 1 has no assignments — it's the conceptual foundation. Hands-on practice starts in Session 2.

---

## Before Session 2

Make sure you have:
- [ ] An AI coding tool installed (Kahuna recommended)
- [ ] Python and pandas available (for assignments)
- [ ] Reviewed the G/R/S/O framework

---

*Session 1 — AI Collaboration Course*
