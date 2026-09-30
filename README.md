# UIDAI Data Hackathon 2026 — Aadhaar Enrollment Data Analysis

![UIDAI Aadhaar Enrollment Dashboard](<UIDAI data hackathon 2026.png>)

## 🏛️ Project

**UIDAI Data Hackathon 2026 — Aadhaar Enrollment Data Analysis & Power BI Dashboard**

This project was developed using the **Aadhaar enrolment dataset provided for the UIDAI Data Hackathon 2026**. The analysis focuses on identifying geographic, demographic, and temporal patterns in Aadhaar enrolment and presenting those findings through an interactive Power BI dashboard.

The official hackathon problem statement was **“Unlocking Societal Trends in Aadhaar Enrolment and Updates”**, with the objective of identifying meaningful patterns, trends, anomalies, or predictive indicators that could support informed decision-making and system improvements. citeturn0search0

---

## 🎯 Hackathon Problem Statement

### Unlocking Societal Trends in Aadhaar Enrolment and Updates

The UIDAI Data Hackathon 2026 provided participants with aggregated/anonymised Aadhaar datasets and invited them to derive meaningful analytical insights from enrolment and update activity.

This project focuses specifically on **Aadhaar Enrolment Data**.

The analysis examines:

- State-wise enrolment
- District-wise enrolment
- Age-group-wise enrolment
- Monthly enrolment trends
- Geographic concentration
- Demographic distribution
- Interactive filtering and exploration

The hackathon permitted analytical and visualization tools such as **Python, R, SQL, Excel, Tableau and Power BI**. citeturn0search0

---

## 📊 Project Objective

The primary objective of this project is to transform raw Aadhaar enrolment data into an interactive analytical dashboard that makes it easier to identify:

1. Geographic differences in enrolment activity.
2. Districts with comparatively high enrolment volumes.
3. Distribution of enrolments across age groups.
4. Monthly changes in enrolment activity.
5. Regional patterns that can be explored through interactive filters.

---

## 🗃️ Dataset

The analysis uses the **Aadhaar enrolment dataset provided for the UIDAI Data Hackathon 2026**.

The official Open Government Data platform describes Aadhaar enrolment data as monthly, age-group-wise and PIN-code-wise data across India. The available resource includes fields such as **Date, State, District, Pincode and Age_0_5**. citeturn0search5turn0search6

### Dataset dimensions used in this project

| Dimension | Description |
|---|---|
| Date | Month/date associated with the enrolment record |
| State | State/UT associated with the record |
| District | District associated with the record |
| Pincode | PIN code associated with the record |
| Age 0–5 | Enrolments for children aged 0–5 |
| Age 5–17 | Enrolments for ages 5–17 |
| Age 18+ | Enrolments for individuals aged 18+ |

> **Important:** The dataset is aggregated/anonymised. This project does not use individual Aadhaar numbers or personally identifiable individual-level records. UIDAI states that aggregated/anonymised Aadhaar datasets were provided for the hackathon. citeturn0search0

---

# 📌 Dashboard Overview

The Power BI dashboard provides an executive-style view of Aadhaar enrolment activity.

### Dashboard components

- Total Enrolment KPI
- State Count KPI
- District Count KPI
- State slicer
- State-wise enrolment
- District-wise enrolment
- Age-group distribution
- Monthly enrolment trend
- Analytical insights panel

---

## 📈 Key Dashboard Metrics

The current dashboard snapshot displays:

| KPI | Value |
|---|---:|
| Total Enrolment | **54,35,702** |
| States | **49** |
| Districts | **965** |

### Age-group distribution

| Age Group | Enrolment | Share |
|---|---:|---:|
| 0–5 | 35,46,965 | 65% |
| 5–17 | 17,20,384 | 32% |
| 18+ | 1,68,353 | 3% |

These values represent the aggregated measures shown in the dashboard snapshot.

---

# 🔍 Key Findings

## 1. State-wise enrolment concentration

The state-level visualization shows substantial variation in enrolment volumes across the states represented in the dataset.

In the displayed dashboard, **Uttar Pradesh and Bihar** are among the states with the highest enrolment volumes.

This is a descriptive observation from the analyzed dataset and should not by itself be interpreted as a measure of population-normalised Aadhaar coverage.

---

## 2. District-level enrolment

The dashboard highlights several districts with relatively high enrolment volumes, including:

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

The district-level chart enables users to compare enrolment volumes and investigate geographic concentration.

---

## 3. Age-group distribution

The largest share of enrolment shown in the dashboard belongs to the **0–5 age group**, representing approximately **65%** of the displayed total.

The other displayed groups are:

- 5–17: approximately 32%
- 18+: approximately 3%

This indicates that child enrolment constitutes a substantial portion of enrolment activity within the analyzed dataset.

---

## 4. Monthly trend

The monthly trend visualization shows fluctuations in enrolment activity over the months represented in the dataset.

The interactive state filter can be used to investigate whether monthly patterns vary across different regions.

---

# 🧠 Analytical Approach

The project follows an end-to-end data analytics workflow:

```text
UIDAI Aadhaar Dataset
        ↓
Data Collection
        ↓
Data Cleaning
        ↓
Data Validation
        ↓
Data Transformation
        ↓
Power BI Visualizations
        ↓
Pattern Identification
        ↓
Insights
```

---

# 🛠️ Tools & Technologies

### Data Analysis

- Microsoft Excel
- SQL
- Power Query

### Visualization & BI

- Microsoft Power BI

### Version Control

- Git
- GitHub

---

# 📊 Dashboard Design

The dashboard contains:

### KPI Cards

Provides a quick overview of:

- Total enrolments
- Number of states
- Number of districts

### State-wise Bar Chart

Used to compare total enrolment volume across states.

### District-wise Bar Chart

Used to identify districts with comparatively high enrolment volumes.

### Age-group Pie Chart

Shows the distribution of enrolments across:

- 0–5
- 5–17
- 18+

### Monthly Line Chart

Shows changes in enrolment activity over time.

### State Slicer

Allows users to filter the entire dashboard by state.

---

# ▶️ How to Run the Project

## 1. Download the Repository

Clone the repository
```

## 2. Obtain the Dataset

Use the official UIDAI/Data.gov.in source and place the required source files under:

```text
data/raw/
```

## 3. Open the Power BI Dashboard

Open:

```text
dashboard/UIDAI_Aadhaar_Enrollment_Dashboard.pbix
```

using **Microsoft Power BI Desktop**.

## 4. Update Data Source

If Power BI reports a missing file path:

1. Open **Transform Data**.
2. Open **Data Source Settings**.
3. Update the source path.
4. Refresh the dataset.

---

# ⚠️ Data Interpretation & Limitations

This project is primarily **descriptive analytics**.

Therefore:

- Higher enrolment volume does not automatically mean higher enrolment coverage.
- State/district differences may be influenced by population size and dataset coverage.
- The dashboard does not establish causal relationships.
- Monthly changes should be interpreted within the time period and coverage of the dataset.
- The displayed dashboard totals should not automatically be interpreted as India's complete Aadhaar enrolment population.

For stronger geographic comparisons, additional population-normalised metrics could be incorporated.

---

# 🏛️ About UIDAI Data Hackathon 2026

The **UIDAI Data Hackathon 2026** was organised by the **Unique Identification Authority of India (UIDAI)** in association with the **National Informatics Centre (NIC)** and the **Ministry of Electronics & Information Technology (MeitY)**.

The official event ran from **5 January 2026 to 20 January 2026**. citeturn0search2turn0search0

The hackathon asked participants to use Aadhaar enrolment and/or update datasets to identify meaningful patterns, trends, anomalies or predictive indicators and translate them into useful insights or solution frameworks. citeturn0search0

The official submission requirements included:

1. Problem Statement and Approach
2. Datasets Used
3. Methodology
4. Data Analysis and Visualisation

The official evaluation criteria included data analysis and insights, creativity/originality, technical implementation, visualization/presentation, and impact/applicability. citeturn0search0

---

# 🔗 Official Sources

### UIDAI Data Hackathon 2026

https://event.data.gov.in/challenge/uidai-data-hackathon-2026/

### Official Hackathon Event

https://event.data.gov.in/event/online-hackathon-on-data-driven-innovation-on-aadhaar-2026/

### Aadhaar Enrolment & Update Data

https://www.data.gov.in/catalog/aadhaar-enrolment-and-update-data

### Aadhaar Monthly Enrolment Data

https://www.data.gov.in/resource/aadhaar-monthly-enrolment-data

### UIDAI

https://uidai.gov.in/

---

# 👨‍💻 Author

## Aditya Kumar Mishra

**Data Analyst | Power BI | SQL | Python | Excel**

### Skills Demonstrated

```text
Power BI
DAX
Power Query
Data Modeling
Data Visualization
Excel
SQL
Data Analysis
```

