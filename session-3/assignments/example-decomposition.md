# Worked Example: Customer Churn Analysis Pipeline

This is a complete worked example showing how to write a G/R/S/O prompt to coordinate complex AI work and understand the expected workflow.

**Note:** This uses a *different* scenario than the assignment (customer churn analysis instead of quarterly sales report) so you can see the expected format without having the answer given away.

---

## The Scenario

Your data science team lead asks:

> "Build an automated customer churn analysis pipeline. We need to identify which customers are at risk of leaving, understand why, and produce a report with recommendations for the retention team."

**Available data:**
- Customer activity logs (CSV)
- Customer support ticket history (CSV)
- Subscription and billing data (CSV)

---

## Part 1: G/R/S/O Prompt

This is the prompt you would write to coordinate this work. Notice: you're not specifying every step — you're describing what needs to be achieved and letting the AI plan the details.

### Goal (G)

Build an automated customer churn analysis pipeline that identifies at-risk customers, explains why they're at risk, and produces a report with actionable recommendations for the retention team.

### Rules (R)

- All three data sources (activity logs, support tickets, billing) must be incorporated
- Churn definition must be unambiguous and implementable as code
- Risk scoring must produce actionable segments, not just a single number
- Final output must be understandable by non-technical retention team members
- Use a rules-based or simple statistical approach — no complex ML models

### Strategies (S)

- Start by assessing data quality and join keys before designing the pipeline
- Define churn operationally based on billing data (e.g., payment gaps > X days)
- Create features from all three data sources that might indicate churn risk
- Use Python for implementation — pandas for data processing
- Structure the final report with executive summary, methodology, findings, recommendations

### Opening (O)

**Available data files:**
- Customer activity logs (CSV): Contains `customer_id`, `activity_type`, `timestamp`, `session_duration`
- Support tickets (CSV): Contains `customer_id`, `ticket_date`, `category`, `resolution_time`, `satisfaction_score`
- Billing data (CSV): Contains `customer_id`, `plan_type`, `monthly_amount`, `signup_date`, `last_payment_date`

**Data quality observations:**
- Activity logs have some missing `session_duration` values
- Support tickets have inconsistent `category` naming
- Billing data appears complete but needs date parsing

**Current state:**
- No existing pipeline or analysis
- Retention team has requested this for quarterly planning
- Data files are in the /data directory

**Available resources:**
- Python environment with pandas, numpy
- Previous quarter's ad-hoc analysis (for reference format, not for reuse)

---

## Part 2: Expected Workflow

Here's what the AI will do with your prompt:

### Planning Phase

- **What happens:** The AI analyzes your requirements and designs the approach
- **What it will produce:** A design document and implementation plan covering:
  - Data cleaning approach for each source
  - Feature engineering definitions
  - Churn definition criteria
  - Risk scoring methodology
  - Pipeline architecture
  - Report structure
- **How your G/R/S/O guides it:** Your Rules (all three sources, unambiguous churn definition, actionable segments) and Strategies (rules-based approach, pandas) set the boundaries. The Planning phase explores options *within* those boundaries.

### Execution Phase

- **What happens:** The AI follows the plan to produce working code and output
- **What it will produce:** Working Python code that:
  - Loads and cleans the three CSV files
  - Engineers the features defined in the plan
  - Applies the churn definition
  - Calculates risk scores
  - Generates the report
- **How the plan guides it:** The plan becomes specific instructions. For example, "Create a feature called `support_ticket_count` calculated as the count of tickets per customer_id in the last 90 days" — the Execution phase follows this exactly without reinterpreting.

### Verification Phase

- **Needed?** Yes
- **Why:** This is a data pipeline with business impact. Verification ensures the implementation matches the design and the output is correct.
- **What it will check:**
  - All three data sources are loaded and joined correctly
  - Features match the definitions in the plan
  - Churn classification logic matches the specification
  - Risk segments are distinct and actionable
  - Report format is suitable for non-technical audience

---

## Part 3: Flow-Through Reflection

### What constraints will guide the Planning phase?

Your prompt flows to the Planning phase with these constraints:
- **From Rules:** "All three data sources must be incorporated" → Planning must design a pipeline that uses all three
- **From Rules:** "Churn definition must be unambiguous" → Planning must produce a precise, implementable definition
- **From Rules:** "No complex ML models" → Planning designs rules-based scoring, not neural networks
- **From Strategies:** "Use Python/pandas" → Planning designs for this technology stack

### What will become specific instructions for the Execution phase?

The plan contains specifics like:
- "Load activity_logs.csv using pandas.read_csv()"
- "Handle missing session_duration by imputing with median value"
- "Create feature: `days_since_last_activity` = current_date - max(timestamp) per customer_id"
- "Define churned = True if last_payment_date > 30 days ago"
- "Calculate risk_score = weighted sum of [feature list]"

These are **specific** — the Execution phase follows them exactly without making design decisions.

### Where is the handoff point?

The **handoff point** is when the plan is complete.

```
You ──G/R/S/O──► AI Coordinator ──G/R/S/O──► Planning ──Plan──► Execution
                                                          ▲
                                                   HANDOFF POINT
                                              (G/R/S/O ends here)
```

**Before the handoff point:** Exploration and decision-making happen. The Planning phase considers options, makes tradeoffs, defines specifics. Your G/R/S/O prompt guides these decisions but doesn't make them directly.

**After the handoff point:** Specific execution. The Execution phase doesn't decide *what* to build — the plan already specifies that. The Execution phase decides only *how* to build it (variable names, code organization, etc.).

---

## Why This Example Works

Notice several things about this approach:

1. **You wrote ONE prompt** — to coordinate the work. You didn't write separate detailed instructions for planning, execution, and verification. The AI handles that breakdown.

2. **G/R/S/O structure at coordination level** — Your Goal describes the outcome. Your Rules are hard constraints. Your Strategies guide without dictating. Your Opening establishes concrete context.

3. **The flow-through is clear** — Your constraints flow to the Planning phase, the Planning phase's decisions become the plan, the plan becomes specific instructions for the Execution phase.

4. **Workflow is explicit** — Planning → Execution → Verification. Each phase produces something concrete before the next begins.

5. **The handoff point is identified** — The plan is where high-level guidance ends. Everything after that is specific execution.

6. **Verification is justified** — Not every task needs it, but this one does because of business impact.

---

## Comparison: Assignment vs. Example

| Aspect | This Example (Churn) | Your Assignment (Sales Report) |
|--------|---------------------|-------------------------------|
| Domain | Customer retention | Sales analytics |
| Data sources | Activity, tickets, billing | Sales transactions, customer demographics |
| Output | Risk report for retention team | Quarterly report for management |
| Key challenge | Defining churn criteria | Integrating and cleaning messy data |

The *structure* is the same — the *content* is different. Use this example as a format guide, not a content guide.

---

*Worked Example — Session 3 Assignment*
