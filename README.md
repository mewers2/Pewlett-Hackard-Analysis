# Pewlett-Hackard-Analysis: The "Silver Tsunami"

## Project Overview
As baby-boomers begin to reach retirement, Pewlett-Hackard is preparing for the upcoming excessive turnover dubbed the "Silver Tsunami" as several thousand of their employees will become retirement eligible in a relatively short time period.  The purpose of this project is to create an employee database to analyze employee data to identify who will be reaching retirement age, what positions will need to be filled, and evaluate the prospect of a potential mentorship program during this time of transition to enable the company to make educated decisions in their human resources department to prepare for the upcoming turnover.

## Resources
- Data Source: departments.csv, dept_emp.csv, dept_manager.csv, employees.csv, salaries.csv, titles.csv
- Software: PostgreSQL 11.16, pgAdmin 4, Visual Studio Code, 1.68.1

## Results
- A Retirement Titles table was created.
  - This table holds all the titles of employees who were born between January 1, 1952 and December 31, 1955.

![retirement_titles](https://github.com/mewers2/Pewlett-Hackard-Analysis/blob/main/Resources/retirement_titles.png)

- A Unique Titles table was created.
  - This table uses the `DISTINCT ON` function to eliminate the multiple titles some employees may have had displayed in the Retirement Titles table and displays only the most recent title held by each employee listed.

![unique_titles](https://github.com/mewers2/Pewlett-Hackard-Analysis/blob/main/Resources/unique_titles.png)

- A Retiring Titles table was created.
  - This table uses the `COUNT()` function to summarize how many positions by job title will need to be filled based on the number of retirement-age employees and the job titles they currently hold.

![retiring_titles](https://github.com/mewers2/Pewlett-Hackard-Analysis/blob/main/Resources/retiring_titles.png)

- A Mentorship Eligibility table was created.
  - This table holds the current employees who were born between January 1, 1965 and December 31, 1965 who would be eligible to participate in a mentorship program where a retiring employee would mentor the junior employee to train him/her to fill the retiree's position.

![mentorship_eligibility](https://github.com/mewers2/Pewlett-Hackard-Analysis/blob/main/Resources/mentorship_eligibility.png)

## Summary
- There are 72,458 employees who are retirement-age and are eligible to retire during the "silver tsunami."  As the "silver tsunami" begins to take place, to make an impact on the employee deficit caused by the "silver tsunami," Pewlett Hackard HR may need to hire as many as 16,000 employees per year (over a three year timeframe) with a plan for the rest of the positions to be filled in the following 1-2 years.  

- Given that there are 72,458 employees who will retire as part of the "silver tsunami," and 1,549 employees eligible for the mentorship program, there are plenty of qualified retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees.  There are only two managers who are retirement-ready, so that may be one position title where the availability of mentorship is a little sparse.  

- The HR department may want to investigate the possibility of widening the mentorship eligibility criteria to include more junior employees in the mentorship program.  By adjusting the criteria to current employees born between January 1, 1962 and December 31, 1965 more current employees could benefit from the knowledge and experience of the retiring personnel.

- Another query to look at could be to group the retiring titles list by department to identify where all of those losses fall amongst the nine departments.

- Perhaps by re-querying the mentorship eligibility table and grouping it by department also, HR could better identify which departments will benefit most from the mentorship program.