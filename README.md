# Job-a-thon-Nov-2021
Problem Statement:

You are working as a data scientist with HR Department of a large insurance company focused on sales team attrition. Insurance sales teams help insurance companies generate new business by contacting potential customers and selling one or more types of insurance. The department generally sees high attrition and thus staffing becomes a crucial aspect.

To aid staffing, you are provided with the monthly information for a segment of employees for 2016 and 2017 and tasked to predict whether a current employee will be leaving the organization in the upcoming two quarters (01 Jan 2018 - 01 July 2018) or not, given:

Demographics of the employee (city, age, gender etc.)
Tenure information (joining date, Last Date)
Historical data regarding the performance of the employee (Quarterly rating, Monthly business acquired, designation, salary)

Leaderboard Rank - 114

Approach:

A snapshot of the data is provided under
![image](https://user-images.githubusercontent.com/89970618/142850640-1a398066-8cca-4e68-826c-b6391c0dc2cc.png)

As the objective was to predict if an employee will leave the organization in the upcoming two quarters, the target variable was taken such that if an employee leaves the organization within 180 days of review it was taken as 1 and 0 otherwise

Feature Engineering:
      
      In LastworkingDate column,they have given the lastworkingdate of some employees who have already left the organisation.so,i have taken those values as 1.
      Now i want to see the behaviour of the employees who have already left the organisation
      i have extracted the rows of employees who have left the organisation,then i have done analysis
      so, i observed people with same designation and with low quarterly rating have left the organisation more
     1. i have considered the features joining designation,designation,salary,quarterly rating,total bussiness value
     2.Applied get_dummies on joining designation and designation
     3.scaled down the values of salary and total bussiness value

Model Building:
   
    1. I  have used KMeans clustering algorithm to separate these employees 
    2. Most employees who have left the organisation fall in cluster 0,so i make that cluster as 1,which represents those employees are leave the organisation
       and cluster 1 as 0 who don't leave the organisation
       
 
