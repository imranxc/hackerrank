# The Blunder

* [The Blunder](https://www.hackerrank.com/challenges/the-blunder/problem) `easy`

Samantha was tasked with calculating the average monthly salaries for all employees in the `EMPLOYEES` table, but did not realize her keyboard's 0 key was broken until after completing the calculation. She wants your help finding the difference between her miscalculation (using salaries with any zeros removed), and the actual average salary.

Write a query calculating the amount of error (i.e.: `actual - miscalculated` average monthly salaries), and round it up to the next integer.

![EMPLOYEES](https://s3.amazonaws.com/hr-challenge-images/12893/1443817108-adc2235c81-1.png)

```sql
select
    ceiling(avg(SALARY) - avg(replace(SALARY, 0, "")))
from EMPLOYEES;
```
