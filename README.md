# Data Scientist Salary Estimation: Project Overview 
> Created By Nisarg Patel

* Created a ML model that estimates data scientists salaries (MAE ~ $ 11K) to help negotiate their salary.

* Scraped over 1000 job descriptions from glassdoor using python and selenium.

- Engineered features from the text of each job description to quantify the value companies put on python, excel, aws, and spark.

- Optimized Linear, Lasso, and Random Forest Regressors using GridsearchCV to reach the best model.
---
## Code and resourses used
**Python Version:** 3.9 <br>
**Libraries:** Pandas, Numpy,Sklearn, Matplotlib, Seaborn, selenium, Json, Pickle <br>
**Scrapper Github:** https://github.com/arapfaik/scraping-glassdoor-selenium <br>
**Scrapper Article:** https://towardsdatascience.com/selenium-tutorial-scraping-glassdoor-com-in-10-minutes-3d0915c6d905 <br>

---
## Web Scrapping
Tweaked the web scraper github repo (above) to scrape 1000 job postings from glassdoor.com. <br>
<br>
With each job, we got the following: <br>
- Job title
- Salary Estimate
- Job Description
- Rating
- Company
- Location
- Company Headquarters
- Company Size
- Company Founded Date
- Type of Ownership
- Industry
- Sector
- Revenue
- Competitors

---

## Data Cleaning 
After scrapping the data, I cleaned it up so that it can be useful for traing the predictive model.
<br>
I made the following changes and created the following variables. <br>
* Parsed numeric data out of salary.
* Made columns for employer provided salary and hourly wages.
* Parsed ratings from the company name.
* Made a sperate column for company state.
* Created a column to identify if the job is at the company's headquarters.
* Created a column named company age from the founded year(2024 - Founded year).
* Made a column for different skills which were listed in the job descrption.
   * Python
   * R
   * Excel
   * AWS
   * Spark
* Created columns for Job Title, Seniority, and Job Description length.



