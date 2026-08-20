# Heart-Disease-Risk-Dashboard---Santosh-Kori

# ❤️ Heart Risk Factor Dashboard

🔗 **Live demo:** https://jade-sentosa-yyyj.pagedrop.io/

An analytics dashboard exploring cardiovascular disease risk across a **9,000-patient** cohort.
This repository contains the source dataset and a PDF of the finished dashboard.

> ⚠️ **Disclaimer:** The dataset is synthetic / for demonstration and this project is for
> data-analysis and visualization purposes only. It is **not** medical advice or a diagnostic tool.

---

## 📦 What's in this repo

| File | Description |
|---|---|
| **`Heart Risk Factor Dashboard.pdf`** | The finished dashboard — screenshots of every page (Overview, Demographics & Age, Cardiac & Vitals, Lifestyle, Risk Scoring). |
| **`heart_disease_risk_2026.csv`** | The source dataset — 9,000 patient records, 27 columns. |

📄 **Start with the PDF** to see the dashboard, then explore the raw data in the CSV.

---

## ✨ Dashboard overview

A neon-themed, dark-mode dashboard organised into **5 pages**:

1. **Overview** — headline KPIs and disease prevalence by age, risk band, cholesterol, and smoking.
2. **Demographics & Age** — cohort makeup and prevalence by age × sex.
3. **Cardiac & Vitals** — blood pressure, HbA1c, cholesterol, and an animated risk-band scatter.
4. **Lifestyle** — how exercise, steps, sleep, and diet quality relate to risk.
5. **Risk Scoring** — a composite 10-factor risk model and its prevalence curve.

Bars are colour-scaled by prevalence (green = lower risk → magenta = higher risk) so patterns read
at a glance.

---

## 📊 The dataset

`heart_disease_risk_2026.csv` — 9,000 rows × 27 columns, one row per patient.

| Group | Fields |
|---|---|
| Demographics | `patient_id`, `age`, `sex` |
| Vitals | `resting_bp_systolic`, `resting_bp_diastolic`, `resting_heart_rate`, `max_heart_rate_achieved` |
| Lipids / metabolic | `cholesterol_total`, `hdl`, `ldl`, `triglycerides`, `fasting_blood_sugar`, `hba1c`, `bmi` |
| Cardiac | `chest_pain_type`, `exercise_induced_angina`, `st_depression` |
| Lifestyle | `smoker_status`, `alcohol_units_per_week`, `exercise_minutes_per_week`, `sleep_hours`, `stress_score`, `diet_quality_score` |
| Wearable | `wearable_owner`, `daily_steps` |
| History / target | `family_history`, `has_heart_disease` |

**Overall disease prevalence: 30.3%** (2,727 of 9,000 patients).

---

## 🧮 Risk model & derived categories

Categories use recognised clinical cut-offs — **BP** (ACC/AHA), **BMI** (WHO), **HbA1c** (ADA),
**cholesterol**, and **exercise** (WHO 150-min guideline) — plus age, sleep, steps, and diet bands.

A **Risk Factor Count (0–10)** sums ten flags: age ≥55, BP ≥130/80, cholesterol ≥240, HDL <40,
HbA1c ≥6.5, BMI ≥30, current smoker, family history, exercise-induced angina, and ST-depression ≥1.
It rolls up into a **Risk Band**: Low / Moderate / High / Very High.

---

## 🔎 Key findings

Prevalence rises cleanly with every risk dimension:

| Dimension | Gradient (disease prevalence) |
|---|---|
| **Risk Band** | Low **3.1%** → Moderate 11.1% → High 41.3% → Very High **79.3%** |
| **Risk Factor Count** | 0 factors **3.1%** → 4 factors 53.3% → 7 factors **95.8%** |
| **Age Group** | 18-34 **9.5%** → 75+ **57.4%** |
| **Smoking** | Never 25.2% → Former 30.3% → Current **46.4%** |
| **HbA1c** | Normal 20.7% → Prediabetes 33.7% → Diabetes **45.6%** |
| **Exercise** | Active 20.1% → Moderate 33.7% → Low **49.8%** |
| **Diet quality** | Excellent 20.7% → … → Poor **46.0%** |

The takeaway: risk is strongly **multi-factorial** — the composite Risk Band separates the cohort far
better than any single measure, from ~3% prevalence at the low end to ~79% at the high end.

---

## 🛠️ Built with

Power BI (data model + DAX measures) for the dashboard, with the visuals designed on a custom
neon theme. Data profiling and validation done in Python (pandas).

---

## 📄 License

Released under the MIT License. Dataset is synthetic and provided for demonstration only.

---

*Built as a data-visualization portfolio project. Feedback and suggestions welcome.*
