# HackerRank-SQL-BasicSelect

Attempt on solving [HackerRank's SQL Challenge](https://www.hackerrank.com/domains/sql) - Topic: Basic SELECT

### Prepare > SQLBasic > Select
### 1) Revising the Select Query I
Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.

The CITY table is described as follows:
|Field|Type|
|---|---|
|ID|NUMBER|
|NAME|VARCHAR2(17)|
|COUNTRYCODE|VARCHAR2(3)|
|DISTRICT|VARCHAR2(20)|
|POPULATION|NUMBER|

Query:
```SQL
SELECT 
    *
FROM 
    CITY
WHERE POPULATION > 100000
AND COUNTRYCODE = 'USA';
```
---
### 2) Revising the Select Query II
Query the NAME field for all American cities in the CITY table with populations larger than 120000. The CountryCode for America is USA.

Query:
```SQL
SELECT
    NAME
FROM CITY
WHERE POPULATION > 120000
AND COUNTRYCODE = 'USA';
```
---
### 3) Select All
Query all columns (attributes) for every row in the CITY table.

Query:
```SQL
SELECT * FROM CITY;
```
---
### 3) Select By ID
Query all columns for a city in CITY with the ID 1661.

Query:
```SQL
SELECT * FROM CITY
WHERE ID = '1661';
```
---
### 4) Japanese Cities' Attributes
Query all attributes of every Japanese city in the CITY table. The COUNTRYCODE for Japan is JPN.

Query:
```SQL
SELECT * FROM CITY
WHERE COUNTRYCODE = 'JPN';
```
---

### 5) Japanese Cities' Names
Query the names of all the Japanese cities in the CITY table. The COUNTRYCODE for Japan is JPN.
The CITY table is described as follows:
|Field|Type|
|---|---|
|ID|NUMBER|
|NAME|VARCHAR2(17)|
|COUNTRYCODE|VARCHAR2(3)|
|DISTRICT|VARCHAR2(20)|
|POPULATION|NUMBER|

Query:
```SQL
SELECT NAME
FROM CITY
WHERE COUNTRYCODE = 'JPN';
```
---

### 6) Weather Observation Station 1
Query a list of CITY and STATE from the STATION table.
The STATION table is described as follows:
|Field|Type|
|---|---|
|ID|NUMBER|
|CITY|VARCHAR2(21)|
|STATE|VARCHAR2(2)|
|LAT_N|NUMBER|
|LONG_W|NUMBER|

where LAT_N is the northern latitude and LONG_W is the western longitude.

Query:
```SQL
SELECT CITY, STATE
FROM STATION;
```
---
