# The Economic Impact of Delayed Diabetic Care: A Comparative Analysis from 1999 to 2021

## Description

This project embarks on a profound journey through data analysis to elucidate the economic implications of delayed diabetic care, spotlighting the nexus between Diabetes Mellitus (DM) and hospitalization rates from 1999 to 2021. With a staggering revelation that 46% of diabetes-related hospital admissions result in readmissions, the initiative seeks to decode the narrative spun by data spanning over two decades to underscore potential interventions for curtailing preventable hospitalizations.

## Getting Started

### Dependencies

To delve into this analysis, ensure the availability of the following tools and libraries in your Python environment:

- Jupyter
- ipykernel
- pandas
- seaborn
- dash
- plotly
- pymysql
- SQLAlchemy

### Installation


pip install jupyter ipykernel pandas seaborn dash plotly pymysql sqlalchemy


## Main Focus Point
The core objective is to unravel the association between Diabetes Mellitus (DM) and escalating hospitalization rates, investigating avenues to alleviate the necessity for hospital-centric quarterly check-ups.

## Example Code
The SQL script below exemplifies the analysis, focusing on gender-wise readmission rates for a nuanced understanding:

USE project4;

-- Analyzing readmission counts by gender for patients over 45
SELECT gender, COUNT(*) AS readmission_count
FROM readmittion
WHERE readmitted = 'Yes' AND age > 45
GROUP BY gender
ORDER BY readmission_count DESC;

This query underscores our commitment to discerning demographic patterns in readmission data, offering a lens to view how gender and age interplay within the readmission statistics.

## Features
Data-Cleaning Techniques: The project applies several data-cleaning methodologies such as irrelevant data removal and error rectification, pivotal for maintaining data integrity.
Visualizations (EDA): Engaging graphs illuminate various dimensions, including gender-based readmission rates and age-specific hospitalization trends.
Comprehensive Analysis: Through SQL, the project delves into demographic distributions, readmission rates, and temporal changes in hospitalization statistics.

## Visuals
Intriguing visuals depict:

Gender disparities in readmission occurrences.
Age-centric analysis of hospital readmissions.
Trends and patterns in diabetes-related hospitalizations across the studied timeframe.

## How to Use
1. Clone the Repository: Start by cloning this repository to your local machine or downloading the SQL script files.
2. Database Setup: Ensure you have a database system that can run SQL queries (e.g., MySQL).
3. Run the Queries: Open your database interface, load the SQL scripts, and execute them.
4. Analyze the Results: Review the output of each query to derive insights into the diabetes patient data.

Data No 1 :

Beata Strack, Jonathan P. DeShazo, Chris Gennings, Juan L. Olmo, Sebastian Ventura, Krzysztof J. Cios, and John N. Clore, “Impact of HbA1c Measurement on Hospital Readmission Rates: Analysis of 70,000 Clinical Database Patient Records,” BioMed Research International, vol. 2014, Article ID 781670, 11 pages, 2014.

https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008

Data No 2 :

California Health and Human Services Agency (CalHHS) Open Data Portal

https://data.chhs.ca.gov/dataset/rates-of-preventable-hospitalizations-for-selected-medical-conditions-by-county/resource/7c7aed93-3643-43b8-92fc-324bf8fc13f2


