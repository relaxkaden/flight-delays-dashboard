# U.S. Flight Delays Dashboard
Tools: Python · Pandas · Matplotlib · Seaborn · Tableau Public
Dataset: Bureau of Transportation Statistics (BTS) — Jan/Feb 2024
Records: 1,048,575 domestic flights

# Overview
Analysis of over one million real U.S. domestic flight records to identify cancellation patterns, ground congestion hotspots, and delay causes across major airports. The cleaned dataset was used to build an interactive Tableau Public dashboard with five views: cancellation rate by airport, delay cause breakdown, ground congestion by taxi-out time, day-of-week patterns, and a geospatial state-level map.

# Files
flight_delays_prep.ipynb                Full data cleaning, feature engineering, EDA, and export pipeline
data/flight_data_2024.csv               Raw BTS flight data (Jan–Feb 2024)
data/flight_delays_tableau_ready.csv    Cleaned and enriched dataset loaded into Tableau

# Key Findings
SEA, EWR, and ORD had the highest cancellation rates among major airports — consistent with winter weather exposure in January and February
Late Aircraft was the most common delay cause, affecting 97,315 flights (9.3% of all records)
JFK, ORD, and LGA ranked highest for ground congestion, averaging over 22 minutes of taxi-out time per departure
Tuesday had the highest cancellation rate of any weekday (3.4%), while Wednesday and Thursday were the most reliable days to fly
Alaska, Washington, and Oregon showed the highest state-level cancellation rates on the geospatial map, driven by Pacific Northwest and interior weather patterns


# Dashboard
View the live interactive dashboard on Tableau Public:
https://public.tableau.com/views/airlinedelays_17764652170450/Dashboard1?:language=en-US&:sid=&:redirect=auth&showOnboarding=true&:display_count=n&:origin=viz_share_link

# Dashboard Sheets
Cancellation Rate by Airport — Top 20 airports filtered to 3K+ flights, sorted by cancellation rate
Delay Causes — Treemap breaking down On Time / Late Aircraft / Ground Congestion / Weather / Cancelled
Ground Congestion — Average taxi-out time by airport (proxy for surface congestion)
Day of Week — Cancellation rate by day, Monday through Sunday
State Map — Filled U.S. map colored by average cancellation rate per state


How to Run
Requirements
pandas
numpy
matplotlib
seaborn
Install with:
bashpip install pandas numpy matplotlib seaborn
Run the notebook
bashjupyter notebook flight_delays_prep.ipynb
The notebook will:

Load and clean the raw BTS CSV
Engineer delay category, primary cause, and congestion flags
Output summary KPIs to the console
Generate all exploratory charts
Export flight_delays_tableau_ready.csv for Tableau


Data Source
https://www.kaggle.com/datasets/nalisha/flight-delay-and-cancellation-data-1-million-2024

Author
Kaden Van Atta
kadenvanatta.com · github.com/kadenvanatta · linkedin.com/in/kadenvanatta
