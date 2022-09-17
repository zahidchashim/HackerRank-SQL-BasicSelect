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
### 7) Weather Observation Station 3
Query a list of CITY names from STATION for cities that have an even ID number. Print the results in any order, but exclude duplicates from the answer.

Query:
```SQL
SELECT DISTINCT CITY 
FROM STATION 
WHERE MOD(ID,2) = 0
ORDER BY CITY;
```
---
### 8) Weather Observation Station 4
Find the difference between the total number of CITY entries in the table and the number of distinct CITY entries in the table.

Query:
```SQL
SELECT
    COUNT(CITY) - COUNT(DISTINCT CITY)
FROM STATION;
```
---
### 9) Weather Observation Station 5
Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.

Query:
```SQL
SELECT MIN(CITY), LENGTH(MIN(CITY)) FROM STATION 
WHERE LENGTH(CITY) = (SELECT MIN(LENGTH(CITY)) FROM STATION);
SELECT MAX(CITY), LENGTH(MAX(CITY)) FROM STATION 
WHERE LENGTH(CITY) = (SELECT MAX(LENGTH(CITY)) FROM STATION);
```
