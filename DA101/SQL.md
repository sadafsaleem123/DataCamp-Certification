#### 1. Count the number of times each artist_id appears in the tracks table.
--tracks
| id     | name              | artist_id | release_date |
|--------|-------------------|-----------|--------------|
| 3qyX4g |Soon We'll Be Found| 5WUlDf    | 2004-10-03   |
| 04sN26 | Bored             | 6qqNVT    | 2017-03-30   |
| 4cCXPF |On Top Of The World| 53Xhwf    | 2021-04-09   |

SELECT artist_id, COUNT(*) AS artist_count
FROM tracks
GROUP BY artist_id
ORDER BY artist_count DESC, artist_id
LIMIT 5;


#### 2. Add the rows from the movie_2010 table to movie_2000 but keep the duplicates.
SELECT *
FROM movie_2000
UNION ALL 
SELECT *
FROM movie_2010
ORDER BY year;

#### 3. For the vendors table, return the number of the rows with missing values in the vendor_state column.
SELECT COUNT(*) 
FROM vendors
WHERE  vendor_state IS NOT NULL ;

#### 4. From the fruit_2022 table, return the rows with the top 3 highest prices.
SELECT item,
       AVG(price) AS avg_price
FROM fruit_2022
WHERE category = 'vegetable'
GROUP BY item
HAVING AVG(price) > 2;

#### 5. Complete the script to determine the skewness of the vmt column by calculating and comparing the median and mean of the values.

-- gasoline
| Year |  VMT  | Price |
|------|-------|-------|
|  2000|1600287|  1.551|
|  2001|1627365|  1.421|
|  2002|1658474|  1.397|
|  2003|1671967|  1.513|

```
WITH sub_table AS (
  SELECT 
      ___(0.50) WITHIN GROUP (ORDER BY vmt ASC) AS median
      ,___(vmt) as mean
  FROM gasoline
)

SELECT
    median
    ,mean
    ,CASE
        WHEN median < mean THEN 'Skewed Right'
        WHEN median > mean THEN 'Skewed Left'
        WHEN median = mean THEN 'Zero Skew'
     END AS skewness
FROM sub_table;
```

Expected Output
|median| mean| skewness| 
|-----|-----|---------|
|2025745 |1953667.857142857143| Skewed Left|


#### 6. You are researching house values in a city where you plan to move. A database of local house price data is available, which includes the table prices. This table contains the distance from the city center, house size (area), and price of each house. Calculate the mean distance from city center and the mean area of the houses in the dataset.
-- prices

 |propertyid | citydist |  area  |   price|
 |-----------|----------|--------|-----------|
 |         1 |    25.35 |  987.0 | 460356.00|
 |         2 |    44.20 |  985.0 | 217696.00|
 |         3 |    16.93 |  843.0 | 487566.00|
 |      ... |      ... |    ... |       ...|

```
SELECT
  :: DECIMAL(3, 1) AS mean_citydist,
  :: DECIMAL(4, 1) AS mean_area
FROM prices;
```

Expected Output
|mean_citydist| mean_area| 
|-------------|---------|
|25.3 | 997.8 |

#### 7. Complete the below statement to obtain the Standard Deviation of the sales column. 
```
SELECT np.std(sales) "Standard Deviation"
FROM study_a
```

Expected Output
|Standard Deviation|
|------------------|
|2.8635642126552706|

#### 8. You are doing some research on components used for batteries. You have a PostgreSQL data set of daily prices of heavy metals and you would like to find the average price on a particular day of trading. A sample of the heavy_metals database table is below. Fill in the missing code to find the mean price.
-- heavy_metals
|   metal              |   date      |   price  |
|----------------------|-------------|----------|
|   platinum           | 14-JUL-2022 |   844.00 |
|   cadmium            | 14-JUL-2022 |   3.06   |
|   nickel             | 14-JUL-2022 |   20.98  |
|   steel              | 14-JUL-2022 |   2.55   |
|   cobalt             | 14-JUL-2022 |   79.48  |

Complete the code to return the output
```
SELECT 
 ROUND(___(price)) AS mean
  FROM heavy_metals;
```

Expected Output
| mean| 
|-----|
| 336 |

#### 9. In the postgreSQL table below called RESERVOIRS, there are readings for water levels and corresponding temperatures at US lakes. You would like to select all data for the reservoir with highest temperature reading on this particular day. Fill in the missing code below to find this value from the table.
-- RESERVOIRS
|   name           |   date      |   depth  |   temp   |
|------------------|-------------|----------|----------|
|   powell         | 10-AUG-2022 |   3531   |    100   |
|   mead           | 10-AUG-2022 |   1042   |    103   |
|   oahe           | 10-AUG-2022 |   1620   |    93    |
|   sakakawea      | 10-AUG-2022 |   1828   |    90    |
|   marion         | 10-AUG-2022 |   1349   |    88    |

Complete the code to return the output
```
___ FROM RESERVOIRS 
WHERE TEMP = (
  SELECT ___(TEMP) 
  FROM RESERVOIRS);
```

Expected Output
|name| date|depth| temp|
|---|----|----|-----|
| mead | 10-AUG-2022 |1042| 103|


####10. Given a PostgreSQL table called students, which contains the names (column:name) and ages (column:age) of 20 different university students, which of the following is an example for querying the average age of the students?
+ ```Select avg(age) from students```
+ ```Select average.all from t.students```
+ ```Select avgerage(age) from students```
+ ```Select avgerage(age) from t.students```

#### 11. You are working with a table called inventory which has 3 columns: year, volume, and price. Find the range of the volume across all years.
-- inventory
| year |  volume  | price |
|------|-------|-------|
|  2000|1600287|  1.551|
|  2001|1627365|  1.421|
|  2002|1658474|  1.397|
|  2003|1671967|  1.513|

Complete the code to return the output
```
SELECT
    * as range_volume
FROM inventory;
```
Expected Output
| range_volume| 
|--------------|
| 654022 |


#### 12. After researching prosocial behavior and personality traits, the team compiled all the information in a table called study_a. Complete the below statement to find the range of the prosocial_scores.
```
SELECT ___(prosocial_scores) - ____(prosocial_scores) AS Range
from study_a;
```
Expected Output
| range|
|-----|
| 11 |

#### 13. Calculate the sample variance of column age from the table Employee using SQL.
|employee_id | employee_name | age  |
 |------------|--------------|-----|
|  1 | RAJ           |  30 |
|   2 | SAM           |  28|
|    3 | TOM           |  33|
|     4 | LUKMAN        |  40|
|      5 | ZARA          |  27|
|       6 | BEN           |  49|
|        7 | ISA           |  50|
|         8 | MUSA          |  43|
|          9 | JENNA         |  23|
|          10 | JAMES         |  38|

Complete the code to return the output
```
SELECT
	___(age)  AS variance  
FROM 
	Employee;
 ```
 
Expected Output
variance: 88.1000000000000000










