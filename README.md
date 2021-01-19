# Pewlett-Hackard-Analysis
## Overview of the Analysis
  The purpose of this assignment was to find the total number of employees that are going to retire according to their title. After finding the employees that will retire a table with employees that are eligible for a mentorship program. Finding the employees that are eligible for the mentorship program, all employees born between January 1,1965 and December 31, 1965.
## Results
* 30% of the workforce is eligible to retire at any given moment.
* The engineering department will be affected the most by the potential retirees. This means that Pewlett-Packard needs to hire new engineers, otherwise their development of newly engineered products will decrease significantly.
* 33% Staff, 31% Senior Engineer, 16% Engineer, 14% Senior Staff, 5% technique Leader, and 2% Assistant Engineer will be retiring.
* When taking a look at the mentorship program, the 1940 employees eligible for the mentorship will not cover the retiring employees.
## Summary
  The coming "silver tsunami", after running the query, about 90,398 employees will be able to retire. This means that a plan must be initiated as quickly as possible to makeup for the jobs that will be vacant. The mentorship program is considerably low, however there are enough employees to mentor the incoming employees. 
  
 There are 29415 Senior Engineers, 8047 Senior Staff, 4503 Engineers, and 4503 Technique Leaders that will be able to mentor.
  
 We could use this query to obtain the results listed above:
-- Use Count() to sum the titles of retiring employees
-- and create retiring_titles table.
SELECT count(title), title
into retiring_titles
from unique_titles
Group By title
order by count desc;
