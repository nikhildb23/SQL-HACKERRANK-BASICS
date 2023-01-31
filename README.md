# SQL-HACKERRANK-BASICS
BASIC SQL PRACTICE


Query all columns for all American cities in the CITY table with populations larger than 100000. The CountryCode for America is USA.


The CITY table is described as follows:
| FIELD  |  TYPE  |
|--------|--------|
|  ID    |  NUMBER|
| NAME   | VARCHAR(17)|
| COUNTRYCODE | VARCHAR(3)|
| DISTRICT |  VARCHAR2(20) |
| POPULATION | NUMBER |

**Solution**
```sql


SELECT * FROM CITY WHERE POPULATION >'100000' AND COUNTRYCODE='USA';
```


































--------------------------------------------------------------------------------------------------------------------------------------------------------


SQL QUERY 
Query the list of CITY names starting with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates.

Input Format

The STATION table is described as follows:

|  FIELD  |  TYPE  |
|---------|--------|
|ID       | NUMBER |
|CITY     |VARCHAR(20)|
|STATE    |VARCHAR(2)|
|LAT_N    |NUMBER|
|LONG_W   |NUMBER|

where LAT_N is the northern latitude and LONG_W is the western longitude.

**Solution**
```sql


SELECT DISTINCT(CITY) FROM STATION
WHERE CITY LIKE 'A%' OR CITY LIKE 'E%' OR CITY LIKE 'I%' OR CITY LIKE 'O%' OR CITY LIKE 'U%';

```
--------------------------------------------------------------------------------------------------------------------------------------
SQL QUERY 
Query the list of CITY names ending with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.



**Solution**
```sql


SELECT DISTINCT(CITY) 
FROM STATION
WHERE CITY LIKE '%A' OR CITY LIKE '%E' OR CITY LIKE '%I' OR CITY LIKE '%O' OR CITY LIKE '%U'
```

------------------------------------------------------------------------------------------------------------------------------------------

SQL QUERY 

Query the list of CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates.

**Solution**
```sql


SELECT DISTINCT(CITY) FROM STATION WHERE ( CITY LIKE 'A%' OR CITY LIKE 'E%' OR CITY LIKE 'I%' OR CITY LIKE 'O%' OR CITY LIKE 'U%') AND (CITY LIKE '%A' OR CITY LIKE '%E' OR CITY LIKE '%I' OR CITY LIKE '%O' OR CITY LIKE '%U');

```
-----------------------------------------------------------------------------------------------------------------------------------------------


SQL QUERY
Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.
**Solution**
```sql

SELECT DISTINCT (CITY) FROM STATION WHERE CITY NOT LIKE 'A%' AND CITY NOT LIKE 'E%' AND CITY NOT LIKE  'I%' AND CITY NOT LIKE  'O%' AND CITY NOT LIKE 'U%' ;

```

SQL QUERY
Query the list of CITY names from STATION that do not end with vowels. Your result cannot contain duplicates.
**Solution**
```sql
SELECT DISTINCT(CITY) FROM STATION WHERE  CITY NOT LIKE '%A' AND CITY NOT LIKE '%E' AND CITY NOT LIKE '%I' AND CITY NOT LIKE '%O' AND CITY NOT LIKE '%U';
```


