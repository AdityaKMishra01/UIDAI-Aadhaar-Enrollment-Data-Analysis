# UIDAI Aadhaar Enrollment Data Analysis

![Dashboard Preview](images/dashboard_preview.png)

## 📊 Project Overview

This project analyzes **Aadhaar enrolment patterns across India** using aggregated UIDAI Aadhaar enrolment data and presents the results through an interactive **Power BI dashboard**.

The analysis focuses on:

- State-level enrolment distribution
- District-level enrolment concentration
- Age-group enrolment patterns
- Monthly enrolment trends
- Geographic variation in Aadhaar enrolment
- High-volume states and districts
- Dashboard-level KPIs for quick exploration

The project was developed as part of the **UIDAI Data Hackathon 2026** and is intended to demonstrate practical skills in data cleaning, exploratory analysis, data modeling, visualization, and business-style dashboard development.

> **Data note:** The dashboard uses aggregated/anonymised Aadhaar data. No individual Aadhaar numbers or personally identifiable individual-level records are used in this analysis.

---

## 🎯 Objectives

1. Understand the geographic distribution of Aadhaar enrolments across India.
2. Compare enrolment volumes across states and districts.
3. Analyze enrolment by age group.
4. Identify monthly trends and changes in enrolment activity.
5. Build an interactive Power BI dashboard for exploratory analysis.
6. Convert raw data into concise, decision-oriented insights.

---

## 🗂️ Dataset

The project uses Aadhaar enrolment data made available for the UIDAI Data Hackathon 2026.

The official hackathon information describes the available datasets as aggregated/anonymised Aadhaar enrolment and update data, including enrolment information by date, state, district, PIN code, and age groups.  
Source: [UIDAI Data Hackathon 2026](https://event.data.gov.in/challenge/uidai-data-hackathon-2026/)

### Main enrolment fields

| Field | Description |
|---|---|
| `date` | Date/month associated with the enrolment record |
| `state` | State/UT associated with the record |
| `district` | District associated with the record |
| `pincode` | PIN code associated with the record |
| `age_0_5` | Enrolments for children aged 0–5 |
| `age_5_17` | Enrolments for ages 5–17 |
| `age_18_plus` | Enrolments for ages 18+ |

### Data availability

The raw source files are not reproduced in this repository by default. If the source files are large, download them from the official UIDAI/Data.gov.in hackathon source and place them in the local `data/raw/` directory.

This keeps the GitHub repository lightweight and avoids unnecessarily committing large source datasets.

---

## 📈 Dashboard KPIs

The current dashboard snapshot reports:

| KPI | Dashboard Value |
|---|---:|
| Total Enrolment | **54,35,702** |
| States | **49** |
| Districts | **965** |

### Age-group distribution shown in the dashboard

| Age Group | Enrolment | Share |
|---|---:|---:|
| 0–5 | 35,46,965 | 65% |
| 5–17 | 17,20,384 | 32% |
| 18+ | 1,68,353 | 3% |

These values are the **dashboard's aggregated enrolment measures**, not the number of source rows.

---

## 🔎 Key Dashboard Insights

### 1. State-level concentration

The dashboard shows substantial variation in enrolment volume across states. **Uttar Pradesh and Bihar** appear among the highest-volume states in the displayed analysis.

### 2. District-level concentration

The district chart highlights several high-volume districts, including:

- Thane
- Sitamarhi
- Bahraich
- Murshidabad
- South 24 Parganas
- Pune
- Jaipur
- Bengaluru
- Sitapur
- Hyderabad

These are observations from the displayed dashboard and should be interpreted within the dataset's geographic and temporal coverage.

### 3. Age-group pattern

The largest share of enrolment shown in the dashboard comes from the **0–5 age group (65%)**, followed by **5–17 (32%)** and **18+ (3%)**.

This indicates that, within the analyzed data, child enrolment contributes a substantial portion of total enrolment activity.

### 4. Monthly trend

The monthly trend chart shows visible variation in enrolment activity across the displayed months, with higher activity in some months and a noticeable decline in others.

The dashboard can be filtered by state to investigate whether these patterns differ geographically.

---

## 🛠️ Tools & Technologies

- **Power BI** — Data modeling, DAX measures, interactive dashboard
- **Microsoft Excel / CSV** — Source data inspection and preparation
- **Power Query** — Data transformation and cleaning
- **DAX** — KPI calculations and analytical measures
- **Git & GitHub** — Version control and project documentation

---

## 🧩 Dashboard Features

The Power BI dashboard includes:

- KPI cards
- State filter
- State-wise enrolment bar chart
- District-wise enrolment bar chart
- Age-group distribution pie chart
- Monthly enrolment trend
- Interactive filtering
- Executive-style insights panel

---

## 🔄 Analysis Workflow

```text
UIDAI / Data.gov.in Dataset
            ↓
      Data Import
            ↓
   Data Cleaning & Validation
            ↓
     Data Transformation
            ↓
      Data Modeling
            ↓
      DAX Calculations
            ↓
   Interactive Power BI Report
            ↓
    Insights & Interpretation
```

---

## 📁 Recommended Repository Structure

```text
UIDAI-Aadhaar-Enrollment-Analysis/
│
├── README.md
│
├── dashboard/
│   └── UIDAI_Aadhaar_Enrollment_Dashboard.pbix
│
├── data/
│   ├── raw/
│   │   └── README.md
│   └── processed/
│       └── README.md
│
├── docs/
│   ├── DATA_DICTIONARY.md
│   ├── METHODOLOGY.md
│   └── INSIGHTS.md
│
├── images/
│   └── dashboard_preview.png
│
├── notebooks/
│   └── analysis.ipynb
│
└── .gitignore
```

> Keep large raw CSV/Excel files out of GitHub unless you have a specific reason to publish them. GitHub recommends good repository hygiene and README documentation for making projects understandable and maintainable.

---

## ▶️ How to Use

### Option 1 — View the dashboard

1. Download the `.pbix` file from the `dashboard/` directory.
2. Open it using **Microsoft Power BI Desktop**.
3. If the data source paths are local, update them in **Power Query**.
4. Refresh the model.
5. Use the state filter and visuals to explore the data.

### Option 2 — Reproduce the analysis

1. Obtain the official UIDAI hackathon dataset.
2. Place the source files in `data/raw/`.
3. Perform the transformations described in `docs/METHODOLOGY.md`.
4. Load the processed data into Power BI.
5. Recreate or refresh the measures and visuals.

---

## 📊 Suggested DAX Measures

Example measures used for dashboard-style analysis:

```DAX
Total Enrolment =
SUM(Enrolment[Total_Enrolment])

Total States =
DISTINCTCOUNT(Enrolment[State])

Total Districts =
DISTINCTCOUNT(Enrolment[District])

Age 0-5 =
SUM(Enrolment[Age_0_5])

Age 5-17 =
SUM(Enrolment[Age_5_17])

Age 18+ =
SUM(Enrolment[Age_18_plus])
```

If your actual Power BI table/column names are different, replace the names accordingly.

---

## ⚠️ Data & Interpretation Notes

- The dashboard presents **aggregated/anonymised data**.
- Dashboard totals represent the selected dataset/filter context and should not automatically be interpreted as India's complete Aadhaar population.
- A high enrolment count in a state or district does not, by itself, establish the reason for that difference.
- Monthly fluctuations should be interpreted in the context of the dataset's coverage and collection structure.
- The age-group percentages shown above are based on the dashboard snapshot provided with this repository.

---

## 📚 Documentation

Detailed project documentation is available in:

- [`DATA_DICTIONARY.md`](docs/DATA_DICTIONARY.md) — Dataset fields and definitions
- [`METHODOLOGY.md`](docs/METHODOLOGY.md) — Cleaning, transformation, modeling and dashboard methodology
- [`INSIGHTS.md`](docs/INSIGHTS.md) — Dashboard findings and interpretation
- [`data/raw/README.md`](data/raw/README.md) — Instructions for handling raw source files

---

## 🏛️ Data Source

The project is based on data provided for the **UIDAI Data Hackathon 2026**, organised by the Unique Identification Authority of India (UIDAI) in association with the National Informatics Centre (NIC), Ministry of Electronics and Information Technology (MeitY).

Official sources:

- [UIDAI](https://uidai.gov.in/)
- [UIDAI Data Hackathon 2026 – Data.gov.in](https://event.data.gov.in/challenge/uidai-data-hackathon-2026/)
- [UIDAI Hackathon Information](https://event.data.gov.in/event/online-hackathon-on-data-driven-innovation-on-aadhaar-2026/)

---

## 👤 Author

**Aditya Kumar Mishra**

Data Analyst | Power BI | SQL | Python | Excel

### Skills Demonstrated

`Power BI` `DAX` `Power Query` `Excel` `Data Analysis` `Data Visualization` `Data Modeling` `SQL` `Python`

---

## 📄 License & Usage

This repository contains the author's analytical work, documentation, dashboard files, and visualisations.

The underlying UIDAI dataset remains subject to the terms and conditions applicable to the official data source/hackathon.

For reuse of the underlying data, refer to the official UIDAI/Data.gov.in source and applicable terms.

---

## ⭐ Project Goal

The goal of this project is to demonstrate an end-to-end **data analytics workflow**:

**Raw Data → Cleaning → Transformation → Modeling → Visualization → Insights**

If you find the project useful, feel free to explore the dashboard, review the methodology, and examine the analytical approach.

---

# Data Dictionary

# Data Dictionary

## Purpose

This document describes the fields used in the Aadhaar enrolment analysis.

> Column names can vary slightly depending on the source file and transformation step. Update this document if the final Power BI model uses different names.

| Field | Data Type | Description |
|---|---|---|
| `date` | Date | Date/month represented by the record |
| `state` | Text | State or Union Territory |
| `district` | Text | District associated with the record |
| `pincode` | Integer/Text | PIN code associated with the record |
| `age_0_5` | Integer | Number of enrolments for age group 0–5 |
| `age_5_17` | Integer | Number of enrolments for age group 5–17 |
| `age_18_plus` | Integer | Number of enrolments for age group 18+ |
| `total_enrolment` | Integer | Sum of enrolments across the three age groups |

## Derived Measures

### Total Enrolment

```text
Total Enrolment =
Age 0–5 + Age 5–17 + Age 18+
```

### Age-group share

```text
Age Group Share =
Age Group Enrolment / Total Enrolment
```

## Geographic Dimensions

The dashboard uses:

- State
- District
- PIN code, where available

These dimensions allow the analysis to move from national/state-level patterns to more granular geographic patterns.

---

# Methodology

# Methodology

## 1. Data Collection

The project uses aggregated/anonymised Aadhaar enrolment data supplied for the UIDAI Data Hackathon 2026.

The official hackathon documentation describes enrolment data across dimensions including date, state, district, PIN code and age groups.

## 2. Data Preparation

The preparation process should include:

1. Import source files.
2. Inspect column names and data types.
3. Standardise field names.
4. Convert date fields to a consistent date format.
5. Validate numeric enrolment columns.
6. Handle blank/null geographic values where applicable.
7. Check for duplicate records.
8. Validate age-group totals.
9. Create a total enrolment measure.
10. Load the cleaned data into Power BI.

## 3. Data Validation

Important checks:

- State count
- District count
- Missing states/districts
- Duplicate combinations of date + state + district + PIN code
- Negative enrolment values
- Null/invalid numeric values
- Total enrolment reconciliation

## 4. Power BI Data Model

The dashboard can use a simple analytical model consisting of:

```text
                 Date
                  │
                  ▼
State ───────► Enrolment ◄────── District
                  │
                  ▼
               Pincode
```

For a larger implementation, separate dimension tables can be introduced for Date, State, District and PIN code.

## 5. Measures

Typical measures include:

- Total Enrolment
- Total States
- Total Districts
- Age 0–5
- Age 5–17
- Age 18+
- Age-group percentage
- Monthly enrolment

## 6. Visualization

The dashboard uses:

- KPI cards for headline metrics
- Horizontal/vertical bar charts for geographic comparison
- A pie/donut chart for age-group composition
- A line chart for monthly trend
- A slicer for state-level filtering

## 7. Interpretation

The analysis is descriptive. It identifies patterns visible in the dataset but does not establish causal relationships.

For example, a state having a higher enrolment count does not by itself explain why the count is higher.

## 8. Reproducibility

To reproduce the dashboard:

1. Obtain the source dataset from the official source.
2. Place files under `data/raw/`.
3. Apply the documented cleaning steps.
4. Load the resulting data into Power BI.
5. Refresh the data model.
6. Validate headline totals against the documented dashboard snapshot.

---

# Dashboard Insights

# Dashboard Insights

## Executive Summary

The dashboard provides an overview of Aadhaar enrolment across states, districts, age groups and months.

### Headline metrics

- **Total enrolment:** 54,35,702
- **States represented:** 49
- **Districts represented:** 965

### Age distribution

The dashboard shows:

- **0–5 years:** 35,46,965 (65%)
- **5–17 years:** 17,20,384 (32%)
- **18+ years:** 1,68,353 (3%)

The 0–5 age group represents the largest share of the displayed enrolment total.

## Geographic Observations

The state chart shows a wide difference in enrolment volume between states. Uttar Pradesh and Bihar are among the highest-volume states visible in the dashboard.

The district chart highlights high-volume districts such as Thane, Sitamarhi, Bahraich, Murshidabad and South 24 Parganas.

## Time Trend

The monthly trend shows fluctuations in enrolment activity across the months represented in the dashboard.

The state slicer can be used to determine whether the overall trend is driven by a small number of states or is broadly distributed.

## Important Interpretation Limitation

These are descriptive observations from the dashboard. They should not be treated as causal explanations.

For example:

- Higher enrolment volume does not automatically mean higher enrolment demand per capita.
- A lower district count may reflect the dataset's coverage rather than lower Aadhaar activity.
- Monthly changes may be affected by data coverage, reporting patterns or operational factors.

Additional population-normalised and time-series analysis would be required for stronger conclusions.

---

# Raw Data Instructions

# Raw Data

Place the original UIDAI/Data.gov.in source files in this directory when reproducing the analysis.

Example:

```text
data/raw/
├── enrolment_*.csv
├── enrolment_*.xlsx
└── source_metadata.txt
```

## Recommended practice

Do not commit large raw source files to GitHub unless required.

Instead:

1. Download the data from the official UIDAI/Data.gov.in source.
2. Store the files locally under `data/raw/`.
3. Run the cleaning/transformation workflow.
4. Commit scripts, notebooks, documentation and small processed samples where appropriate.

The dashboard repository should document the source and reproducibility steps rather than silently relying on an unavailable local file path.
