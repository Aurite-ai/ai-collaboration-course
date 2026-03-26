# Session 2: The Two Modes of Working

How your prompts become working software.

---

## What You'll Learn

By the end of this session, you'll understand:

1. **Two complementary modes** — G/R/S/O (generative) enables exploration; Literal (enumerative) enables execution
2. **Documents bridge the modes** — The design document + implementation plan carries decisions between thinking and doing
3. **The handoff problem** — Why you can't explore and execute simultaneously
4. **Context management** — Why old documents can poison new work, and how to prevent it

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
| [Assignment 1: ETL Pipeline](assignments/assignment-1-etl-pipeline.md) | Experience the two-mode workflow | ✅ Available |
| Assignment 2: Reduced Scaffolding | Write your own prompts | 🔜 Coming Soon |
| Assignment 3: Quality-Focused | Open-ended design | 🔜 Coming Soon |

**Recommendation:** Complete Assignment 1 before Session 3.

---

## Key Concepts

### The Two Modes

| | G/R/S/O (Generative) | Literal (Enumerative) |
|---|----------------------|----------------------|
| **Agency** | Enabled — AI makes decisions | Disabled — AI follows steps |
| **Purpose** | Exploration, design | Execution, implementation |
| **Output** | Design document + plan | Working code |

### The Natural Flow

```
Your thoughts (vague)
        │
        ▼
G/R/S/O Prompt (exploration enabled)
        │
        ▼
AI generates design + plan
        │
        ▼
You review and approve
        │
        ▼
Code executes the plan (literal mode)
```

### Documents Are the Bridge

The design document + implementation plan isn't just documentation — it's the **continuity artifact** that carries your decisions from exploration mode to execution mode.

---

## Assignment Overview

### Assignment 1: ETL Pipeline

Practice the complete two-mode workflow:
1. Write a G/R/S/O prompt
2. Review the AI's design document and plan
3. Approve (or revise) before any code is written
4. Verify the code meets all requirements

**Core discipline:** If code doesn't work, you fix the *design*, not the code.

Choose from:
- Sales Data Cleaner (default)
- Survey Data Validator
- Financial Data Transformer
- Bring Your Own Data

Choose your difficulty mode (Easy / Medium / Hard) — harder modes mean bigger consequences for design failures.

[→ Start Assignment 1](assignments/assignment-1-etl-pipeline.md)

---

## Sample Data

Assignment 1 uses sample CSV files. These will be provided in the `assignments/data/` folder:

| File | Used For |
|------|----------|
| `messy_sales.csv` | Default task / Sales Cleaner |
| `survey_responses.csv` | Survey Validator option |
| `transactions.csv` | Financial Transformer option |

*Note: Sample data files coming soon.*

---

## Before Session 3

- [ ] Complete Assignment 1 (at least the default task)
- [ ] Notice the two modes in your own AI interactions
- [ ] Pay attention to when you're exploring vs. executing

**Coming in Session 3:** The Generate-Critique Cycle — how to iterate between generating and critiquing for quality.

---

*Session 2 — AI Collaboration Course*
