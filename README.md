# HealthConnect Clinic - Data Analytics Track

### AnalystLab Africa | Experience Lab Internship Programme

- **Prepared by:** Richard GNALOU
- **Role:** Junior Business Intelligence Analyst
- **Track:** Data Analytics
- **Current Phase:** Week 4 - Problem Understanding

---

## Project Overview

HealthConnect Clinic is a fictional healthcare provider facing several operational challenges: missed appointments, inefficient use of appointment slots, repetitive patient enquiries, and a general need to improve patient engagement.

### Central Project Question

> How can HealthConnect Clinic use data and AI to reduce missed appointments and improve the patient support experience?

This is a shared project across five internship tracks (Project Management, Data Analytics, Data Science, Machine Learning Engineering, Generative AI), each contributing from their professional angle. This repository covers the **Data Analytics** contribution.

---

## Data Analytics Track Scope

The Data Analytics track is responsible for exploring the appointment dataset to understand attendance patterns and no-show drivers, and for proposing business questions and KPIs that will guide the project's next phases (analysis, modelling, dashboarding).

---

## Repository Structurehealthconnect-week4/
├── README.md
├── data/
│ └── raw/
│ ├── HealthConnect_Appointment_Data.csv
│ └── HealthConnect_Data_Dictionary.xlsx
├── notebooks/
│ └── week4_initial_analysis.ipynb
├── reports/
│ ├── week4_initial_analysis_document.pdf
│ └── week4_project_summary.pdf
└── docs/
└── data_dictionary_notes.pdf

---

## Week 4 Deliverables

| Deliverable | Status |
|---|---|
| Dataset overview | Done |
| Data quality assessment (missing values, logical rules, cross-field consistency) | Done |
| Relevant business questions (5) | Done |
| Potential KPIs identified & justified (5) | Done |
| Initial analysis approach | Done |
| Assumptions, limitations, risks & dependencies | Done |
| Week 4 Project Summary | Done |
| Data Dictionary cross-check | Done |

---

## Key Findings (Week 4)

- **Overall no-show rate: 48.46%**, nearly one appointment in two is missed. Combined with cancellations, **53.72%** of scheduled capacity is not realised.
- **Strongest signal:** patients with a prior no-show history no-show again at **55.4%**, vs. **43.5%** for those without (11.9-point gap).
- **Reminders help moderately:** no-show rate drops from 51.4% (no reminder) to 47.4% (reminder sent); **SMS** is the most effective channel (45.75% no-show).
- **Booking lead time matters:** No-Shows book about 10 days further in advance on average than Attended appointments.
- **Weak signals:** distance to clinic and waiting time show little standalone relationship with attendance in this dataset.
- **Data quality:** dataset is clean and consistent with the data dictionary, with one flagged anomaly: 9 cases of the same patient having two appointment records at the same date/time slot.

Full detail and methodology are available in `reports/week4_initial_analysis_document.pdf` and `notebooks/week4_initial_analysis.ipynb`.

---

## Tools & Technologies

- **Python** (pandas, numpy) for data exploration and quality checks
- **Jupyter Notebook** for reproducible analysis
- **Markdown / PDF** for documentation

---

## How to Reproduce

```bash
git clone https://github.com/Ricardo1826/healthconnect-clinic-analytics.git
cd healthconnect-week4
pip install pandas numpy jupyter openpyxl
jupyter notebook notebooks/week4_initial_analysis.ipynb
```

---

## Proposed Focus for Week 5

- Formal statistical validation (correlation analysis / simple logistic regression) on the three strongest signals: prior no-show history, reminder status/channel, booking lead time.
- Segment-level visualisations of no-show and lost-capacity rates.
- Clarification of the duplicate-booking anomaly with the data source.
- Alignment with the Data Science track to avoid duplicated exploration.

---

## Notes

- Original project resources in `data/raw/` are kept untouched, per project guidelines.
- This analysis uses correlational observations only; no causal claims are made at this stage.
- The `HealthConnect_Clinic_Knowledge_Base.docx` resource is out of scope for this track (it is used by the Generative AI track).

---

*AnalystLab Africa – Data Analytics Internship Programme*