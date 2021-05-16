# [Project 2: EDA on Employee Attrition & Performance](https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset)

Using the dataset IBM HR Analytics, this project in an Exploratory Data Analysis (EDA) showing how to analyze attrition within your company. This project aims to identify the reasons pushing top performer employees to leave the company. By building a visual dashboard, company's decision-makers can assess the situation and answer questions such as:  
  
- Show me a breakdown of distance from home by job role and attrition
- Compare the average monthly income by education field and attrition
  
This project was realized during my **#20daysDataScience2021** challenge so you will find the code in the following links:  
- [Day 12](https://github.com/SandratraR/20Days_DataScience_2021/blob/master/Day12.py)
- [Day 13](https://github.com/SandratraR/20Days_DataScience_2021/blob/master/Day13.py)
- [Day 14](https://github.com/SandratraR/20Days_DataScience_2021/blob/master/Day14.py)
  
## Exploratory Data Analysis  
The first step is to observe the distribution of attrition accross all the employees and departments to have a general overview. This is why I have started with this facet grid based on the columns **Age**, **Department**, **Gender** and **Attrition**.  
  
![Facet_grid_attrition](/images/FacetGrid_AttritionAge_per_Department.png)  
  
*The Research & Development department is the one with the highest rate of attrition in the company. We can see that R & D 
employees between 25 and 35 years old tends to leave the company. Attrition concerns more men than women with an attrition 
rate above 15 where its barely break 10 for women.*  
  
Continuing our analysis let's look at the first possible criterion: **Distance from home** accross all the job role. We have already identified the Research & Development department, therefore by using **Job Role** we can see in more detail how the attrition is distributed accross the roles.  
  
![Box_plot_distance_role](/images/Stripplot_Distance_JobRole.png)  
    
*Attrition (represented by violet dots) seems to concerns mainly Research Scientists, Laboratory Technicians, Sales Executives, and Sales Representatives. Both Distance from home doesn't seem to have an impact on attrition. We have employees living less than 10 km away from the office and employees living
over 20 km away both leaving the company.*  
  
This confirms our first observations but **Distance from home** is not a main factor of attrition. Moving on, we will analyze if **Monthly Income** can have an impact on attrition. First, I have calculated the **Average Monthly Income** for each **Education Field** so that we can assess where each employee stands in comparison to the mean.  
  
![Scatterplot_distance_income](/images/scatterplot_income_education.png)  
  
*Most of the employees who left the company (represented by orange dots) were paid under the average monthly income of their Education Field. So we can 
suppose that Monthly Income can be a cause of attrition among the employees who have a Life Sciences, Medical, Marketing or 
Technical Degree.*  
  
The employees seem to leave the company for financial motives according to our previous graph. Let's see if the attribution of Promotion confirms that trend among the employees.
We will also check if employee's number of years at the company is related to promotion's attribution and attrition as well.  
  
![kde_promotion_yearsatcompany](/images/promotion_vs_years.png)
  
*The promotion doesn't seem to be a reason for attrition because we can observe that the cluster of attrition concerns employees
who recently received a promotion and joined the company for less than 5 years. We can conclude that recent employees tend 
to leave but they also represents most employees of this company. The density on both KDE's graphs confirms that observation. This company struggles to keep its newcomers.*
