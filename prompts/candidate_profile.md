# Candidate Profile — Single Source of Truth

**Owner:** Jianhong (JC) Chen · **Last verified:** 2026-10-25

This file is the only record of what is true about the candidate. The job search agent, the resume tailoring agent, cover letters, and interview prep all read from it. Resumes are *generated* from this file; they are never the source.

**Rules for any agent using this file**

1. Only claim what is in Sections 1–8. Section 11 lists items that are **not yet verified**; never use them until JC moves them up.
2. Every number on a resume must be (a) measured, (b) a labeled backtest/projection, or (c) an informal estimate with a one-sentence basis, marked with "~". Invented numbers are never allowed. If no defensible number exists, use scale or scope facts instead.
3. About 6–8 of 11 resume bullets with an outcome number is enough.
4. Use the "Never say" lines exactly as written. They exist because earlier resumes overclaimed.
5. If this file conflicts with any prompt, resume, or older note, this file wins.

---

## 1. Identity and logistics

| Field | Value |
|---|---|
| Name | Jianhong Chen (goes by JC) |
| Location | Bay Area, CA (moved back to the US in 2026 after ~2 years at Mindray in Shenzhen) |
| Work authorization | U.S. Citizen; no sponsorship needed |
| Relocation | Open to anywhere in the United States |
| Email | jjianhongchen@gmail.com |
| Phone | +1-415-990-2026 |
| LinkedIn | jianhong-chen-9285jc |
| Total experience | ~6 years (May 2020 – June 2026). Do not inflate. |
| Senior since | April 2023 (promotion at Medidata) |
| Current status | Mindray role ended June 2026; focused US job search since |
| Target | Clinical / healthcare applied DS first; also supply chain, forecasting, simulation/OR, applied LLM roles |

**Say:** "About 6 years in data science and statistics, senior since 2023."
**Never say:** "6+ years as a senior data scientist."

## 2. Positioning (strongest differentiators)

1. Clinical trial analytics at Medidata: rebuilt the KRI risk-scoring module (Poisson / negative binomial), productionized on AWS.
2. Survival analysis on longitudinal EHR data at the VA/UCSF, with 2 peer-reviewed publications.
3. Forecasting + stochastic simulation + constrained optimization, end to end, with backtested business impact.
4. Technical leadership: founded a DS team, hired and mentored, introduced agile practices in a traditional industry.
5. Practical LLM engineering: local inference on a self-managed GPU cluster, structured output validation, NL-to-SQL.

## 3. Skills (verified)

### Technical

| Area | Verified skills |
|---|---|
| Languages | Python, SQL, R; uses Claude Code daily |
| Statistics | Survival analysis (Cox PH, Kaplan–Meier), Poisson and negative binomial modeling, chi-square and exact tests, mixed-effects models, OLS with confounder adjustment and collinearity checks, power calculations (light), statistical inference (not causal estimation) |
| Dimensionality reduction | PCA, UMAP, t-SNE (used frequently at the VA and Medidata) |
| ML | XGBoost, LightGBM, Random Forest, anomaly detection, scikit-learn; clustering (K-means, density-based, hierarchical: studied in grad school; used at work for proofs of concept and prototypes) |
| Forecasting | ARIMA, Prophet, LSTM (PyTorch, package baseline model) |
| Simulation & optimization | Stochastic discrete-event simulation, Monte Carlo methods, constrained optimization, grid search over policy parameters, SciPy |
| LLM & agentic | Local LLM serving (vLLM, Ollama), Qwen-2.5-Coder-72B, Anthropic Claude via AWS, prompt engineering, Pydantic output validation, agentic code review; RAG with Chroma (prototype only) |
| Data & engineering | pandas, NumPy, statsmodels, Jupyter, FastAPI, Streamlit, Docker, Git, CI/CD, Linux, uv (Mindray and recent projects), basic ETL design (Mindray), unit and data testing |
| Data platforms & cloud | Snowflake, MySQL; AWS EC2, S3, Step Functions (Medidata: maintained existing pipelines regularly, did not create them) |
| Visualization | ggplot2 (R), Matplotlib, Seaborn, Plotly |
| Healthcare data | Longitudinal EHR, ICD-9 and ICD-10 coding, clinical trial operational data, clinical-form data; HIPAA with de-identified data |
| Self-directed only | Mixed-integer programming (PPC project, Section 6). Skills row only; never in a job bullet; disclose as self-directed if asked. |

### Leadership and soft skills (stated by JC)

- **Team building:** founded Mindray's first data science team; hiring manager for 2 data scientists; technical mentoring, 1:1 pair coding, and technical interview design for DS roles; code review.
- **Stakeholder management:** ~2 years as an internal consultant to supply chain and operations; translated ambiguous business logic into data-driven systems and projects; presented ML results and roadmap to non-technical colleagues and executive leadership.
- **Agile leadership:** introduced agile workflow to a traditional industry; guided the team's first agile project manager / scrum master; ran sprint planning and demos to keep work transparent.

### Spoken languages

English (professional), Mandarin (professional), Cantonese (native).

---

## 4. Experience

### 4.1 Mindray — Senior Data Scientist & Tech Lead

- **Dates:** 2024-06 to 2026-06 · **Location:** Shenzhen, China (always; never "Remote, Bay Area")
- **Company:** large medical device manufacturer.

**Verified facts**

- Founded the data science team from scratch and drove Mindray's first ML transformation; established agile development practices.
- Hiring manager for 2 data scientists (direct reports). The third team member was a PM, not a report. "3-person team" means these three.
- Defined the enterprise ML roadmap; internal consultant to supply chain / operations (~2 years). No formal consulting or agency employment.
- Stochastic discrete-event simulation framework, built end to end (see Project 6.1).
- Demand forecasting for 4,000+ SKUs with ARIMA, Prophet, and LSTM; tracked forecast accuracy over time. No formal drift monitoring tooling.
- Streamlit decision-support tools for planners.
- Local agentic PR-review system (see Project 6.2).
- Prototyped RAG and embedding-based data schema matching with a Chroma vector store for internal use. Never finished or productionized.
- Worked under HIPAA with de-identified data in approved environments.

**Metrics and their basis**

| Metric | Status | Basis |
|---|---|---|
| $200K (15%) S&OP cost reduction | Backtest | Simulated policy vs. historical plans. Always say "projected" / "in backtesting." |
| Service level 85% → 93% | Backtest | From the combined system (forecasts feeding the simulation and planning policy), not forecasting alone. |
| Planning cycle ~3 days → ~3 hours | True, conservative | One planner used to build the monthly plan in Excel over ~3 days with overtime. The framework produces the full report in ~3 minutes; ~3 hours includes planner review and sign-off. |
| PR review time ~80% less | Informal estimate with basis | Reviewers read the agent's structured review instead of reading through every change themselves. Use with "~". |

**Approved resume bullets**

- Founded and led a 3-person data science team, defining the enterprise ML roadmap and translating ambiguous supply chain constraints into AI product strategy for executive leadership.
- Engineered a stochastic discrete-event simulation framework in Python and Docker to model inventory uncertainty, cutting projected S&OP costs by $200K (15%) in backtesting.
- Forecasted demand for 4,000+ SKUs with ARIMA, Prophet, and LSTM, powering an end-to-end planning system that raised backtested service levels from 85% to 93%.
- Developed Streamlit decision-support apps operationalizing simulation and forecasting outputs for planners, replacing a ~3-day manual Excel planning process with a ~3-hour review cycle.
- Architected and deployed an on-prem agentic code-review system using Qwen-2.5-Coder-72B and vLLM on a 4× NVIDIA L20 cluster, cutting manual PR review time by ~80%.

**Never say:** live A/B tests or randomized products in production (A/B tests were simulation-based only; see 6.1); realized or measured savings; service-level gain from forecasting alone; MILP or mixed-integer programming at Mindray; Bayesian optimization (planned, never done); a finished or production RAG system.

### 4.2 Medidata Solutions — Senior Data Scientist (Promoted from Data Scientist)

- **Dates:** 2021-11 to 2024-05 · Data Scientist Nov 2021 – Apr 2023; Senior Data Scientist Apr 2023 – May 2024
- **Location:** Remote (Bay Area, CA)
- **Resume title format:** `Senior Data Scientist (Promoted from Data Scientist)` (no arrows; they render badly)

**Verified facts**

- **R → Python refactor:** led a 3-person team refactoring roughly 10–30 legacy R production scripts ("spaghetti" code) into modular Python, before AI coding tools were capable. Unit tests rewritten in Python; coverage went from ~70% to ~85%. Before: ~3–5 small bugs a week (~1 hour each) or an occasional major bug taking at least half a day; after: most fixes under an hour. Preprocessing got faster after removing unnecessary steps, but runtime was not measured.
- **KRI risk-scoring module (see Project 6.4):** rebuilt with Poisson / negative binomial models on daily-refreshed Snowflake clinical trial data; data-quality and missingness checks; chi-square / exact tests to root-cause shifts; productionized on AWS.
- **Duplicate patient flagging:** matched age, weight, and location to flag potential duplicate patients enrolled across trials. Flagging only; not used to rank reviews. Keep counts off the resume.
- **LightGBM site-selection classifiers:** inherited an existing model; improved workflow logic and engineered features; started the retrain but left before it was finished. Did not choose the label or metric.
- **NL-to-SQL assistant (see Project 6.3):** co-developed a prototype on AWS using an early Anthropic Claude model and prompt engineering. No fine-tuning.
- **AWS:** regularly maintained existing EC2, S3, and Step Functions pipelines (did not create them).
- Used PCA, UMAP, and t-SNE frequently.
- Clustering; mentoring; code review; HIPAA with de-identified data.

**Metrics and their basis**

| Metric | Status | Basis |
|---|---|---|
| Test coverage ~70% → ~85% | Recalled | From the refactor. |
| Major bug fix: half a day → under an hour | Recalled | From the refactor. |
| Hallucinated queries ~10% lower | Informal estimate | Relative reduction vs. the previous prompt version, estimated from one product partner's labels; no formal definition, golden set, or inter-rater agreement. |
| ~~25% faster execution~~ | Retired | Runtime was never measured. |
| ~~13% better risk detection~~ | Retired | No ground truth existed. Never use. |
| ~~6% lower operational latency~~ | Retired | No defined measure. Never use. |

**Approved resume bullets**

- Directed a 3-person team refactoring legacy R production code into modular Python, raising unit-test coverage from ~70% to ~85% and cutting major bug fixes from half a day to under an hour.
- Rebuilt the clinical trial risk-scoring module, engineering site-level Key Risk Indicators with Poisson and negative binomial models on daily Snowflake data; productionized on AWS.
- Improved workflow logic and engineered features for LightGBM site-selection classifiers, laying the groundwork for a model retrain to support global trial resource allocation.
- Co-developed a natural-language-to-SQL assistant prototype on AWS with Anthropic Claude models and prompt engineering, reducing hallucinated queries by ~10% in human-reviewed testing.

**Never say:** "built" the LightGBM models or a finished retrain; "forecasted site performance"; LLM fine-tuning; that the NL-to-SQL assistant reached production (unknown; it was a prototype when JC left); rigorous LLM evaluation, kappa, or golden sets; creating the AWS pipelines; CDISC/SDTM/ADaM or SAS work.

### 4.3 NCIRE | US Dept. of Veterans Affairs | UCSF — Statistician

- **Dates:** 2020-05 to 2021-11 · **Location:** Remote (Bay Area, CA)

**Verified facts**

- Lead data analyst / statistician for the COPD project; trials and experiments were run by other team members.
- Prototyped Random Forest and XGBoost models for some of the data modeling; these results were not published.
- Used PCA, UMAP, and t-SNE frequently.
- COPD progression analysis on longitudinal EHR data: Cox proportional hazards, Kaplan–Meier, mixed-effects models (one analysis), OLS with confounder adjustment and collinearity checks. Statistical inference, not causal estimation.
- Used both ICD-9 and ICD-10 codes for cohort and outcome definitions.
- Helped (a little) define COPD cohorts: inclusion/exclusion criteria and outcomes.
- Consulted (a little) on analysis plans, endpoints, and power calculations.
- Co-author and primary contributor on 2 peer-reviewed publications; publication figures made in R with ggplot2; constant data visualization work.
- Automated data ingestion: replaced file-by-file Excel reading (each file with QC checks and light preprocessing) with automated ingestion into MySQL so analyses query the database directly.

**Approved resume bullets**

- Quantified COPD disease progression risk with survival analysis and regression on longitudinal EHR data, contributing to 2 peer-reviewed publications on critical clinical features.
- Automated file-by-file Excel ingestion and QC into a MySQL database, replacing manual per-file loading with direct SQL queries and removing a key data bottleneck for COPD research.

**Never say:** "500x pipeline capacity" (rough estimate only); causal inference; that he ran the trials or experiments; that tree-based / ensemble models were part of the published work (they were unpublished prototypes). "Led the statistical analysis" is fine.

---

## 5. Education

| Degree | Field | School | Completed |
|---|---|---|---|
| MS | Applied Mathematics and Statistics | University of California, Santa Cruz | 2019-12 |
| BS | Applied Physics (Minor in Electrical Engineering) | University of California, Santa Cruz | 2016-03 |

No PhD. Gap Dec 2019 – May 2020 (after MS, COVID onset).

---

## 6. Projects

### 6.1 Stochastic Discrete-Event Simulation Framework (Mindray)

- **Dates:** 2025-01 to 2026-06 · **Role:** tech lead and founding developer, end to end
- **What it does:** models inventory and demand uncertainty to choose planning policies for medical device product lines (including Immune and Biochem lines).
- **Architecture:** SQL + Python ETL → Python simulation engine, Docker-deployed on a local server; Streamlit front end; ETL scheduled with Linux cron.
- **Model logic:** historical inventory, demand forecasts, product life cycle, and shelf life; volume loss, lead time, and expiration logic (framework v1.4.0).
- **Optimization:** constraints on max daily production capacity, lead time, budget, and storage capacity; weighted objective combining several service-level measures and total cost; grid search over policy parameters (Bayesian optimization was planned and ticketed but never done); Monte Carlo runs for robustness testing only; simulation-based A/B tests of policies.
- **Live A/B test:** JC pushed hard for a live A/B test, but stakeholders declined, seeing it as a waste of time. None was run. (Useful interview story about advocating for rigor.)
- **Results (backtest):** $200K (15%) projected S&OP cost reduction; service level 85% → 93% with the forecasting system. Planning cycle ~3 days → ~3 hours (true).
- **Stakeholders:** the operations director (two levels up) and his non-technical team initially preferred the manual process; trust was earned by checking every assumption and business rule with them and showing backtest results.
- **Time to confirm impact:** ~3 months, using Monte Carlo stress tests plus monthly forecast-accuracy and service-level tracking.

### 6.2 Local Agentic Code-Review System (Mindray)

- **Dates:** 2026-01 to 2026-06 · **Role:** sole developer, end to end
- **Architecture:** vLLM serving Qwen-2.5-Coder-72B on a self-managed 4× NVIDIA L20 server (504 GB RAM); FastAPI service; Pydantic to enforce and validate structured output; Docker; connected to a locally hosted Gitea through webhooks.
- **Model selection:** compared a few candidate models before choosing Qwen-2.5-Coder-72B.
- **Why local:** code stays on-premises.
- **Impact:** ~80% less manual review time (informal estimate). Basis: reviewers read the agent's structured review instead of reading every change line by line.

### 6.3 NL-to-SQL AI Assistant (Medidata)

- **Dates:** 2024-01 to 2024-05 · **Role:** one of two backend/algorithm developers; owned prompt engineering and result evaluation
- **Stack:** an early Anthropic Claude model (Sonnet or Haiku generation) through AWS, chosen for company privacy integration; prompt engineering only, no fine-tuning.
- **Status:** prototype when JC left in May 2024; whether it reached production is unknown.
- **Evaluation:** informal; outputs labeled correct or hallucinated by one product partner. ~10% fewer hallucinated queries in early testing.

### 6.4 Clinical Trial KRI / Adverse-Event Rate Modeling (Medidata)

- **Dates:** 2022-03 to 2023-05 · **Role:** sole backend/algorithm developer, from modeling through production
- **Method:** site-level counts (e.g., adverse events) modeled with Poisson; checked overdispersion and used negative binomial when needed; confidence intervals on rates; exact / chi-square tests to judge whether a shift was real or noise; data-quality and missingness checks.
- **Data and deployment:** daily-refreshed Snowflake data; productionized on AWS.
- **Impact:** no validated performance metric. Describe the rebuild, not an accuracy number.

### 6.5 Amazon PPC Ads Auditor and Budget Optimizer (self-directed)

- **Dates:** recent (as of Oct 2026; exact dates not recorded) · **Role:** independent developer
- **What it does:** analyzes Amazon PPC advertising data to find zero-converting search terms, map buyer intent, and detect search-term cannibalization and structural waste across ad structures.
- **Optimization:** mixed-integer programming / constrained optimization to allocate ad budget and CPC for better ad-spend ROI.
- **Disclosure:** self-directed project, not employment. The only place mixed-integer programming was used.

---

## 7. Confirmed gaps (never claim)

- PhD, MD, clinical licensure, security clearance
- SAS; CDISC / SDTM / ADaM (aware only); regulatory submission work
- Client-facing / forward-deployed / external customer work; startup employment
- MLflow, SageMaker, dbt, Databricks, Hex, Spark/PySpark, Airflow/Prefect/Temporal, Tableau/Looker
- Live A/B tests on users or operations; quasi-experimental methods (DiD, IV, PSM, RD, synthetic control) — conceptual only (studied DiD/PSM for interview prep)
- FHIR / HL7; claims or RCM data; event-stream / product analytics
- Formal LLM eval harness, LLM-as-judge, golden datasets, inter-rater agreement
- Building a supervised ML model from scratch (label/metric selection); finishing the Medidata LightGBM retrain
- Production-measured Mindray cost or service-level results
- Measured PR-review time savings, R→Python runtime gain, or MySQL ingestion speedup
- A measured KRI detection-accuracy improvement
- Mixed-integer programming in any job
- LLM fine-tuning (any model)
- Bayesian optimization (planned, not done)
- A finished or production RAG system; agentic AI orchestration frameworks
- C++; Postgres; SAP
- Creating (vs. maintaining) AWS EC2 / S3 / Step Functions pipelines

---

## 8. Reusable answers

| Question | Answer |
|---|---|
| HIPAA | Worked under HIPAA at Medidata and Mindray; all data de-identified; EDA and training only in approved environments. |
| Consulting | No formal consulting or agency work; ~2 years in an internal-consultant role at Mindray (Jun 2024 – Jun 2026). |
| Employment gap | Mindray role ended June 2026; focused US job search since. Minor gap Dec 2019 – May 2020 (after MS, COVID onset). |
| Why clinical / healthcare | Started in clinical data (VA COPD research, Medidata KRIs); Mindray added operations and stakeholder experience inside a medical device company; returning to clinical deliberately. |
| Coolest thing built | Mindray simulation framework: tunable parameters at critical steps, grid search + Monte Carlo, weighted service/cost objective, simulation-based A/B tests, $200K (15%) projected savings in backtesting. |
| Longest wait to know a change worked | ~3 months for the Mindray simulation-driven policy, with Monte Carlo stress tests and monthly forecast-accuracy / service-level tracking meanwhile. |
| Panel / longitudinal data | Yes (longitudinal patient EHR data). Transaction data: no. |
| Planning cycle | "A planner used to spend about 3 days, with overtime, building the monthly plan in Excel. The framework generates the full report in about 3 minutes; we budget about 3 hours so planners can review and sign off." |
| R → Python refactor | "The R code was hard to maintain: a few small bugs a week, and the occasional big one took half a day to trace. We refactored it into modular, tested Python, raised coverage from about 70% to 85%, and most fixes after that took under an hour." |
| KRI accuracy (on older resumes) | "I'd put less weight on that number. We never had a validated ground truth for site risk. What I stand behind is the rebuild: Poisson and negative binomial scoring on daily data, in production on AWS." |
| Causal inference | "I've applied statistical inference with confounder adjustment; I know DiD and PSM conceptually but haven't run them on production data." |

---

## 9. Caveats on resumes already sent

- Before 2026-10-19: Mindray was listed as "Remote (Bay Area, CA)." Correct location is Shenzhen, China.
- Before 2026-10-25: resumes included the 13% KRI figure, the 6% LightGBM latency, the 25% R→Python speedup, and 500x MySQL capacity; stated Mindray metrics without "backtest"; and implied a finished LightGBM retrain.
- If asked, correct it plainly and briefly; don't defend the old number.

---

## 10. Resume formatting rules

- 11 bullets: 5 Mindray, 4 Medidata, 2 NCIRE; each ≤ ~190 characters (2 rendered lines).
- Summary: full 3 lines, ~290–320 characters.
- Skills: max 5 rows, each label + details ≤ ~95 characters.
- Don't bold a keyword that also appears in a skills label.
- Skip obvious tech terms unless the JD names them (no "pull requests" under Git).
- Vary bullet verbs; avoid repeating "Built."
- RenderCV v2.3, theme sb2nov, us-letter, 0.8cm margins; `design` and `settings` at top level.
- Cover letters delivered as a one-page PDF.

---

## 11. Not yet verified

Nothing open as of 2026-10-25. Add new unconfirmed claims here before using them anywhere.

Resolved on 2026-10-25: live A/B tests (none; stakeholders declined), Bayesian optimization (planned only), Monte Carlo (robustness only), VA role (lead analyst/statistician), VA Random Forest / XGBoost (unpublished prototypes), fine-tuning (none; prompt engineering), PCA/UMAP/t-SNE and clustering, AWS EC2/S3/Step Functions, uv, basic ETL, Postgres (no), SAP (no), C++ (no), RAG (unfinished prototype), agentic orchestration (no), ~80% PR-review basis, NL-to-SQL model, status, and ~10% (relative, estimated).