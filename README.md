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



