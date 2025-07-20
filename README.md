# 🚗 Chicago Car Crashes Analysis (2023)  
*Predicting crash causes to improve road safety*  

**Last Updated**: 7/20/2025
**Author**: Washington Kungu

---

##  Project Overview  
**Goal**: Help the Chicago Department of Transportation (CDOT) reduce accidents by:  
1. Identifying the most common causes of crashes between 2021-2023
2. Building a model to predict high-risk scenarios  
3. Recommending data-driven interventions  

**Originally, I planned to analyze 10 years of data, but my laptop couldn’t handle the 5GB file. Switched to **2021-2023 only** (smarter sampling!).  

---

##  Data Sources  
1. **Main Dataset**: [Chicago Traffic Crashes (2021-2023)](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if)  
   - Key columns: `CRASH_DATE`, `PRIMARY_CONTRIBUTORY_CAUSE`, `WEATHER_CONDITION`  

2. **Supplementary Data**:  
   - [Vehicles](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Vehicles/68nd-jvt3)  
   - [People Involved](https://data.cityofchicago.org/Transportation/Traffic-Crashes-People/u6pd-qa9d)  

---

##  Key Questions  
1. What’s the **#1 preventable cause** of crashes?  
2. Do **rainy days** double distraction-related crashes? 
3. Can we predict **DUI-related crashes** before they happen?  

---

##  Methodology  
### Data Cleaning  
- Grouped 50+ crash causes into **8 categories** (e.g., "PHONE" → "DISTRACTION")  
- Handled missing values in `WEATHER_CONDITION` by labeling them as "UNKNOWN" 

### Modeling  
- Algorithms tested:  
  1. **Logistic Regression** (Baseline)  
  2. **Random Forest** (Best performance)  
  3. **XGBoost** (Overfit, discarded)  

---

##  Preliminary Findings  
| Insight | Impact |  
|---------|--------|  
| **4-6 PM** = 22% of crashes | Rush hour interventions needed |  
| **Rain** increases road-related crashes by 1.8x | Pre-storm road treatments advised |  
| **DUI crashes** are rare (3%) but severe | Hard to predict – need more data |  



---

##  Next Steps  
1. Merge vehicle/people data (WIP)  
2. Optimize model for **rare classes** (DUI, road conditions)  
3. Build interactive dashboard for CDOT  

---

## ⚠️ Known Issues  
1. **Timezone inconsistency**: Crash times don’t account for daylight savings. *(Will normalize in v2)*  
2. **Underreporting**: Minor crashes may be missing.  

---
