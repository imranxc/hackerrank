# Weather Observation Station 7

* [Weather Observation Station 7](https://www.hackerrank.com/challenges/weather-observation-station-7/problem) `easy`

Query the list of `CITY` names ending with vowels (a, e, i, o, u) from `STATION`. Your result cannot contain duplicates.

The `STATION` table is described as follows:

![station-table](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where `LAT_N` is the northern latitude and `LONG_W` is the western longitude.

```sql
select distinct CITY
from STATION
where CITY regexp "[aeiou]$";

-- OR

select distinct CITY 
from STATION 
where right(CITY, 1) in ("a", "e", "i", "o", "u");
```
