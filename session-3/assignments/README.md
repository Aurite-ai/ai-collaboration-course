# Session 3 Assignment: Coordinating Complex AI Tasks

Practice writing G/R/S/O prompts to coordinate multi-step AI work.

---

## What You'll Practice

This assignment teaches you to write prompts that coordinate complex, multi-step AI work:

```
Complex Goal → Your G/R/S/O Prompt → AI Coordinator → Planning → Execution → Result
```

**The core insight:** For complex tasks, you don't tell the AI exactly what to do step-by-step. Instead, you write a well-structured G/R/S/O prompt that gives the AI everything it needs to plan and execute the work itself.

Your prompt flows through the system:
- The **AI Coordinator** receives your prompt and breaks the work into phases
- The **Planning phase** creates a detailed approach and implementation plan
- The **Execution phase** follows the plan to produce the actual output

---

## The Scenario

Your manager sends you this request:

> "Create a quarterly sales report with visualizations and insights. The report needs to pull data from multiple sources, clean it, analyze trends, and produce a presentation-ready document."

This is too complex for a simple prompt. You need to coordinate multiple steps.

**Use the provided data files:**
- `data/sales_transactions.csv` — Q1 sales with dates, products, amounts, regions
- `data/customer_demographics.csv` — Customer info for segmentation analysis
- `data/q4_report_template.md` — Last quarter's report format (reference)

Before writing your prompt, **examine the data**. You'll notice it has realistic quality issues that need addressing (inconsistent formats, missing values, duplicates).

---

## Your Deliverables

### Deliverable 1: G/R/S/O Prompt

Write a complete G/R/S/O prompt for the quarterly sales report task. Include:

- **Goal (G)** — What the final output should achieve
- **Rules (R)** — Hard constraints the work must satisfy
- **Strategies (S)** — Suggested approaches or phasing
- **Opening (O)** — Current state, available data files, context

### Deliverable 2: Expected Workflow

Describe the step-by-step workflow you expect:

- What will the **Planning phase** produce?
- What will the **Execution phase** produce?
- Will a **Verification step** be needed? Why or why not?

### Deliverable 3: Reflection on Flow-Through

Answer: How does your G/R/S/O prompt flow through the system?

- What constraints will guide the Planning phase?
- What will become specific instructions for the Execution phase?
- Where is the **handoff point** — where does your high-level prompt become detailed instructions?

---

## Step-by-Step Instructions

### Step 1: Examine the Data

Open the data files and understand their structure:

**`sales_transactions.csv`:**
- What columns are present?
- What data quality issues do you notice?
- What date range does it cover?

**`customer_demographics.csv`:**
- How can this be joined with sales data?
- Any data quality issues?

**`q4_report_template.md`:**
- What sections does the report need?
- What format is expected?

### Step 2: Analyze the Goal

Read the manager's request carefully. What are the implicit requirements?

- Multiple data sources → need data integration
- Visualizations → need design decisions
- Insights → need analysis methodology
- Presentation-ready → need quality verification

### Step 3: Draft Your G/R/S/O Prompt

Use the G/R/S/O structure from Session 1, now applied at the coordination level:

| Element | What to Include |
|---------|-----------------|
| **Goal (G)** | What success looks like for the complete work |
| **Rules (R)** | Hard constraints the work must satisfy |
| **Strategies (S)** | Suggested approaches, preferred tools, phasing hints |
| **Opening (O)** | What data exists, what files are available, current state |

**Remember:** You're describing work to be *coordinated*, not code to be *written*.

### Step 4: Map the Expected Workflow

The AI will follow a workflow like:

```
AI Coordinator → Planning → Execution → (Verification)
```

For each phase, describe:
- What happens in this phase
- What output it produces
- How your G/R/S/O prompt guides its work

### Step 5: Trace the Flow-Through

Your G/R/S/O prompt flows through the system:

```
You ──G/R/S/O──► AI Coordinator ──G/R/S/O──► Planning ──Plan──► Execution
                                                          ▲
                                                   HANDOFF POINT
                                              (G/R/S/O ends here)
```

Explain:
- Which parts of your prompt guide the Planning phase's design work?
- Which parts become specific instructions in the implementation plan?
- Where does the flow-through "hand off" from high-level guidance to specific execution?

### Step 6: Self-Check Your Work

Use the rubric below to verify your submission.

---

## Self-Check Rubric

Before submitting, verify your work against these criteria:

| Criterion | ✅ Pass | ❌ Needs Work | Notes |
|-----------|---------|---------------|-------|
| **Goal (G)** — Describes outcome, not process | | | |
| **Rules (R)** — Hard constraints, not preferences | | | |
| **Strategies (S)** — Guidance without over-specifying | | | |
| **Opening (O)** — References actual data files | | | |
| **Workflow** — Planning → Execution → Verification described | | | |
| **Flow-through** — Shows how constraints reach each phase | | | |
| **Handoff point** — Identifies where instructions become specific | | | |

**Passing criteria:** All seven items should be checked ✅ Pass.

---

## Tips for Success

1. **Write to coordinate, not to implement.** You're describing what needs to happen, not writing the code yourself.

2. **Goals describe outcomes.** "A presentation-ready report" is a goal. "Use Python pandas" is a strategy.

3. **Rules are constraints, not preferences.** "Must include last quarter comparison" is a rule. "It would be nice to have charts" is not.

4. **Strategies guide without dictating.** Suggest approaches the AI can use, but let it make detailed decisions.

5. **Opening establishes concrete context.** Reference the actual data files. Describe what you observed in them.

6. **The handoff point matters.** Understanding where your high-level guidance becomes specific instructions is the key insight of this session.

---

## Reference Materials

### Worked Example

See [example-decomposition.md](example-decomposition.md) for a complete worked example using a **different** scenario (customer churn analysis). This shows a G/R/S/O prompt and the expected workflow without giving away the assignment answer.

### Submission Template

Use [template.md](template.md) for your submission. It has all the sections pre-formatted.

### Sample Data

The `data/` folder contains:
- `sales_transactions.csv` — 57 rows of Q1 2024 sales data
- `customer_demographics.csv` — 27 customer records
- `q4_report_template.md` — Example of expected output format

---

## Optional: Hands-On Execution

If you chose ⚡ Challenge or 🔥 Hard mode, try running your prompt!

### How to Execute

1. Copy your complete G/R/S/O prompt
2. Open your AI tool (ChatGPT, Claude, Copilot, Cursor, etc.)
3. Share the data files with the AI (upload or paste contents)
4. Send your prompt and observe what happens

### What to Report

- Did the AI follow the workflow you expected?
- Did it handle the data quality issues appropriately?
- What would you change about your prompt based on the results?

### If It Doesn't Work (🔥 Hard Mode)

1. Identify what went wrong
2. Revise your original G/R/S/O prompt
3. Try again with the revised prompt
4. Document what you changed and why

---

## Reflection Questions

After completing the assignment, consider:

1. **How does G/R/S/O at the coordination level differ from Session 1?**
   - Are you describing different things?
   - What's the same structure at different levels of detail?

2. **Why don't you write detailed step-by-step instructions?**
   - What would happen if you tried to specify every step?
   - What value does the planning phase add?

3. **Where does the handoff point occur?**
   - At what point does your high-level guidance become specific instructions?
   - What role does the implementation plan play?

4. **What did running the prompt teach you?** (if you executed it)
   - Did the AI interpret your prompt as you expected?
   - What assumptions did you make that the AI didn't share?

---

## Evaluation Criteria

Your submission will be evaluated on:

| Criterion | What We're Looking For |
|-----------|----------------------|
| **G/R/S/O Quality** | Each element is present, appropriate, and well-written |
| **Appropriate Abstraction** | Prompt describes coordination, not implementation details |
| **Workflow Understanding** | Clear description of Planning → Execution → Verification flow |
| **Flow-Through Understanding** | Shows how your prompt guides each phase |
| **Data Grounding** | Opening references actual data files and their characteristics |
| **Completeness** | All three deliverables present and thoughtful |

---

*Session 3 Assignment — AI Collaboration Course*
