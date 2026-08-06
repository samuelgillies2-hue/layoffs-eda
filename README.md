Layoffs Exploratory Data Analysis (EDA)
Overview

This project explores a dataset of company layoffs using MySQL. It builds on a cleaned staging table (layoffs_staging2) and runs a series of SQL queries to uncover trends in layoffs by company, industry, country, funding stage, and time period.

Dataset
Table: layoffs_staging2 (schema: world_layoffs)
Key columns used:
company — name of the company
industry — industry the company operates in
country — country where layoffs occurred
stage — company funding/growth stage (e.g., Series A, IPO, Post-IPO)
date — date the layoff was reported
total_laid_off — number of employees laid off
percentage_laid_off — proportion of the workforce laid off (1 = 100%, i.e. company shut down)
funds_raised_millions — total funding raised by the company, in millions
What This Analysis Covers

1. Data overview

Full table preview
Max values for total_laid_off and percentage_laid_off
Min/max date range in the dataset

2. Company shutdowns

Companies with percentage_laid_off = 1 (i.e., laid off their entire workforce), sorted by funds raised
Count of full shutdowns by year

3. Aggregate breakdowns

Total layoffs by company
Total layoffs by country
Total layoffs by industry
Average percentage laid off by company

4. Time trends

Total layoffs by year
Total layoffs by month
Rolling (cumulative) monthly total using a window function

5. Company performance over time

Layoffs by company per year
Top 5 companies by layoffs per year, using DENSE_RANK()

6. Funding vs. layoffs

Companies with the highest funds raised alongside their layoff figures, to explore whether well-funded companies were still cutting staff
How to Use
Open Layoffs_EDA.sql in MySQL Workbench (or any MySQL client) connected to the world_layoffs schema.
Run queries individually (highlight + execute) to explore each angle of the data.
Export any result set to CSV via the results grid's export icon, then open in Excel if you want to share or visualize findings outside SQL.
Possible Next Steps
Break out layoffs by location (city-level), if available, for regional analysis.
Correlate percentage_laid_off against funds_raised_millions more formally (e.g., scatterplot in Excel/Python) to see if funding level predicts layoff severity.
Build a dashboard (Tableau, Power BI, or Excel PivotTables) from exported query results for visual storytelling.
