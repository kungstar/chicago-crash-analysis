# Chicago Car Crash Analysis (2021–2023)

##  Project Goal

Assist the Chicago Department of Transportation in reducing preventable traffic injuries by:
- Identifying key crash patterns and high-risk conditions
- Integrating both crash-level and person-level insights
- Predicting injury-related crashes using machine learning

---

##  Data Sources

| Dataset           | Description                          |
|-------------------|--------------------------------------|
| Traffic_Crashes.csv | Primary dataset of reported crashes (2021–2023) |
| People-crashes.csv | Supplementary data of people involved in crashes |

---

##  Key Steps

### 1 Data Preparation
- Filtered records to 2021–2023
- Aggregated person-level data (avg. age, # fatalities, # people per crash)
- Grouped 50+ crash causes into 8 categories
- Handled missing values in weather and road condition fields

### 2 Exploratory Analysis
-  Crashes spike between 4–6 PM (22% of incidents)
-  Rain increases road crashes by 1.8x
-  DUI crashes are rare  but significantly more severe
-  Crashes involving more people correlate with higher injury risk

### 3 Modeling
- Target: INJURY_CRASH (binary)
- Built baseline using Logistic Regression → 68% accuracy
- Improved with Random Forest → 72% accuracy
- Incorporated both environmental + human factors

---

##  Key Insights

- More people involved = Higher injury probability
- Fatalities and average age of people influence severity
- Road surface + weather conditions remain critical predictors

---

##  Repository Structure

| File / Folder        | Description                                |
|----------------------|--------------------------------------------|
| analysis.ipynb     | Main notebook: data prep, EDA, modeling     |
| presentation.pdf   | Summary report for stakeholders             |
| /data/             | Raw CSV files (not committed to repo)       |

---

##  How to Run

###  Setup

Install the dependencies:

```bash
pip install pandas scikit-learn seaborn matplotlib
