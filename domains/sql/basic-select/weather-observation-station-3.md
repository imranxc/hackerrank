# Weather Observation Station 3

* [Weather Observation Station 3](https://www.hackerrank.com/challenges/weather-observation-station-3/problem) `easy`

Query a list of `CITY` names from `STATION` for cities that have an even `ID` number. Print the results in any order, but exclude duplicates from the answer.

The `STATION` table is described as follows:

![table-description](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where `LAT_N` is the northern latitude and `LONG_W` is the western longitude.

```sql
select distinct CITY 
from STATION
where ID % 2 = 0;

-- OR 

select distinct CITY 
from STATION 
where mod(ID, 2) = 0 
order by CITY desc;
```
