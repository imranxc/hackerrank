# Weather Observation Station 5

* [Weather Observation Station 5](https://www.hackerrank.com/challenges/weather-observation-station-5/problem) `easy`

Query the two cities in `STATION` with the shortest and longest `CITY` names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.

The STATION table is described as follows:

![table-description](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where `LAT_N` is the northern latitude and `LONG_W` is the western longitude.

**Note**: You can write two separate queries to get the desired output. It need not be a single query.

```sql
select CITY, length(CITY) as city_length
from STATION
order by length(CITY) asc, CITY asc limit 1;

select CITY, length(CITY) as city_length
from STATION
order by length(CITY) desc, CITY asc limit 1;
```
