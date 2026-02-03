HR Employee Attrition Analysis — Power BI Project
Project Overview
The objective of this project is to analyze employee turnover (attrition) within an organization. By transforming raw HR data into interactive dashboards, we aim to identify patterns related to departments, age demographics, and compensation levels to help HR teams improve retention strategies.

Tools & Technologies
Data Source: WA_Fn-UseC_-HR-Employee-Attrition.csv (Excel/CSV format).
Data Cleaning: Power Query Editor (Power BI).
Data Visualization: Power BI Desktop.
Statistical Logic: Conditional columns and data modeling.

Data Transformation (Power Query Steps)
The following steps were performed to prepare the data for visualization:
Data Ingestion: Loaded the WA_Fn-UseC_-HR-Employee-Attrition.csv file into Power BI.

Column Management: Removed redundant or constant value columns such as EmployeeCount, Over18, and StandardHours to optimize the model.
Data Cleaning: Renamed headers for clarity (e.g., MonthlyIncome to Monthly Salary) and checked for missing values.
Datatype Correction: Ensured Age, MonthlyIncome, and DailyRate were set as Whole Numbers or Currency, while Attrition and Department were set as Text.

Feature Engineering (Conditional Columns):
Age Group: Created categories such as "Under 25", "25-34", "35-44", "45-54", and "55+" using the Age column.
Salary Band: Grouped MonthlyIncome into "Low" (<$5k), "Medium" ($5k-$10k), and "High" (>$10k).

Dashboard Visuals
1. Attrition by Department
Type: Clustered Bar Chart.
Axis: Department (Sales, R&D, HR).
Value: Count of Attrition (Filtered where Attrition = Yes).
Insight: Identifies which business units are losing the most talent.

2. Workforce Distribution by Age Group
Type: Pie Chart or Stacked Column Chart.
Legend: Age Group (Conditional Column).
Value: Count of Employees.
Insight: Displays the demographic balance of the workforce.

3. Salary Band Distribution
Type: Column Chart.
Axis: Salary Band (Low, Medium, High).
Value: Count of Employees.
Insight: Shows whether the majority of employees are in entry-level or senior pay brackets.

The IBM HR Analytics dataset was imported into Power BI and transformed using Power Query. Unnecessary columns such as EmployeeCount, Over18, StandardHours, and EmployeeNumber were removed, and column headers were renamed for better clarity. Data types were corrected, and the dataset was validated for missing values. Conditional columns for Age Group and Salary Band were created to enhance analysis. The transformed data was loaded into Power BI, and visuals such as Attrition by Department, Employee Distribution by Age Group, and Salary Band Analysis were created to derive HR insights

Final Results & Insights
Total Employee Records Analyzed: 1,470.
Key Finding: Workforce stability is centered in the 30–45 age bracket (Mid), which also receives the highest compensation.
Critical Area: The Research & Development department requires targeted retention strategies as it is the largest contributor to turnover metrics.

Reserach & development 971 employyes attrition, Sales has 446, Human resources 63. Reserach & development has the highest attrition and Human resourecs has the low attrition rate. 
Mid age has highest 871 employees with 59,.25%, Young age of 326 employees with 22.18%,  Senior age of 273 employees with 18.57%.
This insight has the Mid level has the highest salary and distribution and young has the lowest one. 


Future Improvements & Recommendations
To enhance this project further, the following steps are recommended:
DAX Measures: Create a % Attrition Rate measure (Total Attrition / Total Employees) to provide a more accurate comparison across departments of different sizes.
Job Satisfaction Analysis: Add a heatmap or radar chart comparing JobSatisfaction scores against Attrition to see if "soft" factors outweigh salary.
Predictive Modeling: Use Power BI’s "Key Influencers" visual to identify the top drivers behind why employees leave (e.g., Overtime or Distance from Home).
Trend Analysis: If date columns are available, add a Time-Series chart to see if attrition is seasonal or increasing year-over-year.
