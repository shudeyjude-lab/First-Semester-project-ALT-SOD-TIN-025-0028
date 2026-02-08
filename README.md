 # =========================================

# Student Name: Achuka Jude

# Learner ID: ALT/SOD/TIN/025/0028

# Track: Data Engineering

# Mini Project: Contact Tracing System

# =========================================

## Health Clinic Data and Outlier Analysis

This is a health data analysis that processes patient vital signs, performs statistical analysis, detects abnormal values, and identifies high-risk patients using medical thresholds and IQR outlier detection.

This system simulates a clinical monitoring tool used in hospitals or health centres to analyse patient vitals and detect potential medical risk early. 

## The program:

* Loads patient data from a CSV file
* Clean and validates health data
* Performs statistical analysis
* Detects abnormal vital signs using IQR (Interquartile Range)
* Classifies patient risk levels
* Generates summary reports
* Visualises heart rate distribution

## How it works
1.  Data Loading: The system reads the CSV using ```csv.DictReader```, converts values to numeric types and skip invalid rows

2.  Statistical Analysis: The following are computed:
```
* Mean
* Median
* Mode
```

3.  Outlier Detection, using the IQR formula:
```
* IQR = Q3 − Q1
* Lower Bound = Q1 − 1.5 × IQR
* Upper Bound = Q3 + 1.5 × IQR
```

4.  Risk classification: Patients are classified based on abnormal vital signs and clinical thresholds.

5.  Dataset Format: The CSV file includes:
```
{patient_id, age, systolic_bp, heart_rate, oxygen_saturation, and temperature}
```

## How to run 
 
```bash
python health_clinic_analysis.py
```
Run Unit Tests:
```bash
python tests.py
```

## Output

![alt text](image/summary_report.png)

![alt text](image/visualisation.png)