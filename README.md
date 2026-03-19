# Operational-Challenges-in-the-Healthcare-System-with-Data-Driven-Recommendations-Project


## Project Overview

This project analyses operational challenges in a mid-sized hospital using patient flow data. Six operational problems were investigated with the aim of providing data-driven recommendations to promote optimal healthcare system functioning.


## Data Source
Kaggle - Healthcare Analytics Patient Flow Data

## Tool
Microsoft Excel


## Clinical Problem
Hospital facilities in the healthcare system need to understand the factors that result in operational difficulties during specific time period. Management wants to know how patient’s demographics, time and date of presentation, and departmental referral can improve patient’s satisfaction and reduce waiting time, alongside other factors. 

## Dataset description
The dataset contains simulated patient’s record from a medium-sized hospital facility over a 16 Months period from September 2023 to December 2024. 
Columns included in the dataset:
-	Patient Id: unique anonymized patient identifier
-	Patient Admission Date/Time: date and time of patient arrival/registration 
-	Patient Gender: biological sex; male/female 
-	Patient Age: patient’s age in years (range: 0-79) 
-	Patient Race: self-reported ethnicity/background
-	Department Referral: specialty department for consultation 
-	Patient Admission Flag: admission decision; “Admission” vs “Not Admission”
-	Patient Wait time: measured in “weeks” 
-	Patient Satisfaction Score: graded from 1 to 10, with 1 being “least satisfied” and 10 being “very satisfied”. “Blank” means no response


## Data Cleaning/preparation
data was imported into Excel, inspected and duplicates were removed. formatting for each column was checked to ensure swift analysis.


## Exploratory Data Analysis
this involves exploring the data to answer key questions such as 

-	What are the demographics of the time period?
-	What factors determine a patient’s willingness to be admitted?
-	How does season affect the volume of patients?
-	What factors determine the wait time and how can it be improved?
-	what factors determine patient’s satisfaction?
-	which department is at a bottleneck and requires more attention?


## Data Analysis
the range was converted into a table, then several pivot tables were created on a new worksheet for proper analysis. Helper columns were created to create dummy numeric colume for regression analysis. Then regression analysis and multiple regression analysis were done. Lastly, different pivot charts were created to help summarize the data.


## Key Finding
1.	Demographics
    - Male patients represent 51.3% (n = 4,729), female 48.5% (n = 4,470)
    - Middle Aged (25.44%) and Older Adults (24.09%) represent over 50% of patients.
    - African American patients form the largest racial group 
    - Admission and non-admission rates are near equal at 5.1% and 49.9%
  
2.	Seasonal Volume Analysis
    - Total Patient volume increased 12.4% year on year (2023: 4,338 \ 2024: 4,878)
    - Summer consistently recorded peak volumes in both years
    - Monthly volume range was narrow (431 – 530) indicating stable year-round demand
    - No dramatic winter surge was observed contrary to typical hospital patterns.
      
3.	Wait Time Analysis
    - Mean wait time of 35.26 weeks significantly exceeds the NHS RTT target of 18 weeks
    - Multiple regression analysis (p<0.005) confirmed no single demographic factor significantly predicts wait time
    - Admission status showed the strongest association approaching significance at P=0.054
    - Department Referrals emerged as the greatest source of wait time variation (range 2.10 weeks)
    - Neurology (36.80 week) and Physiotherapy (36.57 weeks) recorded the highest wait time
      
4.	Admission Determinants
    - No demographic or operational factor significantly determines admission
    - Admission rates were equitable across all gender age, race and specialty groups
    - Renal recorded the highest specialty admission rate at 53%
    - Findings suggest admission decisions are clinically driven rather than demographically influenced
  
5.	Patient Satisfaction
    - Overall mean satisfaction score was 4.00/10 (1 being least and 10 being best) – critically low
    - 72.7% of satisfaction records were missing – representing a major data quality gap
    - Gastroenterology recorded highest satisfaction (5.80) and Renal lowest (4.35)
      
6.	Specialty Bottleneck
    - Neurology is the primary wait time bottleneck (36.80 weeks \ n =198)
    - Physiotherapy demonstrates dual pressure – high wait time (36.57 weeks) and average satisfaction
    - Renal presents a quality bottleneck – lowest satisfaction (4.57) despite shortest wait time (34.70 weeks)
    - General practice manages highest volume (n = 1,840) with below average wait times and above average satisfaction. 


## Recommendations

1.	Implement trust-wide RTT reduction programme – mean wait of 35.26 weeks is nearly double NHS target
2.	Mandatory satisfaction data collection at every patient contact
3.	Neurology capacity expansion – additional consultants and referral pathway review
4.	Physiotherapy service redesign including group and community therapy models
5.	Renal patient Experience improvement programme
6.	Elderly-targeted service enhancement programme
7.	Summer capacity planning – consistently peak demand season
8.	Winter surge preparedness given 12.4% year on year growth.


## Limitations
  - 58.6% of patients had no specialty recorded, limiting specialty-level analysis
  - 72.7% of satisfaction scores were missing limiting generalizability of satisfaction findings
  - Categorical variables were assigned ordinal numeric codes for regression – full dummy coding in python is recommended for future analysis
  - Dataset represents a single mid-sized facility and may not be generalisable. 


## Next Step
  - Integration of diagnosis and treatment outcome data for deeper clinical analysis
  - Benchmarking against NHS operational standards
  - Venturing into the world of database and use of SQL and Python for advanced analysis.
