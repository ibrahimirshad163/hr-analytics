Data Dictionary & Logic Reference
This project uses the standard MySQL sample database with custom business rules defined for analysis.

Core Definitions
Active Employee: Tracked using dept_emp.to_date = '9999-01-01', which indicates an open-ended current record.

Tenure: The total duration of employment in years, calculated from the hire date to either current date (CURDATE()) or department exit date.

Attrition: Triggered when an employee's department end date (to_date) is a valid calendar date rather than the active placeholder 9999-01-01.

Promotion: Counted when an employee has a new entry in the titles table starting after their initial hire date (title_changes > 1).

Flight Risk: Flagged for active employees who have been with the company for 5+ years without a single promotion.

Gender Pay Gap: Calculated as percentage difference: (Male Average Salary - Female Average Salary) / Male Average Salary * 100, measured at the department level.

Manager Pay Ratio: Manager salary divided by the average team salary (standard benchmark is 1.15 to 1.5).

Salary History Tracking
The salaries table keeps a complete historical log of pay changes.

Current Salary: Filter by to_date = '9999-01-01'.

Starting Salary: Filter by from_date = hire_date.

Department Reference
Code	Department Name
d001	Marketing
d002	Finance
d003	Human Resources
d004	Production
d005	Development
d006	Quality Management
d007	Sales
d008	Research
d009	Customer Service