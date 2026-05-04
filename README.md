**⚙️ HR Analytics: Data Modeling & DAX Implementation**
**📝 Project Overview**
This repository contains a comprehensive Human Resources Analytics dashboard. While the front-end provides interactive visualizations of employee attrition and satisfaction, the core of this project lies in its robust data model and custom DAX (Data Analysis Expressions) calculations.

The goal of this project was to transform raw human resources data into an optimized, relational data model capable of supporting complex time-intelligence and categorical analysis.

**🗄️ Data Architecture & Modeling**
Data Cleaning: Raw data was ingested and cleaned using Power BI. Handled missing values, standardized departmental naming conventions, and formatted data types for performance optimization.

Data Model: Built using a standard Star Schema to ensure efficient filtering and cross-filtering across visuals.

Fact Table: Employee_Metrics (Contains employee IDs, performance scores, salary data, and attrition status).

Dimension Tables: Dim_Department, Dim_JobRole, Dim_Calendar (for time-series analysis on employee tenure).

**🧮 Key DAX Measures**
Custom measures were created to dynamically calculate KPIs regardless of the filter context applied by the user. Examples include:

Total Employees: Total Employee = DISTINCTCOUNT(Employee_Metrics[EmployeeID])

Employee Left: Employee Left = CALCULATE([Total Employee], Employee_Metrics[Attrition] = "Yes")

Attrition Rate: Attrition Rate = DIVIDE([Employee Left], [Total Employee], 0)

Sum of Salary: Sum of Salary = SUM(Employee_Metrics[Salary])

**📊 Visual Analytics & UI**
The front-end was designed with a focus on user experience and data clarity:

Card Visuals: High-level executive KPIs prominently displayed.

Clustered Bar & Column Charts: Used to cleanly compare discrete categories (e.g., Employee Left by Department and Count of Job Role by Performance Score).

Scatter Plot: Deployed to identify correlations between dual numeric variables (Sum of Salary vs. Performance Score).

Line & Clustered Column Chart: Used to track the distribution of the workforce alongside tenure (Total Employee by Years At Company).

**🚀 Technologies Used**
Reporting & Visualization: Power BI Desktop

Data Transformation: Power Query (M Formula Language)

Calculations: DAX

Database/Storage: https://1drv.ms/x/c/38e6f2af47a8e4ba/IQCQIgchUPU-Tbt5x4vwbwuzAUIyT6fnAhXlwfRV6BEgZ4k?e=TmjjSh

Power BI:https://1drv.ms/x/c/38e6f2af47a8e4ba/IQCQIgchUPU-Tbt5x4vwbwuzAUIyT6fnAhXlwfRV6BEgZ4k?e=TmjjSh
<img width="1361" height="734" alt="Screenshot 2026-05-04 134558" src="https://github.com/user-attachments/assets/bcbae083-55c0-4d00-a1fc-c2f47fa56595" />

