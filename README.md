# MTA_Turnstile_Data_2018_2021
Exploratory Data Analysis: MTA Turnstile Data
NYC Subway Ridership Changes from 2018 – 2021: Before & During the Pandemic
Abstract
•	The goal of this analysis is to explore how NYC subway trends have changed from pre-pandemic life through the past two years with COVID-19 (2018 - 2021). 
o	Insights from this data can be used to improve train scheduling & management. 
•	The analysis will begin with overall annual ride changes, and how those compare to several stations of interest (select transportation hubs, sports arenas, and parks). 
o	It will then take a more in-depth look at daily ridership sums in 2020 & 2021, which are placed next to daily new coronavirus cases in NYC.  
Design
•	MTA’s weekly public turnstile data was the foundation of the project.  4 months were selected (February – May) from each of the 4 years (2018 – 2021).  
o	The subset was chosen because the timeframe coincides with the initial shutdown in March 2020, and it was a manageably sized database for Jupyter manipulation.  
•	Pandas was used to scrub the data, which was then grouped by year, year/month, year/day, and then year/station.  
o	Pyplot was used to chart these new tables.
Data
•	Each individual turnstile is represented by a unique combination of control unit, remote unit, submit channel position, and station.  
•	The raw MTA data contains cumulative (instead of net) entries & exits for each of these turnstiles, which is reported at various 4 hour intervals.
o	Additionally, power & service outages sometimes created inaccurate & messy data.
Algorithms
•	The database was sorted by turnstile and then descending dates & times so that net entries or exits could easily be calculated/subtracted.  
o	If the new columns had irrational values, they were reset to zero in new cleaned columns.
•	Three new columns on the right (“Clean Net Entries”, “Clean Net Exits”, “Clean Net Entries & Exits”) formed the basis for all other analyses.
o	“Clean Net Entries” were used to determine overall rides taken during the time frame comparisons.
o	“Clean Net Entries & Exits” were used to get a sense of a station’s overall activity in the individual station analysis.
Tools
•	SQLite & SQLAlchemy for database selection & creation
•	Pandas for data manipulation
•	Seaborn & Matplotlib for visualizations
![image](https://user-images.githubusercontent.com/44270061/151106822-8641cc93-774a-4c9e-85d5-ce4e720c9d0c.png)
