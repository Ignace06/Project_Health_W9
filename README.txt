PART I : DATA SOURCE AND DATA SET

Source :
	Health Nutrition and Population Statistics / Doing Business /Statistical Capacity Indicators
	Online at:  https://data.worldbank.org
3 Dataset
	Rows :
		152 countries + years (1995-2021)
	Columns
		373 +54 Features (columns)
	Output 
		Health : Life expectancy (years)
		Wealth : GDP / Capita (PPP $)
		Health * Wealth 

Context: 
	Life expectancy is the fundamental metric for assessing population health. 
	Wealth is measured as GDP/capita in Purchasing Power Parity (PPP) for each country

Scope : 
	Countries with a sufficiently high GDP and with correctly recorded statistics
	Year : 2004-2016

Problem statement:
	How can countries better allocate their limited resources 
		To improve overall life expectancy for their population?
		To have a richer population  ?

Main takeaway (features which impacts) :
	Health : 	Mortality rate (infant)
	Wealth : 	% international migrant 
	Both : 		Electricity power demand


PART II : 
Details steps Import libraries Exploring the database Drop the unrelevant columns
Check, fill or drop the missing value per country and per columns 
Extraction dataframe for data Viz on Tableau 
Selecting columns1rows, check correlation, train, split and run 
Drop redundant rows 
Run heatmap matrix Distribution plots of numerical variables Selection minimum relevant columns for analysis 
Train/test/split
Scaling & transformation
Hyperparameter search


PART III : Apply RandomForestRegressor + GridSearchCV & Result

The R2 for the Random Forest in the TRAIN set is 0.99
The R2 for the Random Forest in the TEST  set is 0.95


 What characteristics have an impact on the life expectancy?

[('Mortality rate, infant (per 1,000 live births)', -21.0),
 ('Incidence of tuberculosis (per 100,000 people)', -19.0),
 ('Lifetime risk of maternal death (%)', -8.0),
 ('Mortality caused by road traffic injury (per 100,000 people)', -7.0),
 ('Out-of-pocket expenditure per capita, PPP ($)', 6.0),
 ('Prevalence of anemia among children (%)', -6.0),
 ('Prevalence of overweight (% of adults)', -3.0),
 ('Cause of death, by non-communicable diseases (% of total)', -2.0),
 ('Maternal mortality ratio ( per 100,000 live births)', 2.0),
 ('Fertility rate, total (births per woman)', -2.0),
 ('School enrollment, tertiary (%)', 1.0),
 ('People using drinking water services (%)', 1.0),
 ('% of adults with hypertension', 1.0)]
