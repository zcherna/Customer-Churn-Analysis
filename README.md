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
The first thing I wanted to understand was the distribution of my target variable, churn.

![Churn Distribution](./images/churn_distribution.jpg)

As visualized in the chart, the churn rate is just about 15%. This implies the dataset is disproportionate in that it has substantially more samples of customers without churn than customers with churn. Later in my analysis, I utilize SMOTE as an oversampling technique to account for this class imbalance. 

I then sought to visualize the distribution of the numeric data by creating a pair plot.

![pairplot](./images/pairplot.jpg)

With the exception of the 'area_code' and 'number_vmail_messages' columns, you can see how the data is normally distributed. There is also a strong positive linear relationship between 'total_day_minutes' and 'total_day_charge'; 'total_eve_minutes' and 'total_eve_charge"; 'total_night_minutes' and 'total_night_charge'; 'total_intl_calls' and 'total_intl_charge'. This may present an opportunity for feature engineering later on.

I then created a number of additional visualizations which can be viewed in the jupyter notebook, but the one that stood out the most to me was the the countplot that showed the proportion of customer churn given the presence or absence of an International Plan.

![International Plan](./images/intlplan2.jpg)

Starting on the left with customers who were signed up for plan, churn rate is only about 10%. Whereas on the right for customers who did not have a plan, churn rate is about 40%. This 30% decrease in churn tells me that the International Plan may be a great service that customers like and may be worth looking deeper into.

# Feature Engineering
As I mentioned when discussing the pairplot, there is a strong positive linear relationship between many of the features in the dataset as well as potential redundancy. For example, there are separate columns for "daytime calls", "evening calls", and "night calls". In order to visualize the aggregate of these features, I performed feature engineering. The histogram below is one example of the visualizations I created to examine the aggregate of a number of customer attribute features.

![Aggregate Charge](./images/aggcharge.jpg)

What stood out to me about this plot is you can see clearly that as total aggregate charge approaches that $75 mark, customer churn starts to surpass customer retention. This indicates that customers have limits on how much they're willing to pay. Churn increases for high paying customers.


**For additional info, contact:**
- Zach Cherna: zacharycherna@gmail.com
