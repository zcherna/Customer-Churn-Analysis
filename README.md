![header](./images/Customer_Churn.jpg)
# Overview

The purpose of this project is to build a predictive model that will enable SyriaTel, a Telecommunications company, to better understand customer churn and leverage the insights of data to make smarter decisions. Ultimately, their goal is to increase profits by reducing customer churn. At the end of my analysis, I present concrete recommendations to reduce customer churn based on my findings and discuss next steps for deployment of the predictive model going forward. 
# Business Understanding
It is well understood that the cost to acquire new customers is significantly more expensive than the cost to keep current customers. Therefore, customer churn - the turnover rate of customers, is a crucial metric that organizations must seek to minimize. This is especially true now at the time of my analysis, January 2023,  due to rising interest rates and high inflation. The challenging economic environment forces customers to be even more selective about spending money and businesses will be under greater pressure. In order to minimize churn, organizations need to first gain a deep understanding of how customers feel about the products and services they offer and identify which customers are most at risk of leaving. Armed with those insights, the organization can then act strategically to keep their customers satisfied and reduce churn. 
# Data Understanding
For my analysis I used the SyriaTel dataset, which contains churn data for over 3,300 telecom customers. This dataset also contains customer attributes such as how much were they paying, how many minutes were used, did the customer have an international plan, and a number of other attributes as well.  My reason for building a predictive model is to solve what is known in data science as a classification problem. I want my model to learn from customer data and accurately classify future customers as falling into two binary groups:
Likely to 1.) Churn  2.) Not churn.  
# Exploratory Data Analysis
I began my EDA with data cleaning and visualizations to better understand the relationships between Churn and various customer attributes. 
The first thing I wanted to understand was what is the distribution of my target variable, churn.
![Churn Distribution](./images/Customer_Churn.jpg)
As visualized in the chart, the churn rate is just about 15%. This implies the dataset is disproportionate in that it has substantially more samples of customers without churn than customers with churn. Later in my analysis, I utilize SMOTE as an oversampling technique to account for this class imbalance. 


**For additional info, contact:**
- Zach Cherna: zacharycherna@gmail.com
