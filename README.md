# Pewlett-Hackard-Analysis

## Overview and Purpose:
The purpose of this analysis is to create two tables: 
- to determine the number of retiring employees and their position titles, 
- to identify employees who are eligible to participate in a mentorship program. 

## Results:
An entity relationship diagram was created using quick database diagrams to gather and organize the key elements from various data tables. 
The data was imported using Postgres and the pgAdmin interface.  
SQL queries were written to create data tables by joining primary keys from different data sets together and establishing foreign keys.  
SQL queries were created to generate a list of retiring employees by title and a list of employees eligible for mentorship.

1. Employee database relationship diagram for Pewlett Hackard:
![Pic 1](https://github.com/Akotovets1/Pewlett-Hackard-Analysis/blob/main/EmployeeDB.png)

2. A Retirement Titles table was made that holds all the titles of employees who were born between January 1, 1952 and December 31, 1955:

![Pic 2](https://github.com/Akotovets1/Pewlett-Hackard-Analysis/blob/main/retirement_titles.png)

But there were many duplicate entries because some employees had multiple titles in the database.

3. Using the 'distinct on' SQL script, the duplicates were removed leaving the most recent job title to create a unique list of retiring employees:

![Pic 3](https://github.com/Akotovets1/Pewlett-Hackard-Analysis/blob/main/unique_titles.png)

4. Then a Retiring Titles table was created

![Pic 4](https://github.com/Akotovets1/Pewlett-Hackard-Analysis/blob/main/retiring_titles.png)


5. Finaly a Mentorship-eligibility table was created that holds the current employees who were born between January 1, 1965 and December 31, 1965:

![Pic 5](https://github.com/Akotovets1/Pewlett-Hackard-Analysis/blob/main/mentorship_eligibilty.png)

## Summary: 

### How many roles will need to be filled as the "silver tsunami" begins to make an impact?
Thre will be 90,398 vacancies that will need to be filled. 

### Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
There are 1,549 employees eligible for mentorship program.
There are 90,398 vacancies that will need to be filled.
So the gap is significant. It looks like Pewlett Hackard does not have enough retirees to mentor the next generation of employees. 

It would be useful to have a query that indicates a list of employees who will be retired for each following year.
It could help Pewlett Hackard to prepare better for the "silver tsunami".
Also we could create a query that indicates salaries of all retiring employees.
