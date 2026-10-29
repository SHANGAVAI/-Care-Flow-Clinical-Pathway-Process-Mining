# Care-Flow: Clinical Pathway Process Mining

This repository contains the data and code for **Group 7**, led by **Shangavai (Team Lead)**. The project focuses on data preprocessing and clinical pathway transition tracking using a patient treatment event log dataset.

---

## 📌 Project Overview
The objective of this project phase is to ingest, clean, and structure raw clinical logs. By tracking sequential events per patient, the pipeline lays the groundwork for generating structural care flows, identifying medical bottlenecks, and mapping clinical actions.

---

## 🚀 Key Achievements & Core Workflow

*   **Exploratory Data Analysis (EDA):** Verified data shapes, column configurations, and confirmed that the event dataset contains zero missing values before transformation.
*   **Temporal Chronology Sorting:** Converted text fields to true timestamp objects and ordered the event sequence chronologically based on individual patients.
*   **Directly-Follows Mapping:** Generated transition variables by linking each active clinical task to its immediate subsequent action within the patient journey.
*   **Terminal Sequence Imputation:** Handled missing tracking endpoints at discharge by filling empty transition markers with the dataset's modal action.

---

## 🛠️ Tech Stack & Libraries Used
The pipeline is developed using **Python 3** and leverages the following data-centric libraries:
*   **`pandas`** — Handled core DataFrame structural operations, CSV parsing, file sorting, and grouping.
*   **`numpy`** — Integrated for performance computing and handling system null structures.
*   **`scikit-learn`** — Imported preprocessing utility classes (`LabelEncoder`, `StandardScaler`) for upcoming modeling stages.
*   **`warnings`** — Cleaned up system runtime visualization by filtering operational code notices.

---

## 📊 Dataset Profile (`ArtificialPatientTreatment.csv`)
The codebase processes an event dataset mapped with the following characteristics:
*   **Data Dimensions:** 690 total event log listings across 4 tracking fields (`patient`, `action`, `org:resource`, `DateTime`).
*   **Cohort Count:** Tracks 100 individual patient records sequentially.
*   **Clinical Elements:** Classifies 8 distinct operational actions (First consult, Blood test, Physical test, Second consult, Surgery, X-ray scan, Medicine, Final consult).
*   **Operational Staff:** Distributes actions across 13 recorded medical providers (physicians, nurses, and laboratory units).

---

## 📂 Project Branch Execution

### 1. Ingest and Process Data
Execute the primary python workspace environment to load the source data matrix and build out the transition sequence map:
```python
import pandas as pd

# Load dataset
df = pd.read_csv("ArtificialPatientTreatment.csv")

# Format timelines and sort pathways
df['DateTime Change'] = pd.to_datetime(df[' DateTime'])
df = df.sort_values(by=['patient', 'DateTime Change'])

# Build NextActivity sequence map
df['NextActivity'] = df.groupby('patient')[' action'].shift(-1)
df['NextActivity'] = df['NextActivity'].fillna(df['NextActivity'].mode()[0])
```

---

## 👥 Group 7 Contributor
*   **Shangavai** — *Team Lead (TL)*

