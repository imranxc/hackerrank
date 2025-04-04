# Weather Observation Station 13

* [Weather Observation Station 13](https://www.hackerrank.com/challenges/weather-observation-station-13/problem) `easy`

Query the sum of Northern Latitudes (`LAT_N`) from `STATION` having values greater than `38.7880` and less than `137.2345`. Truncate your answer to 4 decimal places.

![station](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where `LAT_N` is the northern latitude and `LONG_W` is the western longitude.

```sql
select
    round(sum(LAT_N), 4) as lan
from STATION
where LAT_N between 38.7880 and 137.2345;

-- OR

select
    round(sum(LAT_N), 4) as lan
from STATION
where LAT_N > 38.7880 and LAT_N < 137.2345;
```
