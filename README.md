# F1-Formula-1-Race-Weekend-Analytics-Dashboard
An **end-to-end data analytics project** that analyzes a complete Formula 1 race weekend using **real lap-level and telemetry data** from the FastF1 API.  
The project transforms raw motorsport data into **actionable insights** through **feature engineering, exploratory analysis, and an interactive dashboard built with Plotly Dash**.

## Project Overview
This project focuses on **race-weekend performance analysis**, covering:
- Free Practice (FP1, FP2, FP3)
- Qualifying
- Race

The goal is to evaluate **driver performance, consistency, race pace translation, tyre degradation, and telemetry-based driving behavior** using a real-world, high-frequency dataset.

## Objectives
- Analyze how **qualifying performance translates into race pace**
- Measure **driver consistency** using lap-time variability
- Study **tyre degradation and stint behavior**
- Compare **drivers vs teammates** to control for car performance
- Visualize **telemetry metrics** (speed, throttle, brake, RPM)
- Build an **interactive dashboard** for exploratory analysis

## Tech Stack
### Programming & Analysis
- Python
- pandas, numpy
- scipy (statistical analysis)

### Data Source
- **FastF1 API**
  - Official Formula 1 timing and telemetry feeds
  - Lap times, stints, tyre compounds, speed, throttle, brake, RPM

### Visualization & Dashboard
- Plotly
- Dash

## Data Pipeline
### Data Ingestion
- Loaded race-weekend sessions (FP → Q → Race) using FastF1
- Cached data locally for performance and reproducibility

### Data Cleaning
- Removed in-laps, out-laps, and invalid lap times
- Filtered representative laps for accurate performance analysis

### Feature Engineering
- Lap time in seconds
- Tyre age per stint
- Qualifying vs race pace deltas
- Consistency metrics using lap-time standard deviation

### Exploratory Data Analysis (EDA)
- Free practice pace evolution
- Qualifying lap distributions
- Race consistency vs average pace
- Tyre degradation trends

### Interactive Dashboard
- Driver & session selection
- Metric selector (Speed, Throttle, Brake, RPM)
- Teammate comparison toggle
- Telemetry visualization with defensive error handling

## Dashboard Features
### Lap Time Trend
Visualizes lap-by-lap performance for any driver and session.
  
### Qualifying vs Race Pace
Evaluates how well peak qualifying speed translates into race execution.

### Consistency vs Average Pace
Highlights drivers who combine **speed and reliability**.

### Tyre Degradation Analysis
Shows compound-specific degradation trends during the race.

### Telemetry Comparison
Interactive telemetry plots:
- Speed
- Throttle
- Brake
- RPM  
Supports **driver vs teammate comparison** with defensive handling for missing data.

## Key Insights (Example)
- Qualifying speed alone is not a reliable predictor of race performance
- Drivers with lower lap-time variance often achieve stronger race results
- Tyre management and long-run consistency outweigh peak lap speed
- Teammate comparison isolates driver execution from car performance

## Skills Demonstrated
- Exploratory Data Analysis (EDA)
- Time-Series Analysis
- Feature Engineering
- API Data Ingestion
- Statistical Reasoning
- Interactive Dashboard Development
- Defensive Programming & Error Handling

## Future Enhancements
- Multi-race and season-level analysis
- Teammate performance benchmarking
- Sector-level telemetry comparison
- Predictive tyre degradation modeling
- Cloud deployment (Render / Streamlit Cloud)

## Acknowledgements
- FastF1 open-source community
- Formula One Management (FOM) public timing feeds
