# Chicago Car Crash Analysis (2021-2023)  
*Helping CDOT Save Lives Through Data*

## Project Goal  
We're helping Chicago's transportation team reduce serious crashes by:  
1. Finding **where and when** crashes most often cause injuries  
2. Identifying **key risk factors** (like speed, weather, road conditions)  
3. Building a **predictive model** to flag high-risk locations  
4. Giving **practical recommendations** to make streets safer  

*Expected Impact*: Could help prevent ~50 deaths/year (20% reduction goal)

## What We Discovered  

### Key Patterns in the Data  
- **Timing Matters**: 22% of crashes happen during rush hour (4-6PM)  
- **Weather Risk**: Rain makes crashes **1.8× more likely** to cause injuries  
- **Vehicle Occupancy**: Crashes with 3+ people have **3× more injuries**  
- **Age Factor**: Crashes involving seniors (65+) are **2.5× more deadly**  

### Model Insights  
Our best model (Random Forest) can predict injury crashes with **72% accuracy**:  
- **Top Predictors**:  
  1. Number of people in crash  
  2. Posted speed limit  
  3. Road surface condition  
  4. Lighting at time of crash  
  5. Driver age  

- **Limitations**:  
  - Struggles with rare severe crashes (only catches 53% of fatalities)  
  - Doesn't include real-time traffic data  

## How CDOT Can Use This  

### Immediate Action Items  
1. **Target High-Speed Zones**  
   - Install speed cameras where speed > 40mph  
   - *Expected impact*: 30% fewer fatal crashes  

2. **Improve Nighttime Safety**  
   - Add streetlights at 50 worst locations  
   - *Expected impact*: 15% reduction in night crashes  

3. **Fix Problem Roads**  
   - Prioritize resurfacing roads with poor conditions  
   - *Expected impact*: 10% fewer injury crashes  

### Long-Term Strategies  
- Test adding **weather alerts** to traffic signals  
- Focus **DUI enforcement** on Friday/Saturday nights  
- Develop **senior driver safety program**  

## About the Data  
We analyzed **327,608 crashes** (2021-2023) from Chicago's open data portal:  
- **Crash Data**: Location, time, road conditions  
- **People Data**: Age, injury level, role (driver/pedestrian)  

*Limitations*: Some weather data was missing - could improve with live feeds  

## How to Run This Analysis  

1. **Get the Data**  
   ```bash
   git clone https://github.com/kungstar/chicago-crash-analysis.git
   cd chicago-crash-analysis
2. **Install Requirements**
3. **Open the Notebook**
