🏥 CareFlow: Clinical Pathway Process Mining

This repository contains the data and code for **Group 7**, led by **Shangavai (Team Lead)**. The project focuses on data preprocessing and clinical pathway transition tracking using a patient treatment event log dataset.

📌 Project Overview

Healthcare organizations generate large volumes of event data through Electronic Health Record (EHR) systems. Understanding patient journeys and identifying inefficiencies within clinical processes is critical for improving healthcare delivery.

CareFlow is a Clinical Pathway Process Mining project that analyzes patient treatment journeys using healthcare event logs. The project reconstructs real-world clinical workflows, discovers treatment pathways, identifies bottlenecks, and provides actionable insights to improve patient flow and operational efficiency.

🎯 Business Problem

Hospitals often face challenges such as:

1. Long patient waiting times
2. Inefficient resource utilization
3. Delays between diagnostic and treatment activities
4. Lack of visibility into patient pathways
5. Difficulty identifying process bottlenecks

This project applies Process Mining techniques to discover how patients actually move through the healthcare system and where delays occur.

🎯 Project Objectives

1. Analyze patient treatment event logs
2. Discover actual clinical pathways
3. Identify bottlenecks and delays in patient care
4. Measure pathway performance and lead times
5. Track resource utilization across doctors, nurses, labs, and treatment teams
6. Generate actionable recommendations for healthcare administrators

📂 Dataset Description

The dataset contains patient treatment event logs with the following attributes:

  **Column**                **Description**
  
patient	      Unique patient identifier
action	      Clinical activity performed
org:resource	Healthcare resource involved
DateTime	    Timestamp of activity

**Sample Activities**
-- First Consult
-- Blood Test
-- Physical Test
-- X-Ray Scan
-- Second Consult
-- Surgery
-- Medicine
-- Final Consult

Each patient's treatment journey is captured as a sequence of timestamped events.

🔄 Clinical Workflow
First Consult
      ↓
Diagnostic Tests
(Blood Test / Physical Test)
      ↓
X-Ray Scan
      ↓
Second Consult
      ↓
Medicine / Surgery
      ↓
Final Consult

🛠️ Technologies Used
**Programming Language**

-- Python

**Libraries**

-- Pandas
-- NumPy
-- PM4Py
-- Matplotlib
-- Seaborn

**Process Mining Techniques**

-- Process Discovery
-- Variant Analysis
-- Directly-Follows Graph (DFG)
-- Bottleneck Detection
-- Throughput Time Analysis
-- Resource Analysis

**Visualization**
-- Process Flow Maps
-- DFG Models
-- Statistical Charts
-- Performance Dashboards

📊 Project Workflow

1️⃣ **Data Loading**

Import and inspect healthcare event logs.

import pandas as pd

df = pd.read_csv("ArtificialPatientTreatment.csv")

2️⃣ Data Preprocessing

-- Handle timestamp conversion
-- Create event logs
-- Sort activities by patient and timestamp

3️⃣ Event Log Creation

Convert structured event data into process mining event log format.

4️⃣ Process Discovery

Generate process maps showing actual patient pathways.

5️⃣ Performance Analysis

Calculate:

-- Case durations
-- Activity frequencies
-- Waiting times
-- Throughput times

6️⃣ Bottleneck Detection

Identify stages where patient delays occur.

Examples:

-- Delays before second consultations
-- Diagnostic test wait times
-- Surgical scheduling delays

📈 Key Insights Generated

**Process Discovery**

-- Identified the most common patient treatment pathways.
-- Revealed variations across patient journeys.

**Bottleneck Analysis**

-- Detected high waiting times between diagnostic tests and consultations.
-- Highlighted stages contributing most to overall treatment duration.

**Resource Utilization**

-- Measured workload distribution among doctors, nurses, laboratories, and imaging teams.
-- Identified potential resource constraints.

**Clinical Performance**

-- Measured average treatment completion times.
-- Quantified process efficiency across patient cases.

📊 Example Metrics

The project analyzes:

1. Total Patients
2. Total Clinical Activities
3. Average Pathway Duration
4. Average Waiting Time
5. Surgery Cases
6. Medicine Cases
7. Resource Utilization Rate
8. Process Variants

💡 Business Value

Healthcare administrators can use the findings to:

✅ Reduce patient waiting times

✅ Improve patient satisfaction

✅ Optimize staff allocation

✅ Improve clinical workflow efficiency

✅ Increase treatment throughput

✅ Support data-driven decision making

📸 Project Outputs

**Process Map**
Visual representation of patient journeys.

**Directly-Follows Graph (DFG)**
Displays relationships between sequential clinical activities.

**Bottleneck Analysis**
Highlights stages responsible for treatment delays.

**Resource Analysis**
Measures utilization of clinical resources.

**Performance Dashboard**
Provides operational insights for stakeholders and decision-makers.

🚀 Future Enhancements

1. Interactive Power BI Dashboard
2. Real-Time Process Monitoring
3. Predictive Delay Analysis
4. Machine Learning for Patient Outcome Prediction
5. Healthcare KPI Monitoring Framework

📁 Repository Structure

CareFlow-Clinical-Pathway-Process-Mining
│
├── Dataset
│   └── ArtificialPatientTreatment.csv
│
├── Notebooks
│   └── Clinical_Pathway_Process_Mining.ipynb
│
├── Visualizations
│   ├── Process_Map.png
│   ├── DFG.png
│   └── Bottleneck_Analysis.png
│
├── README.md
│
└── requirements.txt

🎓 Skills Demonstrated

-- Process Mining
-- Healthcare Analytics
-- Data Cleaning
-- Data Visualization
-- Business Process Analysis
-- Event Log Analysis
-- Python Programming
-- Data Storytelling
-- Operational Analytics

👩‍💻 Author
Shangavai P A

Aspiring Data Analyst | Process Mining Enthusiast | Healthcare Analytics

Connect With Me
LinkedIn: https://www.linkedin.com/in/shangavai/
GitHub: https://github.com/SHANGAVAI
⭐ If you found this project interesting, feel free to star the repository and connect with me!
