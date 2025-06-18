Project: Wild Goose Chase

Goal:
To explore whether the period of the “solar maximum” (1986–2008) and two large solar flares (1989 and 2003) correlate with an increase in residential fire activity caused by electrical factors.

______________________________________________________________________________

Steps:

1) Data Collection & Initial Cleaning
Downloaded all fire incident data from FEMA (1986–2008).
Removed irrelevant columns and information.
→ See folder: “Preclean Data”


2) Filtering for Relevant Incidents
Since we are focusing on residential fires with an electrical cause, we applied filters using several columns.
Because FEMA used two different coding systems during this period, we used two sets of filters:
	a) First Dataset (1986–1998)
	Residential fires: Column FPU (Fixed Property Use), any code starting with "4"
	Electrical cause: Column IF (Ignition Factor), codes:52, 54, 55, 59, 50, 74, 75, 76, 79, 70, 99, 00

	b) Second Dataset (1999–2008)
	Residential fires: Column AREA_ORIG (Area of Fire Origin), codes:14, 20, 21, 22, 23, 24, 25, 26, 27, 28, 52, 55, 72, 73, 74, 75, 76, 77, UU
	Electrical cause: Column CAUSE_IGN (Cause of Ignition), codes: 2, U
				  Column FACT_IGN_1 (Factors Contributing to Ignition 1), codes:0, 21, 22, 30, 31, 32, 33, 34, 35, 36, 37, 40, 41, 42, 43, 44, 52, 53, 54, 56, 58, 60, UU
→ See folder: “Filter Data”


3) Analysis
Counted the number of filtered fire incidents per year.
Calculated Spearman correlation between the number of incidents and the mean yearly number of sunspots (data retrieved from SILSO).
→ See CSV file: “Result” (Source links to both the FEMA fire incidents and SILSO Yearly Mean Sunspots data)
→ Code see IPYNB file: "Data_Filtering_&_Spearman_Correlation"
