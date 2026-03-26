# Assignment 1: Build an ETL Pipeline

Practice the two-mode workflow by building a real data pipeline.

---

## What You'll Practice

This assignment walks you through the complete two-mode workflow from Session 2:

```
G/R/S/O Prompt → Design Document → Implementation Plan → Working Code
```

**The core discipline:** You produce a design and plan FIRST. Only after reviewing and approving the design does code get written. If the code doesn't work, you fix the *design*, not the code.

This teaches the most important lesson in AI collaboration: **design quality determines code quality.**

---

## Choose Your Task

Pick a task that interests you. All tasks teach the same workflow — choose based on what data sounds fun to work with.

### 🎯 Default: Sales Data Cleaner

*Don't feel like choosing? Start here.*

You have a messy sales CSV with inconsistent formatting. Build a pipeline that cleans it up.

**Your Core Requirements:**
1. Load the CSV and identify data quality issues
2. Standardize all date columns to YYYY-MM-DD format
3. Replace empty strings and whitespace-only values with proper nulls
4. Remove exact duplicate rows
5. Output a cleaned CSV file

**Sample Data:** `data/messy_sales.csv` (provided)

---

### 📊 Option A: Survey Data Validator

You have survey responses that need quality checks before analysis.

**Your Core Requirements:**
1. Load the survey data
2. Validate email format (must contain @ and .)
3. Validate age is numeric and between 18-120
4. Validate rating values are 1-5
5. Report all validation failures with row numbers

**Sample Data:** `data/survey_responses.csv` (provided)

---

### 📈 Option B: Financial Data Transformer

You have transaction data that needs reshaping and aggregation.

**Your Core Requirements:**
1. Load transaction data
2. Add a `month` column extracted from date
3. Calculate running balance per account
4. Aggregate total spending by category
5. Output transformed data + summary statistics

**Sample Data:** `data/transactions.csv` (provided)

---

### 🔧 Option C: Bring Your Own Data

Have data you actually care about? Use it!

**Constraints:**
- Define exactly 5 core requirements (specific and verifiable)
- At least one requirement must involve cleaning, validation, or transformation
- Output must be a file (CSV, JSON, or report)

**Write your requirements like this:**
```
1. Load [your specific input file]
2. [First transformation or validation]
3. [Second transformation or validation]
4. [Third transformation or validation]
5. Output to [specific format]
```

---

## Choose Your Difficulty Mode

Now choose how strict you want to be with yourself. This affects what happens if your code doesn't meet the core requirements.

### Why Difficulty Matters

Here's the uncomfortable truth: **the harder the consequences, the better you learn.**

In Easy mode, you can iterate freely if things go wrong. That's comfortable — but it lets you rush through the design phase without really investing in it. "I'll just fix it later" becomes the habit.

In Hard mode, if your design fails, you lose everything and start over. This sounds harsh — but it teaches a critical lesson: *the cost of a bad design is paid in wasted work.* When the stakes are real, you'll spend more time getting your design right before approving it.

The goal of this course is for you to eventually produce designs so solid that the code "prints out" correctly on the first try. Hard mode trains this discipline directly.

### The Modes

| Mode | If Core Requirements Fail... | What You Learn |
|------|------------------------------|----------------|
| 🌱 **Easy** | Iterate on the design freely | Basic workflow familiarity |
| ⚡ **Medium** | Redo design from scratch (same conversation) | Cost of incomplete thinking |
| 🔥 **Hard** | Start a completely new conversation | True investment in design quality |

**Our recommendation:** Try 🔥 Hard mode. Yes, it's painful when you fail. That's the point — you'll work harder to not fail. If you're truly just getting started, Easy mode is fine, but consider upgrading as you get comfortable.

---

## The Prompt

Copy this prompt into your AI copilot. Replace the bracketed section with your chosen task's core requirements.

```markdown
## Goal

Build a data pipeline that accomplishes these requirements:

[PASTE YOUR 5 CORE REQUIREMENTS HERE]

The output should be a working Python script that I can run on the provided data.

## Rules

- You MUST produce a design document FIRST, before any code
- The design document must explain your approach to each requirement
- You MUST produce an implementation plan with specific steps
- Do not write any code until I approve the design and plan
- The script must work with the sample data provided

## Strategies

- Prefer pandas for data manipulation
- Keep the code simple and readable
- Add comments explaining what each section does
- Handle edge cases gracefully (don't crash on unexpected data)

## Opening

First, examine the sample data I'll provide to understand its structure. Then produce:
1. A design document explaining your approach
2. An implementation plan listing the specific steps

Wait for my approval before writing any code.
```

---

## Step-by-Step Instructions

### Step 1: Set Up

1. Download the sample data for your chosen task (or prepare your own)
2. Open your AI copilot (Kahuna, Claude Code, Cursor, etc.)
3. Start a new conversation

### Step 2: Provide Context

Share the sample data file with your copilot so it can examine the structure.

### Step 3: Send the Prompt

Copy the G/R/S/O prompt above (with your chosen requirements) and send it.

### Step 4: Review the Design

The AI should produce:
- **Design Document:** Explaining the approach to each requirement
- **Implementation Plan:** Specific steps it will take

**Before approving, ask yourself:**
- Does this address all 5 core requirements?
- Do I understand the approach being proposed?
- Are there any obvious gaps or risks?
- Would I bet that this plan will work on the first try?

If something seems off, ask questions or request changes to the design NOW. This is the time to catch problems — not after the code is written.

### Step 5: Approve and Execute

Once you're satisfied with the design, tell the AI to proceed with implementation.

### Step 6: Verify Core Requirements

Test the output against each core requirement:

| Requirement | ✅ Pass | ❌ Fail |
|-------------|---------|---------|
| 1. | | |
| 2. | | |
| 3. | | |
| 4. | | |
| 5. | | |

**If any requirement fails:** Follow your chosen difficulty mode.
- 🌱 Easy: Iterate on the design to fix it
- ⚡ Medium: Redo the design from scratch in the same conversation
- 🔥 Hard: Start a completely new conversation and try again

**If all requirements pass:** Congratulations! You've successfully completed the two-mode workflow.

### Step 7 (Optional): Add Enhancements

If your core requirements all pass, you can now iterate freely to add enhancements:

- Generate a report showing what was changed/validated/transformed
- Add logging for each pipeline step
- Support additional input formats
- Create visualizations of the results

Enhancements are iterative — no need to follow strict difficulty modes here.

---

## Reflection Questions

After completing the assignment, take a few minutes to reflect:

1. **What decisions did the design phase surface?**
   - What choices did the AI make that you wouldn't have thought of?
   - Were there trade-offs discussed that surprised you?

2. **How much did you invest in reviewing the design?**
   - Did you approve too quickly? (Be honest!)
   - Did you catch any issues before code was written?
   - In hindsight, what should you have questioned?

3. **What would you change about your prompt?**
   - Were any requirements ambiguous?
   - Did the AI misunderstand something you thought was clear?
   - What would you add or clarify next time?

4. **How did your difficulty mode affect your behavior?**
   - Did the stakes change how carefully you reviewed?
   - Would you choose a different mode next time?

---

## Sample Data

Download from the `data/` folder in this directory:

| Task | File |
|------|------|
| Default / Sales Cleaner | `data/messy_sales.csv` |
| Survey Validator | `data/survey_responses.csv` |
| Financial Transformer | `data/transactions.csv` |

*Note: Sample data files coming soon.*

---

## What's Next

After completing this assignment, you've experienced the core two-mode workflow:

1. ✅ G/R/S/O prompt triggers exploration and design
2. ✅ Design document captures decisions and approach
3. ✅ Implementation plan becomes literal instructions
4. ✅ Code executes the plan

**Assignment 2** will reduce the scaffolding — you'll write more of the prompt yourself rather than using our template.

---

*Session 2 Assignment 1 — AI Collaboration Course*
