# Skill Specification: Collaborative Socratic Decision Framework

## 1. Metadata
- **Skill Name:** `collaborative_socratic_decision_triage`
- **Version:** `1.0.0`
- **Description:** Guides teams and managers through structured decision triage, assumption stress-testing, and cognitive bias mitigation using a non-adversarial Socratic inquiry model integrated with MBA strategic frameworks.
- **Author/Owner:** Management Decision Systems
- **Trigger Patterns:** 
  - "Run decision triage on [initiative]"
  - "Stress-test assumptions for [proposal]"
  - "Evaluate strategic options for [project]"
  - "Review definition alignment on [concept]"

---

## 2. Objective & Scope
The goal of this skill is to evaluate ambiguous, non-programmed business and engineering decisions by:
1. Clarifying foundational definitions without creating defensive resistance.
2. Uncovering unexamined assumptions along the Ladder of Inference.
3. Conducting rigorous pre-mortem analysis on potential failure modes.
4. Preserving relational trust and team alignment (subordinating pure dialectic victory to actionable consensus).

---

## 3. Core Execution Protocol

```
[Input: Decision Proposal / Problem Statement]
                   │
                   ▼
       Step 1: Decision Triage
  (Programmed vs. Non-Programmed)
                   │
                   ▼
  Step 2: Definition Alignment Audit
(Neutral, Objective Parameterization)
                   │
                   ▼
Step 3: Ladder of Inference & Bias Scan
 (Identify Inferred Steps & Blind Spots)
                   │
                   ▼
  Step 4: Pre-Mortem Scenario Matrix
  (Map Failure Modes across Options)
                   │
                   ▼
   Step 5: Trip Wire & Action Commit
  (Falsification Criteria & Governance)
```

---

## 4. Phase-by-Phase Instructions

### Phase 1: Decision Triage (Soll, Milkman, & Payne)
Classify the nature of the decision before engaging in deep questioning:
* **Programmed Decision:** Routine, recurring, governed by existing rules or quantitative thresholds.
  * *Action:* Do not run full dialectic analysis. Apply standard operating procedures or decision trees.
* **Non-Programmed Decision:** Novel, unstructured, high-ambiguity, or strategic.
  * *Action:* Proceed to Phase 2.

### Phase 2: Depersonalized Socratic Definition Audit
Examine core terms to ensure cross-functional alignment. 
* **Directive:** Frame questions around shared technical or operational benchmarks, never individual competence.
* **Bad Practice (Adversarial):** *"What do you mean by scalable? Can you even define that?"*
* **Best Practice (Collaborative Socratic):** *"To make sure engineering and product share the same baseline, what specific throughput and latency thresholds are we using to define 'scalable' for this release?"*

### Phase 3: Ladder of Inference & Cognitive Bias Scan (Argyris & Kahneman)
Trace the proposal from raw data to proposed action:
1. **Raw Observable Data:** What objective facts exist that everyone agrees on?
2. **Selected Data & Interpretations:** What data was prioritized, and what was omitted?
3. **Implicit Assumptions:** What must be true for this recommendation to work?
4. **Bias Audit:**
   * *WYSIATI Check:* What information is currently invisible to us?
   * *Status Insecurity / Sunk Cost:* Is the proposal defending prior investments or organizational face?
   * *Curse of Knowledge:* Are leaders assuming alignment simply because the logic is clear to them?

### Phase 4: Pre-Mortem Scenario Planning
Evaluate at least three paths forward (e.g., Aggressive Implementation, Complete Consensus/Status Quo, Calibrated Middle Ground):
* Assume the decision failed catastrophically 12 months after deployment.
* Identify the primary failure vector for each alternative.
* Evaluate whether the failure stems from flawed execution, ambiguous definitions, or social/relational breakdown.

### Phase 5: Trip Wire Definition
Establish an objective threshold that halts or redirects the decision:
* **Operational Trip Wire:** Quantitative metric that signals an assumption is false (e.g., *"If conversion drops below $X\%$ in week 2, the rollout pauses"*).
* **Interpersonal Trip Wire:** If stakeholders display defensive recoil (arm crossing, monosyllabic agreement, appeal to raw authority), pause the inquiry immediately and switch to joint hypothesis generation.

---

## 5. Input & Output Contract

### Required Inputs
```json
{
  "decision_context": "Brief summary of the business or technical dilemma",
  "stakeholders": ["Engineering", "Product", "Operations"],
  "proposed_action": "Initial solution proposed by the team",
  "stated_rationale": "Why the team believes this is the optimal approach"
}
```

### Template Output Schema (Markdown)

```markdown
### 1. Decision Classification
- **Type:** [Programmed | Non-Programmed]
- **Readiness Level:** [Low | Medium | High]
- **Triage Rationale:** [Why full analysis is or is not warranted]

### 2. Definition & Alignment Audit
- **Contested / Ambiguous Terms:** [List key nouns/adjectives, e.g., 'Reliable', 'Ready']
- **Operational Reframing Questions:**
  - *Term 1:* [Depersonalized probe targeting shared benchmarks]
  - *Term 2:* [Depersonalized probe targeting boundaries]

### 3. Ladder of Inference Diagnostic
- **Observed Data:** [Facts verified by all parties]
- **Inferred Assumptions:** [Critical unverified links in logic]
- **Flagged Biases:** [Identified cognitive traps]

### 4. Pre-Mortem Evaluation Matrix
| Option | Proposed Path | Primary Failure Mode | Organizational Consequence |
| :--- | :--- | :--- | :--- |
| A | [Option A] | [Cause of failure] | [State of team/product] |
| B | [Option B] | [Cause of failure] | [State of team/product] |
| C | [Option C] | [Cause of failure] | [State of team/product] |

### 5. Governance & Trip Wires
- **Quantitative Trip Wire:** [Measurable condition to reconsider]
- **Relational Trip Wire:** [Behavioral indicator to de-escalate debate]
- **Next Immediate Step:** [Single operational next action]
```