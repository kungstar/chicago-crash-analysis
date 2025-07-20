# Chicago Car Crash Analysis (2021-2023)

## Project Goal
Help the Chicago Department of Transportation reduce preventable accidents by identifying patterns in crash causes and predicting high-risk scenarios.

## Data Sources
- Primary dataset: [Chicago Crash Reports (2021-2023)](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if)
- Supplementary data: [Vehicles](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Vehicles/68nd-jvt3) and [People Involved](https://data.cityofchicago.org/Transportation/Traffic-Crashes-People/u6pd-qa9d)

## Key Steps

### 1. Data Preparation
- Filtered to 2021-2023 data due to hardware limitations
- Grouped 50+ crash causes into 8 main categories
- Handled missing weather/road condition data

### 2. Analysis
- Found 4-6 PM as peak crash hours (22% of incidents)
- Identified rain as increasing road-related crashes by 1.8x
- Noted DUI crashes are rare (3%) but severe

### 3. Modeling
- Built Logistic Regression baseline (68% accuracy)
- Improved with Random Forest (72% accuracy)
- Focused on predicting: Failure to Yield, Distraction, Speeding

## How to Use This Repository

### Files
- `analysis.ipynb`: Full Python analysis notebook
- `presentation.pdf`: Non-technical summary for stakeholders
- `/data`: Contains raw CSV files (not committed)

### Setup
1. Install requirements:
   ```bash
   pip install pandas scikit-learn