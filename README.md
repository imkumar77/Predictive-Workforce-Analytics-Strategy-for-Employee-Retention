# Predictive-Workforce-Analytics-Strategy-for-Employee-Retention
Novotel implements predictive analytics to enhance employee retention. By analyzing data and developing personalized interventions, they create a stable workforce, ultimately boosting customer satisfaction and business success.
# 🧠 Predictive Workforce Analytics for Employee Retention - Novotel Case Study

This project is based on my MBA thesis and focuses on the use of predictive analytics to understand and improve employee retention at Novotel, a global leader in the hospitality industry. Using data-driven insights and machine learning models, we identify patterns of attrition and recommend personalized interventions.

---

## ✅ Project Overview

High employee turnover is a major challenge in the hospitality industry. This project leverages historical employee data and predictive modeling to forecast attrition and suggest retention strategies. The analysis is based on data from Novotel and covers demographics, job roles, satisfaction, compensation, and more.

---

## 🎯 Objectives

- Analyze factors contributing to employee turnover.
- Use machine learning models to predict attrition risk.
- Visualize insights for easy stakeholder interpretation.
- Recommend targeted HR interventions for retention.
- Build a reproducible and interactive dashboard using Streamlit.

---

## 🛠️ Technologies Used

- **Languages**: Python
- **Libraries**: pandas, seaborn, matplotlib, scikit-learn, streamlit
- **ML Models**: Random Forest Classifier
- **Statistical Tools**: Z-Test, Chi-Square Test
- **Platforms**: Jupyter Notebook, Streamlit

---

## 📂 Dataset Summary

A sample anonymized dataset includes:
- **Demographics**: Age, Gender
- **Employment**: Department, Job Role, Years at Company
- **Performance**: Monthly Income, Job Satisfaction, Overtime
- **Target Variable**: `Attrition` (Yes/No)

Example schema:

| EmployeeID | Age | Department | Gender | MonthlyIncome | JobSatisfaction | YearsAtCompany | Attrition |
|------------|-----|------------|--------|----------------|------------------|----------------|-----------|
| 101        | 35  | Sales      | Male   | 45000          | 3                | 5              | No        |
| 102        | 29  | HR         | Female | 38000          | 2                | 2              | Yes       |

---
## DATA ANALYSIS AND INTERPRETATION
**Description of the dataset**
![{624D80FE-333E-4FE0-B4E6-5456C37CA654}](https://github.com/user-attachments/assets/6ad0d4e7-f311-4696-928b-413ab220f398)


**: Employee attrition stats**
![{992F46A0-DF54-489C-BAD1-0A6B699CDC58}](https://github.com/user-attachments/assets/bfad7048-1e3f-42af-be26-ed8df0eb1a73)
-- **16.1%** of employees are no longer with the company (attrition).
-- **83.9%** are still employed.
-- This is your overall attrition rate—a critical business metric in HR analytics.
-- A healthy attrition rate varies by industry, but 16.1% could indicate potential concerns, especially in a service-driven sector like hospitality.

**Attrition by department**

![{1B1ED6DF-7D6E-43E8-8E91-0FDE06A4CD6D}](https://github.com/user-attachments/assets/c3211d78-53b4-4d8d-8415-d32553ccdc6d)
--Most attrition is happening in R&D, followed by Sales.
--Human Resources has the least attrition.
-- This may indicate role-based dissatisfaction, leadership issues, or a misalignment between job expectations and daily tasks in R&D and Sales.

**Attrition rate by Job satisfaction**
![{DD27EEBD-7BA0-47F9-B13C-3CD3B8047A08}](https://github.com/user-attachments/assets/19ee93f4-d1a2-49d1-8e34-e5c19ef78ce2)
--Employees who seem satisfied (rated 'Good') may still be at risk, indicating a need for deeper qualitative feedback.
--Focus on converting “Good” to “Excellent” by providing better career development, rewards, and work-life balance.
--"Neutral” employees are a critical segment to target for engagement initiatives—they're the easiest to retain or lose.

**Correlation matrix of the dataset**
![{D40106D7-AA04-4D74-A6E8-5974099757CB}](https://github.com/user-attachments/assets/b6836661-e23d-4ce0-a870-e92ca52d906e)
-- Confirming our findings in the scatterplot above, MonthlyIncome has a strongpositive correlation to Total Working Years of **0.77**.
-- Additionally, YearsAtCompany has a strong positive association with YearsWithCurrManager **(correlation = 0.77)**as well as with YearsInCurrentRole **(correlation = 0.76)**.
-- There are no variables with a correlation above **0.8**,indicating a potential collinearity issue.

## Hypothesis Testing
-- ** Z - Test**
![{0EBF0E6D-4455-4AC2-B6FC-078556957AD6}](https://github.com/user-attachments/assets/87c15761-ffbb-4acb-b86a-c5c13a23e0a6)
--Z-statistic:
-- The Z-statistic is -7.4826, indicating how many standard deviations the difference between the means of the two groups is away from zero.
--  A negative value suggests that the Monthly Income of Former Employees is significantly lower than that of Current Employees.

-- P-value:
--  The p-value is 7.2831e-14, an extremely small value.
--  This low p-value provides strong evidence against the null hypothesis, indicating a statistically significant difference in Monthly Income between the two groups.

**Chi-Square Test of Independence**
![{259BB85A-51B8-44FA-9D1D-571E1E78AD19}](https://github.com/user-attachments/assets/edbcd58c-bdda-4653-ae59-8161b7ec75e4)
-- Attrition and Education are independent (p-value = 0.55).
-- Attrition and Gender are independent (p-value = 0.29).
-- Attrition and PerformanceRating are independent (p-value = 0.99).
-- Attrition and RelationshipSatisfaction are independent (p-value = 0.15).

**Attrition based on Random forest modelling**
![{813C12F8-4BA9-411A-A0FC-191B5FCCECA0}](https://github.com/user-attachments/assets/bfe96863-5dc2-41aa-b9ba-0d4554443856)
-- **Validation Accuracy**: 83.6% and AUC = 0.773
-- **Test set Accuracy**: 84.2% and AUC = 0.816


##  Key Findings

- 📌 **16%** attrition rate overall.
- 💼 **Overtime**, **Monthly Income**, and **Job Satisfaction** are strong predictors.
- 🔍 Women in HR and men in Sales show higher attrition risk.
- 🔥 Random Forest model achieved:
  - **Validation Accuracy**: 83.6%
  - **Test Accuracy**: 84.2%
  - **AUC**: 0.816
- 🎯 Actionable features:
  - Monthly income
  - Total years of work
  - Distance from home
  - Manager relationship

 ##   CONCLUSION
--This study presents a comprehensive examination of employee attrition within the organization, revealing several critical insights and patterns:
-- The overall attrition rate of 16% indicates a dynamic workforce, with distinct trends across departments. Research & Development shows significantly higher turnover, while Human Resources maintains lower attrition levels.
-- Gender-based differences were observed: attrition is higher among women in HR and men in Sales, suggesting department-gender interactions may influence turnover.
-- Interestingly, a majority of departing employees reported job satisfaction, which implies that factors beyond contentment—such as compensation disparities, lack of growth, or work-life imbalance—play a role in their decision to leave.
-- Salary inequities across genders and roles emerged as a potential area for HR intervention. A Z-test on Monthly Income confirmed a statistically significant difference between former and current employees.
--Strong correlations were observed between MonthlyIncome and TotalWorkingYears, reinforcing the influence of experience on compensation—and potentially on attrition.

--Predictive modeling using Random Forest identified key factors impacting attrition, including:
-Monthly Income
-Age
-Years at Company
-Overtime
-Stock Options
-Job Satisfaction
-Departmental Affiliation
--The model performed robustly across both validation and test sets, achieving high accuracy and AUC, supporting its use as an early-warning tool for HR professionals.

##  SUGGESTIONS
--**Tailored Retention Strategies**
-Develop targeted retention programs based on the identified factors influencing attrition, such as work-life balance, job satisfaction, and overtime. Customize initiatives for different departments to address specific concerns.
-- **Employee Engagement Initiatives**
  -Implement initiatives to boost overall jobsatisfaction, considering the positive correlation between satisfaction and retention. Regular feedback mechanisms, recognition programs, and professional development
opportunities can contribute to a more engaged workforce.
-- **Flexible Work Arrangements**
- Recognize the impact of work-life balance on attrition. Explore flexible work arrangements, remote work options, or compressed workweeks to accommodate diverse employee needs and promote a healthier worklife balance.
-- ** Overtime Management**
   -Address concerns related to working overtime, as indicated by its significance in predicting attrition. Evaluate workload distribution, assess resource allocation, and consider measures to manage and minimize overtime demands.
-- **Competitive Compensation**
  -Given the importance of monthly income in predicting attrition, ensure that the company's salary structure remains competitive within the industry. Regularly review and adjust compensation packages to reflect market trends.


