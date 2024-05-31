# PowerBI-Telecom-Customer-Churn
## Customer Churn Analyzed Using Power BI

### Key Features
1. The churn, also known as the attrition rate or customer churn, is the rate at which customers stop doing business with an entity.
2. Churn rate = customers lost / total number of customers
- e.g. Churn rate = 10 / 100 = 10%

3. There are multiple ways to calculate churn<br>
- Varies by industry and revenue model.
- An e-commerce platform could e.g. define a churner as someone who hasn’t made a purchase in the last 12 months.

4. Importance of churn rate:<br>
- Allowing companies to measure competitiveness.
- It tells you exactly why customers are leaving.
- It is a rate at which customers stop doing business with an entity.

5. The Data:
- Dataset from Telecom Provider
-	One big table containing 29 columns
-	One row per customer

### Key Insights
1. Top 3 Churn Reasons:
-	Competitor made a better offer.
-	Competitors had better devices.
-	Attitude of support person.

2. The State with the highest Churn Rate:
-	CALIFORNIA 63.24%

3. The Churn Rate for Senior Citizens is significantly above the average:
-	38.46%

4. The age bracket with the highest number of customers churn rate is:
- 45

5. The churn rate for female customers in monthly-based contracts:
- 47.31%

6. The churn rate for people on an unlimited plan who consume less than 5 GB of data:
-	34.71%

7. Percentage of customers who actively make international calls but do not have an international plan:
-	72%

8. The churn rate for customers who are not in a group plan, who belong to the age group 50, and who have an account length of 12 months or less:
-	50.67%

9. The Churn rate for customers who are on a monthly contract and pay by debit card:
-	1.47
-	53.90%

10. Average extra data charges for customers who are on an unlimited data plan and consume 10 or more gigabytes:
-	31.19

### Some of the formulas used in Data Analysis Expressions (DAX):
1. Number of Customers = COUNT('Datalabel - Data'[Customer ID]
2. Number of Unique Customers = DISTINCTCOUNT('Databel - Data'[Customer ID])
3. Churned = IF('Databel - Data'[Churn Label] = "Yes", 1, 0)
4. Creating a measure for "Number of churned customers"
   Number of Churned Customers = SUM('Databel - Data'[CHURNED])
5. Calculating "Churn Rate"
   Churn Rate = [Number of Churned Customers] / [Number of Customers]
6. Demographics = if('Databel - Data'[Senior]="Yes","Senior", if('Databel - Data'[Under 30]="Yes","Under 30","Other"))
7. Contract Category = SWITCH('Databel - Data'[Contract Type], "One Year", "Yearly", "Two Year", "Yearly", "Monthly")
8. Grouped Consumption = IF('Databel - Data'[Avg Monthly GB Download] < 5, "Less than 5 GB", IF('Databel - Data'[Avg Monthly GB Download] < 10, "Between 5 and 10 GB", "10 or more GB"))
11. Avg Customer Service Calls per customer
   Avg Customer Service Calls = SUM('Datalabel - Data'[Customer Service Calls]) / [Number of Customer]
12. Avg Extra International Charges = SUM('Databel - Data'[Extra International Charges])/[Number of Customers]
13. Avg Extra Data Charges = SUM('Databel - Data'[Extra Data Charges]) / [Number of Customers]









  
