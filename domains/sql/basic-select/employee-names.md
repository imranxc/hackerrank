# Employee Names

* [Employee Names](https://www.hackerrank.com/challenges/name-of-employees) `easy`

Write a query that prints a list of employee names (i.e.: the name attribute) from the `Employee` table in alphabetical order.

The `Employee` table containing employee data for a company is described as follows:

![employee-table-description](https://s3.amazonaws.com/hr-challenge-images/19629/1458557872-4396838885-ScreenShot2016-03-21at4.27.13PM.png)

where `employee_id` is an employee's ID number, `name` is their name, `months` is the total number of months they've been working for the company, and `salary` is their monthly salary.

![table-data](https://s3.amazonaws.com/hr-challenge-images/19630/1458558612-af3da3ceb7-ScreenShot2016-03-21at4.32.59PM.png)

```sql
select name
from Employee
order by name asc;
```
