# Match Scoring Rubric — Single Source of Truth

This file is the **only** definition of match scoring for this project. The job search agent and the resume tailoring agent both use it. If any other file conflicts with this one, this file wins.

---

## 1. Requirement evidence labels

Classify each JD requirement against the candidate's verified evidence (master resume + `verified-experience-additions.md`):

| Label | Meaning |
|---|---|
| **Strong Match** | Directly demonstrated in production or research work, with specifics. |
| **Partial Match** | Demonstrated in a related form, at smaller scope, or as a contributor rather than owner. |
| **Weak Match** | Only adjacent or conceptual exposure; hard to defend in an interview. |
| **No Evidence** | Not in the verified record, or listed as a confirmed gap. |

Required vs. preferred comes from the JD wording ("required", "must", "minimum" vs. "preferred", "nice to have", "bonus"). If unclear, treat it as preferred and say so.

---

## 2. Components (total 100)

### A. Domain fit — 30
Score the team's actual responsibilities, not just the employer's industry.

| Points | Domain |
|---|---|
| 26–30 | Clinical trial analytics, RWE, biostatistics on clinical data, longitudinal EHR / patient risk modeling |
| 20–27 | Other healthcare applied ML (payer/provider, care management, health-tech product data, med-device analytics) |
| 16–24 | Supply chain, logistics, forecasting, operations research, simulation-heavy planning |
| 6–18 | Other applied DS that explicitly values forecasting, survival analysis, statistical modeling, simulation, optimization, or applied LLM systems |
| 0–8 | No meaningful domain overlap |

### B. Method & technical fit — 30
Weight required methods first, preferred second. Production or research evidence counts more than a tool in a skills list.

| Points | Fit |
|---|---|
| 26–30 | Nearly all required methods are Strong Matches |
| 18–25 | Most required methods match; one is only Partial |
| 10–17 | Core partially matches; two or more required methods are Weak or No Evidence |
| 0–9 | Little overlap |

### C. Seniority & experience fit — 15
Candidate: ~6 years (May 2020 – June 2026), senior IC and tech lead.

| Points | Fit |
|---|---|
| 13–15 | Senior IC; required YOE ≤ 6 |
| 10–12 | Staff/Lead IC with scope matching the evidence, or required YOE of 7 |
| 8–10 | Mid-level role with strong domain alignment, or required YOE of 8 |
| 3–7 | Principal, manager, or director scope beyond the evidence |
| 0–2 | Junior or intern |

### D. Screen competitiveness — 25
Start at 25. For each **required** qualification:

| Evidence | Deduction |
|---|---:|
| No Evidence | −8 |
| Weak Match | −6 |
| Partial Match | −4 |
| Strong Match | 0 |

- Each important **preferred** qualification at Weak or No Evidence: −2 (max −6 total).
- Add up to **+3** when the JD explicitly values a rare differentiator the candidate has (e.g., clinical trial data *and* LLM systems; survival analysis *and* production ML).
- Floor 0, cap 25.

**Overall = A + B + C + D.**

---

## 3. Calibration anchors

Use these to keep scores consistent across runs:

| Example role | A | B | C | D | Total |
|---|---:|---:|---:|---:|---:|
| Senior clinical-trial analytics; requires Python, SQL, survival analysis; SAS preferred | 29 | 25 | 14 | 21 | **89** |
| Senior supply-chain forecasting; requires Spark and Databricks | 22 | 22 | 14 | 9 | **67** |
| Senior product DS; requires live A/B testing and causal inference | 8 | 12 | 14 | 13 | **47** |

---

## 4. Thresholds and actions

| Score | Label | Job search agent | Resume tailoring agent |
|---|---|---|---|
| **≥ 68** | **Tier A** | Main table; apply first; seek referral | Full tailoring; output resume |
| **55–67** | **Tier B** | Main table | Tailor and output resume |
| **50–54** | **Stretch** | Secondary "Stretch" list only | Output resume with a **STRETCH** warning and top gaps at the very top |
| **< 50** | **Stop** | Do not list | STOP. Reply **"NOT A GOOD MATCH"** with the score table and the 2–3 gaps that caused it. No resume. |

---

## 5. Scoring discipline

- Show the score as `Total (A/B/C/D)`, e.g., `78 (28/24/14/12)`, with a one-line rationale per component when space allows.
- A score is a fit estimate, never a probability of getting an interview.
- Do not inflate scores to reach a target number of roles or to justify tailoring.
- Hard filters in the job search agent are separate from scoring: a high score never overrides a failed hard filter.
- Scores made before this rubric existed are not directly comparable; don't re-score old roles unless asked.