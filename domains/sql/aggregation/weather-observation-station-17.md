# Weather Observation Station 17

* ![Weather Observation Station 17](https://www.hackerrank.com/challenges/weather-observation-station-17/problem) `easy`

Query the Western Longitude (`LONG_W`) where the smallest Northern Latitude (`LAT_N`) in `STATION` is greater than `38.7780`. Round your answer to 4 decimal places.

![station](https://s3.amazonaws.com/hr-challenge-images/9336/1449345840-5f0a551030-Station.jpg)

where `LAT_N` is the northern latitude and `LONG_W` is the western longitude.

```sql
select
    round(LONG_W, 4) as lon
from STATION
where LAT_N > 38.770
order by LAT_N
limit 1;
```
