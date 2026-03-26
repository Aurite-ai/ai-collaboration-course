# Session 2 Assignments

Practice assignments for "The Two Modes of Working"

---

## Available Assignments

| # | Assignment | Focus | Scaffolding | Status |
|---|------------|-------|-------------|--------|
| 1 | [ETL Pipeline](assignment-1-etl-pipeline.md) | Experience the workflow | Full prompt provided | ✅ Available |
| 2 | Reduced Scaffolding | Write your own prompts | Partial prompt | 🔜 Coming Soon |
| 3 | Quality-Focused | Open-ended design | Problem only | 🔜 Coming Soon |

---

## Assignment 1: ETL Pipeline

**What you'll practice:**

The complete two-mode workflow:
```
G/R/S/O Prompt → Design Document → Implementation Plan → Working Code
```

**The core discipline:** Produce a design and plan FIRST. Only after reviewing and approving the design does code get written. If the code doesn't work, you fix the *design*, not the code.

**Task options:**
- 🎯 Sales Data Cleaner (default — start here if unsure)
- 📊 Survey Data Validator
- 📈 Financial Data Transformer
- 🔧 Bring Your Own Data

**Difficulty modes:**
- 🌱 Easy — Iterate freely if code fails
- ⚡ Medium — Redo design from scratch (same conversation)
- 🔥 Hard — Start a completely new conversation

[→ Start Assignment 1](assignment-1-etl-pipeline.md)

---

## Sample Data

Sample CSV files for each task option:

| File | Task |
|------|------|
| `data/messy_sales.csv` | Default / Sales Cleaner |
| `data/survey_responses.csv` | Survey Validator |
| `data/transactions.csv` | Financial Transformer |

*Note: Sample data files coming soon.*

---

## Design Principles

These assignments are designed with a specific pedagogical approach:

1. **No iteration on code — only iteration on design.** If code fails, you revise the design, not the code. This teaches that design quality determines code quality.

2. **Three difficulty axes:**
   - Task type (precision vs. quality)
   - Scaffolding level (how much prompt we provide)
   - Consequence strictness (what happens when code fails)

3. **Student choice.** You choose your task and difficulty mode. We recommend Hard mode — the pain of starting over teaches you to invest in design.

For the full framework, see [Assignment Design Framework](../../resources/assignment-design-framework.md).

---

*Session 2 Assignments — AI Collaboration Course*
