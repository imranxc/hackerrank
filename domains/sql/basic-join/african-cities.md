# African Cities

* [African Cities](https://www.hackerrank.com/challenges/african-cities/problem) `easy`

Given the `CITY` and `COUNTRY` tables, query the names of all cities where the `CONTINENT` is 'Africa'.

Note: `CITY.CountryCode` and `COUNTRY.Code` are matching key columns.

The `CITY` and `COUNTRY` tables are described as follows:

![city](https://s3.amazonaws.com/hr-challenge-images/8137/1449729804-f21d187d0f-CITY.jpg)

![country](https://s3.amazonaws.com/hr-challenge-images/8342/1449769013-e54ce90480-Country.jpg)

```sql
select 
    c.NAME
from CITY as c 
join COUNTRY as co
on c.COUNTRYCODE = co.CODE
where co.CONTINENT = "Africa";
```
