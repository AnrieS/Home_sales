# Home_sales

This project required using spark sql in Google colab and using spark.sql queries to do data analysis

The Dataframe
| ID | Date | Date Built | Price | Bedrooms | Bathrooms | Sqft Living | Sqft Lot | Floors | Waterfront | View |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| f8a53099-ba1c-47d... | 2022-04-08 | 2016 | 936923 | 4 | 3 | 3167 | 11733 | 2 | 1 | 76 |
| 7530a2d8-1ae3-451... | 2021-06-13 | 2013 | 379628 | 2 | 2 | 2235 | 14384 | 1 | 0 | 23 |
| 43de979c-0bf0-4c9... | 2019-04-12 | 2014 | 417866 | 2 | 2 | 2127 | 10575 | 2 | 0 | 0 |
| b672c137-b88c-48b... | 2019-10-16 | 2016 | 239895 | 2 | 2 | 1631 | 11149 | 2 | 0 | 0 |
| e0726d4d-d595-407... | 2022-01-08 | 2017 | 424418 | 3 | 2 | 2249 | 13878 | 2 | 0 | 4 |
| ... | ... | ... | ... | ... | ... | ... | ... | ... | ... | ... |


# 3. What is the average price for a four bedroom house sold per year, rounded to two decimal places?

|YEAR_SOLD|AVERAGE_PRICE|
| --- | ---  |
|     2022|    296363.88|
|     2021|    301819.44|
|     2020|    298353.78|
|     2019|     300263.7|

# 4. What is the average price of a home for each year the home was built,
that have 3 bedrooms and 3 bathrooms, rounded to two decimal places?


|YEAR_BUILT|AVG_PRICE|
|----------|---------|
|      2010|297001.32|
|      2011| 300603.7|
|      2012|298451.99|
|      2013|302956.63|
|      2014|302426.89|
|      2015|299061.15|
|      2016|302937.87|
|      2017|300313.63|

# 5. What is the average price of a home for each year the home was built,
that have 3 bedrooms, 3 bathrooms, with two floors,
and are greater than or equal to 2,000 square feet, rounded to two decimal places?

|YEAR_BUILT|AVG_PRICE|
|----------|---------|
|      2010|301130.93|
|      2011|290688.58|
|      2012|319456.36|
|      2013|310510.69|
|      2014| 309821.9|
|      2015| 307147.8|
|      2016|300851.65|
|      2017|293281.74|


# 6. What is the average price of a home per "view" rating, rounded to two decimal places,
having an average home price greater than or equal to $350,000? Order by descending view rating. 
Although this is a small dataset, determine the run time for this query.


|VIEW_RATING| AVG_PRICE|
|-----------|----------|
|         99|1061201.42|
|         98|1053739.33|
|         97|1129040.15|
|         96|1017815.92|
|         95| 1054325.6|
|         94| 1033536.2|
|         93|1026006.06|
|         92| 970402.55|
|         91|1137372.73|
|         90|1062654.16|
|          9| 401393.34|
|         89|1107839.15|
|         88|1031719.35|
|         87| 1072285.2|
|         86|1070444.25|
|         85|1056336.74|
|         84|1117233.13|
|         83|1033965.93|
|         82| 1063498.0|
|         81|1053472.79|

only showing top 20 rows

--- 0.8067865371704102 seconds ---

# 9. Using the cached data, run the last query above, that calculates 
the average price of a home per "view" rating, rounded to two decimal places,
having an average home price greater than or equal to $350,000. 
Determine the runtime and compare it to the uncached runtime.
|VIEW_RATING| AVG_PRICE|
|-----------|----------|
|         99|1061201.42|
|         98|1053739.33|
|         97|1129040.15|
|         96|1017815.92|
|         95| 1054325.6|
|         94| 1033536.2|
|         93|1026006.06|
|         92| 970402.55|
|         91|1137372.73|
|         90|1062654.16|
|          9| 401393.34|
|         89|1107839.15|
|         88|1031719.35|
|         87| 1072285.2|
|         86|1070444.25|
|         85|1056336.74|
|         84|1117233.13|
|         83|1033965.93|
|         82| 1063498.0|
|         81|1053472.79|
|-----------|----------|
only showing top 20 rows

--- 2.4207892417907715 seconds ---


# 13. Using the parquet DataFrame, run the last query above, that calculates 
the average price of a home per "view" rating, rounded to two decimal places,
having an average home price greater than or equal to $350,000. 
Determine the runtime and compare it to the cached runtime.
|view|AVERAGE_PRICE|
|----|-------------|
|  99|   1061201.42|
|  98|   1053739.33|
|  97|   1129040.15|
|  96|   1017815.92|
|  95|    1054325.6|
|  94|    1033536.2|
|  93|   1026006.06|
|  92|    970402.55|
|  91|   1137372.73|
|  90|   1062654.16|
|  89|   1107839.15|
|  88|   1031719.35|
|  87|    1072285.2|
|  86|   1070444.25|
|  85|   1056336.74|
|  84|   1117233.13|
|  83|   1033965.93|
|  82|    1063498.0|
|  81|   1053472.79|
|  80|    991767.38|
only showing top 20 rows

--- 0.779369592666626 seconds ---
--- 0.779531717300415 seconds ---
