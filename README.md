# Pwc_task3_Customer_Retention_Power_BI
Task 3: Customer Retention (Customer demographics and insights)

**Overview**

Task 3: Customer Retention This task requires you to define the appropriate KPIs for the retention manager based on the dataset. Create a dashboard for the retention manager reflecting the KPIs: This task requires you to create a dashboard that displays the defined KPIs for the retention manager to track the customer retention rate. Write a short email to him (the engagement partner) explaining your findings, and include suggestions as to what needs to be changed: This task requires you to write an email to the engagement partner, explaining the findings from the dashboard and providing suggestions on what needs to be changed to improve customer retention.

**Problem Statement**

The telecom Retention Manager has scheduled a meeting with the engagement partner at PwC to cover these points:

• Customers in the telecom industry are hard-earned: we don’t want to lose them.

• The retention department is here to get customers back in case of termination.

• Currently, we get in touch after they have terminated the contract, but this is reactionary: it would be better to know in advance who is at risk.

• We have done customer analysis with Excel: it has always ended in a dead-end.

• We would like to know more about our customers: visualised clearly so that it’s self-explanatory for our management.

Your colleague, the engagement partner, asks you to do the following tasks:

Define proper KPIs

Create a dashboard for the retention manager reflecting the KPIs

Write a short email to him (the engagement partner) explaining your findings, and include suggestions as to what needs to be changed

Here are some inputs:

• Customers who left within the last month

• Services each customer has signed up for: phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies

• Customer account information: how long as a customer, contract, payment method, paperless billing, monthly charges, total charges and number of tickets opened in the categories administrative and technical

• Demographic info about customers – gender, age range, and if they have partners and dependents

Data Cleaning and transformation for the dataset were done in power query as follows: • Each of the columns in the table was validated to have the correct data type • Unnecessary rows were removed

**Data preparation: -**

**Data Modelling**

After the dataset was cleaned and transformed, it was ready to be modelled. • The official dataset is marked as the 01 CHURN-Dataset table in the dataset.

• Along with this, a separate table- All Measuress is created to store all the measures which we have used in this model.

Data Visualization
Data visualization for the datasets was done in Microsoft Power BI Desktop:

• Demographic Info : Shows the male-female distribution,churn by senior citizen,dependents impact,partner impact effect of internet service provider recommendations and a short insight on the report

• Account Info : shows contrct type payment method tenuraity impact on customer count total charges, average monthly charges etc

• Services : shows customer count by streamingTV,customer count by streamingmovies,churn by phoneservice,online security device protection,Tech support etc

• Email / Insights and suggestion :Insights ans suggestions to the engagement partner explaining findings, and include suggestions as to what needs to be changed
Data Analysis

**Measures used in visualization are:**

% of Dependents = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Dependents]),'01 Churn-Dataset'[Dependents] = "Yes",'01 Churn-Dataset'[Churn] = "Yes"),CALCULATE(COUNT('01 Churn-Dataset'[Dependents]),'01 Churn-Dataset'[Churn] ="Yes"),0)

% of Partner = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Partner]),'01 Churn-Dataset'[Partner] = "Yes",'01 Churn-Dataset'[Churn] = "Yes"),CALCULATE(COUNT('01 Churn-Dataset'[Partner]),'01 Churn-Dataset'[Churn] ="Yes"),0)

% of Senior Citizen = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[SeniorCitizen] = 1,'01 Churn-Dataset'[Churn] = "Yes"),CALCULATE(COUNT('01 Churn-Dataset'[SeniorCitizen]),'01 Churn-Dataset'[Churn] ="Yes"),0)

churn rate % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[Churn]),'01 Churn-Dataset'[Churn] ="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[Churn]),ALLSELECTED('01 Churn-Dataset'[Churn])))

Online Backup in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[OnlineBackup] ="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineBackup]),'01 Churn-Dataset'[Churn]="Yes"),0)

Online sec in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[OnlineSecurity] ="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[OnlineSecurity]),'01 Churn-Dataset'[Churn]="Yes"),0)

Phone Service in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[PhoneService] ="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[PhoneService]),'01 Churn-Dataset'[Churn]="Yes"),0)

Streaming Movies in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[StreamingMovies] ="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingMovies]),'01 Churn-Dataset'[Churn]="Yes"),0)

Streaming TV in % = DIVIDE(CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[StreamingTV] ="Yes",'01 Churn-Dataset'[Churn]="Yes"),CALCULATE(COUNT('01 Churn-Dataset'[StreamingTV]),'01 Churn-Dataset'[Churn]="Yes"),0)


**Insights**

As shown by Data Visualization, It can be deduced that:

• Out of all the 7043 customers, 26.54 i.e overall 27 % of the customers churned last month.

• Customers having short tenure are more frequently switching than customers having longer tenure.

• If no Tech Support, Device Protection, and Online Security are provided then the chances of customers churning are high.

• payment method like Electronic check also makes a significant impact on the churning decision.

• There is no relation between gender with churning.

• senior citizens are less likely to churn rate.

• Customers with any dependents or partners are churning less likely, whereas the non-dependents and non-partners customers are more likely to shift.

• Tenure and contract play an important role in determining whether the customer will churn. Customers with monthly contracts i.e. lower tenure will switch frequently.

• Customers with Fiber Optic internet service will churn more compared to DSL internet service holders.

**Suggestions**

• Increasing the basic contract plan from 1 month to 3 months or 6 months can be a good starting point. This will help customers to be with us for a longer tenure.

• Starting special offers or schemes for customers who are single and have no family responsibility. They can become a permanent customer of the company. 'Catch them Young' is key to success here.

• provide some offers to the senior citizens as they are stable customers like overall offer some discounts on long tenure plans.

• Offering basic services like device protection, tech support, and online security should be the primary goal. This will help the customer stay longer with the brand.

**Dashboard images**


![Customer_retention_welcome](https://github.com/user-attachments/assets/285f77c6-8893-419a-bfdb-dca742076dc4)

![Customer_retention_churn](https://github.com/user-attachments/assets/dde54179-31c5-443a-bacd-1a4706e741a7)

![Customer_retention_Customer_Risk_Analysis](https://github.com/user-attachments/assets/d110d7ad-42fd-4fe9-b018-f600b7e79499)

![customer_retention_email_insights](https://github.com/user-attachments/assets/22510ab5-e46a-43a3-80c1-1e283d490304)
