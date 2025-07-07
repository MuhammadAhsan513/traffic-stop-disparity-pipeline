# traffic-stop-disparity-pipeline
A scalable data pipeline built in Python to ingest and preprocess multi-source traffic stop datasets across the U.S., enabling deep investigation of racial and demographic disparities in policing practices for Power BI analysis.
 
# 🚔 Traffic Stop Disparity Data Pipeline – USA

A robust, memory-efficient data processing pipeline designed for loading and cleaning multiple large CSV files from subfolders. This project lays the foundation for a **fairness-driven analysis** of policing patterns using the U.S. traffic stop dataset.

---

## 🎯 Case Study: Disparities in Traffic Stops

### 📢 Problem Statement

Over the past decade, civil rights organizations and policy makers have raised critical concerns about disproportionate policing of **minority** and **young drivers** across U.S. states. Issues include:

- Increased search or arrest rates with lower contraband discovery
- Aggressive enforcement during certain time slots
- Unequal treatment for the same violation based on race or age

A national commission has launched a data-driven investigation using standardized, public traffic stop data to uncover these disparities and promote transparency.

---

## 💼 Business Problem

Stakeholders want evidence to evaluate whether law enforcement:

- Applies consistent and fair practices
- Uses data efficiently to drive outcomes
- Demonstrates implicit bias based on demographics

---

## 🧠 Analytical Objectives (Post-Pipeline)

Once the data is processed, the analysis should focus on:

1. **Search efficiency vs. demographic bias**
2. **Time-of-day enforcement spikes**
3. **Violation vs. outcome disparity**
4. **Shift-based officer behavior**
5. **Contraband trends by group**
6. **Geographic patterns of leniency/aggression**
7. **Clustering of stereotyped enforcement**
8. **Impact of historical/external events**

---

## 📊 What This Pipeline Does

This pipeline prepares the data for the above investigations by:

- 📂 Scanning multiple nested folders for `.csv` files
- 💾 Reading massive CSVs with memory-efficient loading
- 🧹 Removing duplicates and empty columns
- 🕒 Standardizing datetime columns
- 🧱 Combining them into a single clean dataset for Power BI

---

## 🛠 Technologies Used

- Python 3
- Pandas
- Jupyter Notebook / Anaconda
- CSV I/O
- OS Module

---

## 🧪 How to Run

```python
from pipeline import process_csvs_memory_safe

process_csvs_memory_safe(
    input_dir=r"C:\Users\YourName\Desktop\Dataset\Dataset",
    output_csv="final_dataset_for_powerbi.csv",
    chunk_size=5000
)

