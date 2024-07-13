# Data Scientist Salary Estimation: Project Overview 
> Created By Nisarg Patel

* Created a ML model that estimates data scientists salaries (MAE ~ $ 11K) to help negotiate their salary.

* Scraped over 1000 job descriptions from glassdoor using python and selenium.

- Engineered features from the text of each job description to quantify the value companies put on python, excel, aws, and spark.

- Optimized Linear, Lasso, and Random Forest Regressors using GridsearchCV to reach the best model.
---
## Code and resources used 
**Python Version:** 3.9 <br>
**Libraries Used:** Pandas, Numpy, Sklearn, matplotlib, seaborn, selenium, json, pickle
**Scrapper Github:** https://github.com/arapfaik/scraping-glassdoor-selenium
**Scrapper Article:** https://towardsdatascience.com/selenium-tutorial-scraping-glassdoor-com-in-10-minutes-3d0915c6d905
