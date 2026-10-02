[README.md](https://github.com/user-attachments/files/32938805/README.md)
# Player Performance Modeling

**Sports analytics portfolio · Boston College, M.S. Sports Analytics (Fall 2026)**
Andrés Garcia Damasco · [LinkedIn](https://www.linkedin.com/in/andres-garcia-damasco)

I build models that help sports staff make decisions, then explain them in plain language to the people who make those decisions. This repo collects my work from **Player Performance Modeling (ADSA 8035)**. It's a full injury-risk project on Premier League data, carried from raw data to a recommendation for a club's Head of Medical.

---

## Featured project: Should a club trust its injury-risk model?

**[→ Injury Risk Technical Report](./lab04-injury-report)**

A medical department has **four recovery beds** and wants a model to tell them which injured players will be out more than 30 days. I built the model, then tested whether it was actually good enough to use.

**What I found:**
- The model ranks players only slightly better than chance (**AUC 0.58**, 90% bootstrap CI 0.51–0.65), and it drops from 0.72 on training data.
- It loses to "predict nobody gets hurt long" on accuracy (57% vs 59%), and its probabilities are slightly worse than guessing the base rate (Brier 0.247 vs 0.242).
- Its top four names went **1 for 4**, inside the range you'd get picking players at random.
- Using a cost ratio I built (a missed long absence ≈ 8× a false alarm), the cheapest cutoff flags 146 of 152 players, which is useless with four beds.

**What I recommended:** don't let the list allocate beds. Keep it with medical staff as a second opinion, and never use it in selection or contract decisions.

**Why it matters:** the hard part of applied analytics isn't fitting a model. It's being able to prove when a model isn't ready, say how sure you are, and still give the decision-maker something they can act on.

---

## All projects

| Project | What I did | Key skills |
|---|---|---|
| [Exploratory analysis of Premier League injuries](./lab01-eda) | Profiled ~600 injuries, found and fixed inconsistent injury labels, audited missing data, compared recovery times by injury type | EDA, data cleaning, missing-data reasoning |
| [Injury-risk feature engineering](./lab02-features) | Built features like prior injuries, days since last injury, body region and recurrence; designed my own feature and stress-tested its threshold | Feature engineering, pandas, stability checks |
| [Logistic regression injury model](./lab03-model) | Built a preprocessing pipeline, translated coefficients into odds multipliers for coaches, produced a risk list, checked model assumptions | scikit-learn pipelines, interpretability |
| [Model evaluation & technical report](./lab04-injury-report) | ROC/AUC with bootstrap intervals, calibration, cost-based thresholds, top-k vs random baselines, paired-bootstrap test of a model change | Evaluation, uncertainty, decision analysis, stakeholder writing |

*More projects added as the course continues: model comparison, player archetypes, risk assessment brief and capstone.*

---

## Skills shown here

**Python:** pandas · NumPy · scikit-learn · matplotlib
**Modeling:** logistic regression · preprocessing pipelines · train/test discipline
**Evaluation:** precision & recall · ROC/AUC · calibration · Brier score · bootstrap confidence intervals · permutation baselines
**Decision-making:** cost-of-error analysis · threshold selection · fixed-capacity (top-k) decisions
**Communication:** reports and memos for medical and performance staff · limitations and ethics

## About me

I'm a performance analyst and opponent scout for **Boston College Women's Soccer** while finishing my M.S. in Sports Analytics. I've also worked on data-warehouse integration in pro soccer. My goal is to lead BI and analytics for a professional sports organization. I speak English, Spanish and Italian.

---

<sub>Datasets and stakeholder scenarios come from course case studies. Built with AI assistance for code and drafting; every analysis was run, checked and interpreted by me.</sub>
