# Session 3 Assignment: Orchestration Plan

Practice breaking down complex tasks into coordinated sub-agents.

---

## What You'll Practice

This assignment walks you through task decomposition and mode selection:

```
Complex Goal → Task Decomposition → Mode Assignment → Sub-Agent Prompts
```

**The core discipline:** Before any work begins, you plan the orchestration. You identify the sub-agents, assign modes, and write clear prompts for each phase.

---

## The Scenario

Your manager sends you this request:

> "Create a quarterly sales report with visualizations and insights. The report needs to pull data from multiple sources, clean it, analyze trends, and produce a presentation-ready document."

This is too complex for one conversation. You need to orchestrate.

**Assume you have access to:**
- Sales transaction data (CSV)
- Customer demographics data (CSV)
- Last quarter's report (for format reference)

---

## Your Deliverables

### Deliverable 1: Task Decomposition Document

Break the goal into 4-6 sub-agent tasks. For each task:

- **Task name and description** — What this sub-agent accomplishes
- **Input** — What context this sub-agent needs
- **Output** — What deliverable it produces
- **Dependencies** — Which tasks must complete first

### Deliverable 2: Mode Assignment with Justification

For each sub-agent task:

- **Assigned mode** — Research, Architect, Analysis, or Code
- **One-sentence justification** — Why this mode fits the task

### Deliverable 3: One Detailed Sub-Agent Prompt

Choose one of your sub-agent tasks (we recommend the Design task) and write the full prompt including:

- **Context section** — Background the sub-agent needs
- **Task section** — What specifically to do
- **Deliverable section** — What to produce
- **Success criteria section** — How to verify quality

---

## Step-by-Step Instructions

### Step 1: Analyze the Goal

Read the manager's request carefully. What are the implicit requirements?

- Multiple data sources → need integration
- Visualizations → need design decisions
- Insights → need analysis
- Presentation-ready → need quality verification

### Step 2: Identify the Phases

What major phases does this work require? Consider:

- Understanding requirements
- Gathering/cleaning data
- Designing the report structure
- Creating visualizations
- Analyzing for insights
- Reviewing quality
- Producing final output

### Step 3: Create Your Decomposition

Write out your task decomposition document using the [template](template.md). Don't just list tasks — show the flow and dependencies.

### Step 4: Assign Modes

For each task, assign a mode. Use this quick reference:

| Task Type | Mode | Why |
|-----------|------|-----|
| Gathering information | Research | Finding and compiling data |
| Creating designs/plans | Architect | Making decisions, defining structure |
| Reviewing/verifying | Analysis | Critiquing, checking quality |
| Building/implementing | Code | Following a plan to produce output |

### Step 5: Write the Detailed Prompt

For your chosen task (recommend Design), write a complete sub-agent prompt using the four-part template:

```markdown
## Context
[Background the sub-agent needs to know]

## Task
[What specifically to do]

## Deliverable
[What to produce, with structure if relevant]

## Success Criteria
[How to verify this sub-agent succeeded]
```

### Step 6: Review Your Work

Ask yourself:

- Does every task have a clear deliverable?
- Do the modes match the task types?
- Is the sub-agent prompt specific enough to execute?
- Could someone else follow this orchestration plan?

---

## Evaluation Criteria

Your submission will be evaluated on:

| Criterion | What We're Looking For |
|-----------|----------------------|
| **Completeness** | All three deliverables present and filled out |
| **Clarity** | Each task has clear inputs, outputs, and dependencies |
| **Mode Selection** | Modes are appropriate for task types with reasonable justification |
| **Prompt Quality** | Detailed prompt includes all four sections with specificity |
| **Logical Flow** | Tasks build on each other in a sensible order |

---

## Tips for Success

1. **Think outputs, not activities.** Each sub-agent should produce something concrete.

2. **Don't over-decompose.** 4-6 tasks is the sweet spot. Too many creates coordination overhead.

3. **Be specific about dependencies.** "Depends on Task 2" is clearer than "comes later."

4. **Success criteria should be verifiable.** "Good quality" is vague. "Addresses all three data sources" is verifiable.

5. **The design task is often the most interesting.** That's why we recommend writing the detailed prompt for it.

---

## Reference Materials

### Worked Example

See [example-decomposition.md](example-decomposition.md) for a complete worked example using a **different** scenario (customer churn analysis). This shows the expected level of detail.

### Submission Template

Use [template.md](template.md) for your submission. It has all the sections pre-formatted.

---

## Reflection Questions

After completing the assignment, consider:

1. **What was hardest about decomposition?**
   - Where did you struggle to draw boundaries between tasks?
   - Did you find tasks that seemed to overlap?

2. **How did you decide on modes?**
   - Were any assignments unclear?
   - Did the mode selection table help?

3. **How detailed should sub-agent prompts be?**
   - Did you feel like you were writing too much or too little context?
   - What would happen if a sub-agent got this prompt?

4. **Could you run this orchestration?**
   - If you gave these prompts to Kahuna, would it work?
   - What's missing or underspecified?

---

*Session 3 Assignment — AI Collaboration Course*
