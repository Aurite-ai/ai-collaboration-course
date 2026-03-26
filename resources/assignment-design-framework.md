# Assignment Design Framework

A framework for designing AI collaboration practice assignments that train specific skills through structured exercises.

---

## Core Principle: Two-Mode Workflow

All assignments teach the same fundamental workflow:

```
G/R/S/O Prompt → Design Document → Implementation Plan → Code Execution
```

Students must produce a **design document and plan** before any code is written. This is non-negotiable.

**The key constraint:** If the code doesn't work, students revise the *design*, not the code. This teaches that design quality determines code quality.

---

## The Three Difficulty Axes

Assignments vary along three independent dimensions:

### Axis 1: Task Type (What Skill Is Trained)

| Type | Noise Level | Rule Complexity | Skill Trained | Evaluation Question |
|------|-------------|-----------------|---------------|---------------------|
| **Type A: Precision** | Low | High | Executing exactly to spec | "Did it match requirements precisely?" |
| **Type B: Quality** | High | Low | Generating excellent artifacts | "How good is the result?" |
| **Type C: Mastery** | High | High | Both precision and quality | "Did it hit the spec AND is it excellent?" |

**The insight:** These types parallel prompt styles:
- Type A (low noise, high rules) ≈ Literal instructions territory
- Type B (high noise, low rules) ≈ G/R/S/O territory
- Type C = Both combined (advanced)

**Pedagogical progression:** A → B → C

---

### Axis 2: Scaffolding Level (How Much We Provide)

| Level | What We Provide | What Student Provides | Focus |
|-------|-----------------|----------------------|-------|
| **Level 1** | Complete G/R/S/O prompt + context files | Nothing (copy-paste) | Observe the workflow |
| **Level 2** | Complete G/R/S/O prompt | Their own context/data | Personalize the task |
| **Level 3** | Problem description only | G/R/S/O prompt + context | Write effective prompts |
| **Level 4** | Nothing | Identify problem + prompt + context | Full independence |

**Pedagogical progression:** 1 → 2 → 3 → 4

At Level 1, students experience the workflow without writing anything. By Level 4, they own the entire process.

---

### Axis 3: Consequence Strictness (What Happens on Failure)

| Mode | If Core Capabilities Fail... | Learning Intensity |
|------|------------------------------|-------------------|
| **🌱 Easy** | Iterate on existing design freely | Gentlest — good for first exposure |
| **⚡ Medium** | Redo design from scratch (same conversation) | Moderate — feels the cost of bad design |
| **🔥 Hard** | Start completely new conversation | Maximum — painful but memorable |

**Recommendation:** Hard mode produces the deepest learning. The pain of starting over teaches students to invest in their designs.

**For optional assignments:** Present all three modes; recommend Hard mode; let students self-select.

---

## Assignment Structure

Every assignment, regardless of difficulty settings, follows this structure:

### 1. Core Capabilities (Must Work in One Pass)

Define specific, verifiable capabilities that must work from a single design→code pass.

```markdown
CORE CAPABILITIES:
☐ [Specific capability 1]
☐ [Specific capability 2]
☐ [Specific capability 3]

If ANY core capability fails → follow your chosen consequence mode
```

### 2. Enhancements (Iterate After Core Works)

Define optional improvements that can be added iteratively after core success.

```markdown
ENHANCEMENTS (only after core works):
☐ [Nice-to-have feature 1]
☐ [Nice-to-have feature 2]
```

### 3. Reflection Prompts

Questions that reinforce learning:
- What decisions did the design phase surface?
- What would you change about your design?
- Where did the AI need more guidance?

---

## Suggested Progression for Session 2

| Assignment | Task Type | Scaffolding | Consequences | Description |
|------------|-----------|-------------|--------------|-------------|
| **1** | Type A (Precision) | Level 1 (full prompt) | Student chooses | Watch the workflow happen |
| **2** | Type A (Precision) | Level 2-3 | Student chooses | Start writing prompts |
| **3** | Type B (Quality) | Level 2-3 | Student chooses | Open-ended design |

This progression:
1. First assignment: Pure observation (copy-paste, see the flow)
2. Second assignment: Begin taking ownership (write prompt or context)
3. Third assignment: Different skill type (quality vs precision)

---

## Domain Recommendations

For data analytics students (ipynb/notebook familiarity):

### Good Domains
- Data cleaning pipelines
- Summary statistics / EDA tools
- Data validation checkers
- Report generators
- Visualization scripts

### Why These Work
- Universal pain points (everyone has messy data)
- Multiple valid approaches (forces design decisions)
- Tangible results (before/after visible)
- Low stakes (can verify output, undo mistakes)

---

## Future Extensions

### Type C (Mastery) Assignments

High noise + high rule complexity. Both precision AND quality matter.

Example: "Build a data pipeline that meets these exact specifications, integrates with this complex existing codebase, AND is production-quality."

Not yet designed — for advanced students who've mastered Types A and B.

### Technical Enforcement

Currently, consequence strictness is pedagogical (honor system). Future assignments could explore:
- Read-only code output
- Automated verification of core capabilities
- Required "design approval" checkpoint before code generation

---

## Key Takeaways for Assignment Designers

1. **Always require design first** — No code without a design document and plan
2. **Make success criteria clear** — Students should know exactly when they've succeeded
3. **Choose difficulty consciously** — Vary Task Type, Scaffolding, and Consequences intentionally
4. **Start easy, increase challenge** — Level 1 + Type A before Level 3 + Type B
5. **Let students choose consequence mode** — Hard mode is recommended but not required

---

*Framework developed for USC AI Collaboration course, March 2026*
