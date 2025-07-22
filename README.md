# Chicago Car Crash Analysis (2021-2023)

## Project Goal

This project helps Chicago Department of Transportation reduce traffic injuries by figuring out what causes crashes with injuries. We use data from 2021-2023 to find patterns and make predictions so the city can focus on high-risk areas and save lives.

- Look at crash data and people involved to spot risky conditions
- Build a model to predict injury crashes
- Give recomendations to make streets safer

## Data Sources

Data comes from the Chicago Data Portal:
- [Traffic Crashes](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if) - Crash incidents (327,608 rows)
- [People Data](https://data.cityofchicago.org/Transportation/Traffic-Crashes-People/u6pd-qa9d) - People in crashes (712,248 rows)

## Key Steps

### 1. Data Preparation
- Used crashes from 2021-2023 only
- Combined crash and people data by CRASH_RECORD_ID
- Handled missing data like weather and age with zeros or averages
- Grouped crash causes into 8 main types

### 2. Exploration
- Crashes peak at 4-6 PM (22% of total)
- Rain makes crashes 1.8x more likely
- DUI crashes are rare but really bad
- More people in a crash means more injuries

### 3. Modeling
- Target: Injury crashes (yes/no)
- Tried Logistic Regression first (68% accurate)
- Switched to Random Forest, got better results (72% accurate)
- Used factors like number of people, age and weather

### 4. Results
- More people = higher chance of injuries
- Older people and fatalities linked to worse crashes
- Weather and road conditions matter a lot

## Repository Structure

| File/Folder | Description |
|-------------|-------------|
| `data/` | Crash and people datasets (CSV files, tracked with Git LFS) |
| `data/car-crashes-data-2021-2023.csv` | Crash data (327,608 rows) |
| `data/people-crashes.csv` | People data (712,248 rows) |
| `chicago-car-crash-analysis.ipynb` | Notebook with all code (prep, analysis, modeling) |
| `presentation.pdf` | Slide for stakeholders (presentation.pdf) |
| `.gitattributes` | Sets up Git LFS for large files |
| `.gitignore` | Ignores temporary files |

## How to Run

1. **Clone the Repo**:
   git clone https://github.com/kungstar/<repo-name>.git
   cd <repo-name>