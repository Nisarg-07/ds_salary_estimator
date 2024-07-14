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

---
## EDA
<br>
I looked at the distribution of data and the value counts for various categorical variables. 
<br>

Below are the few highlights from my observation.
<br>

<img width="219" alt="StateXavg_salary" src="https://github.com/user-attachments/assets/ad8b6f85-a655-4b71-b921-ee5a5f3549cf"> <br>
- From the above table it can be said that avgerage Data scientist's salary in the **California** is the **highest**<br> 
- However it is bit odd that the **New york** is in the **Last** Place in top 8 highest paying states. <br>
<br>
<img width="219" alt="PositionXAvg_salary" src="https://github.com/user-attachments/assets/5e4a4b00-3bab-4614-9e00-1aa8095490c3"> <br>
<br>
- The above table shows average salary for various positions in the data science field. <br>

<br>

![CityXJobs_count](https://github.com/user-attachments/assets/cb2e1ef0-6a8a-4a74-87be-1dc51bd96642)
* The above bar graph displays the number of job present in each state and it can be seen that the **California** has **highest number** of jobs in the **Data science field**.

![heatmap](https://github.com/user-attachments/assets/f31c3db5-39a7-46f8-8091-7a1e79bbf5b8)
* The above Heatmap it can be seen that the **strong positive correlation** is between company **age** and **descriptionlength** and **age** of the company and **Number of competitors**.
* Also there is a **positive corrrelation** between **average Salary** and **decription length** and **average Salary** and **Number of competitors**.
* Whereas, a **strong negative correlation** between **ratings** and **description length**.

---
## Model Building

First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 20%.<br>
<br>
I tried three different models and evaluated them using Mean Absolute Error. I chose MAE because it is relatively easy to interpret and outliers aren’t particularly bad in for this type of model.<br>
<br>
I tried three different models:

* **Multiple Linear Regression** – Baseline for the model.
* **Lasso Regression** – Because of the sparse data from the many categorical variables, I thought a normalized regression like lasso would be effective.
* **Random Forest** – Again, with the sparsity associated with the data, I thought that this would be a good fit.

---
## Model Performance 

The Random Forest model far outperformed the other approaches on the test and validation sets.
- **Random Forest :** MAE = 11.22
- **Linear Regression:** MAE = 18.86
- **Lasso Regression:** MAE = 19.67
---
## Huge thanks to
**ken Jee :** https://github.com/PlayingNumbers

Nisarg Patel © 2024









