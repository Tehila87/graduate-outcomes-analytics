# Graduate Outcomes Analytics
**Unemployment among Mathematical & Physical Sciences graduates**

*Cohorts 2021–22 & 2022–23 · Experimental analysis of anonymised GOS data*

### Overview

This repository presents an exploratory analysis of graduate employment outcomes among Mathematical & Physical Sciences graduates, with a particular focus on unemployment patterns across fields of study and demographic groups. Using anonymised Graduate Outcomes Survey (GOS) data for the 2021–22 and 2022–23 cohorts, the project examines structural unemployment risks and highlights potential intervention points relevant to higher education policy, curriculum design, and industry engagement.

The analysis is designed to surface directional signals and risk concentrations, rather than to reproduce official Graduate Outcomes statistics or support causal inference. It demonstrates a governance-aware analytical workflow, careful disclosure control, and the ability to translate complex data into decision-relevant insights.

> **Note**: While the underlying data cannot be shared, the notebook and codebase are published as a **reproducible analytical template** and methodological reference that can be applied to real-world GOS data by institutions, researchers, or policy teams.

### Data and Coverage

The analysis draws on three de-identified datasets derived from institutional Higher Education (HE) administrative data and the Graduate Outcomes Survey (GOS). The data covers approximately **3,700 Mathematical & Physical Sciences graduates from the 2021–22 and 2022–23 cohorts**, of whom approximately one third participated in the Graduate Outcomes Survey (15 months after graduation).

To enable public sharing while preserving analytical validity and confidentiality, the original datasets were processed through a controlled anonymisation and privacy-protection workflow and **expanded into a semi-synthetic analytical dataset comprising 4,812 graduates**. Consistent with the original data, across both cohorts in the anonymised dataset, **approximately 32% of graduates have known employment outcomes** - yielding an effective analytical base of around **1,560 respondents**.

### Methods Summary

This project applies a multi-stage, governance-aware analytical workflow. Original identifiers were replaced with stable, keyed anonymised IDs to preserve cross-dataset linkability without exposing personal data. Datasets were then synthetically expanded using controlled bootstrap-based resampling, combined with limited stochastic perturbation applied only to selected, eligible non-outcome variables. This approach preserves empirical distributions and analytical signal while reducing disclosure risk.

All analyses are exploratory and diagnostic in nature. **Subgroup-based visualisations apply a fixed minimum threshold of n ≥ 40 respondents with known outcomes** to ensure interpretability, analytical stability, and responsible disclosure. Suppressed categories and excluded respondents are explicitly documented for transparency. The full pipeline is reusable and can be applied directly to real-world GOS data (with anonymisation steps omitted where appropriate), subject to adequate sample-size and event-count considerations.

A more detailed methodological and governance discussion is provided in the notebook and accompanying presentation slides.

### Analytical Scope

The analysis addresses outcome-focused questions such as:
* Unemployment rates by cohort, department, and gender
* Year-on-year changes in unemployment patterns
* Gendered differences in unemployment risk across departments
* Graduate destinations by industry sector
* Diversity and inclusion indicators within Mathematical & Physical Sciences

Reusable, parameterised functions are used to compute rates, generate ranked summaries, and produce consistent visualisations across subgroups.

Following the question-led analysis, the notebook includes:
* A focused set of visualisations on unemployment risk and trends
* A complementary diversity snapshot covering gender and ethnicity composition

### Key Insights (High-Level)

At a high level, the analysis highlights:
* Meaningful variation in unemployment rates across subject areas and cohorts
* Pronounced gender gaps in unemployment within specific disciplines
* Concentrations of unemployment risk among certain graduate groups
* Structural under-representation of women and minority groups in some of the most resilient, high-demand fields

These patterns are used to motivate **testable hypotheses** and practical considerations for curriculum design, early-career pathways, and academia–industry collaboration.

### Risks and Limitations

This project explicitly documents risks and limitations throughout the notebook. Key constraints include:
* **Sample size and sparsity**: Effective sample sizes shrink rapidly under disaggregation; unemployment is a low-frequency outcome in many subgroups.
* **Response rate**: Survey response rates declined from approximately 37% in 2021–22 to 28% in 2022–23, limiting generalisability and raising the risk of under-representation of minority groups.
* **Feature coverage**: Available variables constrain interpretive depth and limit the ability to identify causal drivers of outcomes.
* **Structural factors**: Graduate employment outcomes are shaped by macroeconomic conditions, sectoral hiring cycles, and institutional practices that are only partially observable in survey data.

Accordingly, all findings should be interpreted as **exploratory and hypothesis-generating**, rather than as definitive evidence for operational or policy decisions.

### Reproducibility and Reuse

The analytical pipeline is designed for transparency, reproducibility, and reuse. Researchers or institutions with access to complete Graduate Outcomes datasets can apply and extend this workflow to generate robust, unbiased, and policy-relevant evidence, subject to appropriate governance and disclosure controls.

The repository demonstrates:
* Responsible handling of sensitive individual-level data
* Explicit documentation of analytical choices and thresholds
* Clear separation between exploratory insights and evidentiary claims

### Repository Structure
* `notebooks/` – Main analysis notebook with full methodology, code, and documentation
* `figures/` – Exported visualisations used in presentation decks
* `slides/` – Summary presentation decks (intro, unemployment analysis, diversity snapshot, methods & governance)


### Author
**Tehila Sharabi**
Data Analyst & Researcher
GitHub: https://github.com/Tehila87



