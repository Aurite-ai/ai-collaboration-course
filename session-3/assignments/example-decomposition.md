# Worked Example: Customer Churn Analysis Pipeline

This is a complete worked example showing how to decompose a complex task, assign modes, and write a detailed sub-agent prompt.

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

## Part 1: Task Decomposition

### Task 1: Data Assessment

- **Description:** Examine all three data sources to understand their structure, quality, and how they can be joined together.
- **Input:** Raw CSV files (activity logs, support tickets, billing data)
- **Output:** Data assessment report documenting schema, quality issues, and join keys
- **Dependencies:** None

### Task 2: Pipeline Design

- **Description:** Design the data pipeline architecture including cleaning, feature engineering, and analysis approach.
- **Input:** Data assessment report from Task 1
- **Output:** Design document with pipeline stages, feature definitions, and churn criteria
- **Dependencies:** Task 1

### Task 3: Design Review

- **Description:** Review the pipeline design for completeness, feasibility, and alignment with business goals.
- **Input:** Design document from Task 2
- **Output:** Assessment with findings, gaps identified, and recommendations
- **Dependencies:** Task 2

### Task 4: Pipeline Implementation

- **Description:** Build the data pipeline according to the approved design.
- **Input:** Approved design document (after Task 3 revisions if needed)
- **Output:** Working Python script that produces churn analysis results
- **Dependencies:** Task 2, Task 3

### Task 5: Results Analysis

- **Description:** Analyze the pipeline output to extract insights and formulate recommendations.
- **Input:** Churn analysis results from Task 4
- **Output:** Insights document with key findings and retention recommendations
- **Dependencies:** Task 4

### Task 6: Report Generation

- **Description:** Compile findings into a presentation-ready report for the retention team.
- **Input:** Insights document from Task 5, design document from Task 2
- **Output:** Final report with executive summary, methodology, findings, and recommendations
- **Dependencies:** Task 5

---

## Part 2: Mode Assignments

| Task | Mode | Justification |
|------|------|---------------|
| Task 1: Data Assessment | Research | Gathering and documenting information about the data |
| Task 2: Pipeline Design | Architect | Creating a new design with decisions about structure |
| Task 3: Design Review | Analysis | Critiquing the design against criteria |
| Task 4: Pipeline Implementation | Code | Following the design to produce working code |
| Task 5: Results Analysis | Analysis | Interpreting results and identifying patterns |
| Task 6: Report Generation | Architect | Creating a new document structure with synthesis |

---

## Part 3: Detailed Sub-Agent Prompt

**Task selected:** Task 2: Pipeline Design

### Context

We're building an automated customer churn analysis pipeline for the retention team. The goal is to identify at-risk customers and understand churn drivers.

**Data Assessment Summary (from Task 1):**
- Customer activity logs: 50,000 rows, columns include customer_id, activity_type, timestamp, session_duration
- Support tickets: 12,000 rows, columns include customer_id, ticket_date, category, resolution_time, satisfaction_score
- Billing data: 8,000 unique customers, columns include customer_id, plan_type, monthly_amount, signup_date, last_payment_date

**Key findings from assessment:**
- All three datasets can be joined on customer_id
- Activity logs have 3% missing session_duration values
- Support tickets have categories: billing, technical, account, other
- Billing data shows 15% of customers have payment gaps > 30 days

### Task

Design the data pipeline architecture for the churn analysis. Your design should cover:

1. **Data cleaning approach** — How to handle missing values and data quality issues
2. **Feature engineering** — What features to create that might predict churn
3. **Churn definition** — How we operationally define "churned" vs "active"
4. **Analysis approach** — What method to use for identifying churn risk

Focus on practical, implementable decisions. We're not building a complex ML model — we want a rules-based or simple statistical approach that the retention team can understand.

### Deliverable

A design document with the following sections:

1. **Pipeline Overview** — High-level flow diagram (ASCII is fine)
2. **Data Cleaning Steps** — Specific actions for each data quality issue
3. **Feature Definitions** — Table of features with name, calculation, and rationale
4. **Churn Definition** — Precise criteria for classifying customers
5. **Risk Scoring Approach** — How at-risk customers will be identified
6. **Output Specification** — What the final analysis output looks like

### Success Criteria

- [ ] All three data sources are incorporated into the pipeline
- [ ] Missing value handling is specified for each known issue
- [ ] At least 5 features are defined with clear calculations
- [ ] Churn definition is unambiguous (could be implemented as code)
- [ ] Risk scoring produces actionable segments (not just one number)
- [ ] Output format is suitable for the retention team (non-technical audience)

---

## Why This Example Works

Notice several things about this decomposition:

1. **Clear deliverables** — Every task produces something concrete (report, document, code, etc.)

2. **Logical flow** — Each task builds on previous ones. You can't design without assessing, can't implement without designing, can't analyze without results.

3. **Generate-critique cycle** — Tasks 2 and 3 form a generate-critique pair. The design (Architect) gets reviewed (Analysis) before implementation proceeds.

4. **Mode selection follows function** — Research for gathering info, Architect for creating, Analysis for reviewing, Code for implementing.

5. **Detailed prompt has all four sections** — Context gives background, Task gives scope, Deliverable gives structure, Success Criteria gives verification.

6. **Success criteria are checkable** — Not "good design" but "at least 5 features defined with clear calculations."

---

*Worked Example — Session 3 Assignment*
