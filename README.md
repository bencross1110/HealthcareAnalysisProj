# HealthcareAnalysisProj
Project using Python to Clean and Analyse Healthcare related dataset.

Start Time: 12:00pm 16/08/2024
Log:

EXPLORATORY STAGE:

Did standard checks:
- head (Name values have inconsistent upper/lower case formatting. Billing Amount values have 6 decimal places)
- dtypes (variables that should be dates are object types)
- shape (55000 rows x 15 columns)
- variable names into list
- checked for any null values (none at all!)
- checked unique values in each column to see if there are any errors (no errors found that weren't already known)

Randomly produced healthcare related dataset with variables such as: Medical Condition, Admission Date, Insurance Provider, 
Age, Medication etc. 
--> Lots of different unique Doctor and Hospital values (40341 and 39876 respectively out of 55000 rows)
--> 5 Insurance providers
--> 3 Admission Types
--> 5 Medications
--> 3 Test Results

Data doesn't have huge amount of variety but there is some cleaning to be done and potentially some simple relationships that can
be explored e.g:
- Insurance Provider/Medication/Medical Conditions x Billing Amount/Age/Time taken to Discharge

As data has been artificially produced - potentially some data that doesn't make sense to real world:
e.g: Medication for 'Cancer' being Penicillin - which is typically used to treat bacterial infections - or just some kind of painkiller



CLEANING STAGE:

- Fixed 'Name' column formatting
- Changed 'Date of Admission' and 'Discharge Date' to datetime variables and altered names of variables to be consistent
		--> Now 'Admission Date' and 'Discharge Date'
		--> Created new variable 'Time Taken to Discharge' by finding the difference between two dates
- Removed excess decimals from 'Billing Amount' values and renamed the variable to 'Billing Amount (£)' to add some context
- Negative values in the 'Billing Amount (£)' which don't really make sense, so removed (108 rows out of 55000 rows - 0.2%)



ANALYSIS STAGE:

Wanted to explore some of the statistics of the data, e.g: finding, min, max, mean and std deviation of variables such as age, billing 
amount, time taken to discharge. Will also make some exploratory plots.

- Min/max/mean/std of Age, Billing Amount, Time Taken to Discharge
- Count of different Blood Types, Medical Condition, Insurance Provider, Admission Type, Medication, Test Results, Gender

- Make splits for Billing amount depending on Insurance Provider, Medical Condition, Medication


