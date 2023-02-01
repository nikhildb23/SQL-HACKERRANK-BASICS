# SQL-HACKERRANK-BASICS
BASIC SQL PRACTICE 1


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

BASIC SQL PRACTICE 2

Query the NAME field for all American cities in the CITY table with populations larger than 120000. The CountryCode for America is USA.

**Solution**
```sql
*/SELECT NAME FROM CITY WHERE POPULATION>120000 AND COUNTRYCODE='USA';

```
BASIC SQL PRACTICE 3

Query all attributes of every Japanese city in the CITY table. The COUNTRYCODE for Japan is JPN.

**Solution**
```sql
*/SELECT * FROM CITY WHERE COUNTRYCODE='JPN';
```

BASIC SQL PRACTICE 4

Query a list of CITY and STATE from the STATION table.

**Solution**
```sql
*/SELECT CITY,STATE FROM STATION;
```

BASIC SQL PRACTICE 5

Query a list of CITY names from STATION for cities that have an even ID number. Print the results in any order, but exclude duplicates from the answer.

**Solution**
```sql
*/SELECT DISTINCT CITY FROM STATION WHERE ID%2=0;

```
BASIC SQL PRACTICE 6

Find the difference between the total number of CITY entries in the table and the number of distinct CITY entries in the table.
**Solution**
```sql
*/SELECT COUNT(CITY)-COUNT(DISTINCT CITY) FROM STATION;

```
BASIC SQL PRACTICE 7

Query the two cities in STATION with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically.







































--------------------------------------------------------------------------------------------------------------------------------------------------------
BASIC SQL PRACTICE

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

BASIC SQL PRACTICE

Query the list of CITY names ending with vowels (a, e, i, o, u) from STATION. Your result cannot contain duplicates.



**Solution**
```sql


SELECT DISTINCT(CITY) 
FROM STATION
WHERE CITY LIKE '%A' OR CITY LIKE '%E' OR CITY LIKE '%I' OR CITY LIKE '%O' OR CITY LIKE '%U'
```

BASIC SQL PRACTICE

Query the list of CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates.

**Solution**
```sql


SELECT DISTINCT(CITY) FROM STATION WHERE ( CITY LIKE 'A%' OR CITY LIKE 'E%' OR CITY LIKE 'I%' OR CITY LIKE 'O%' OR CITY LIKE 'U%') AND (CITY LIKE '%A' OR CITY LIKE '%E' OR CITY LIKE '%I' OR CITY LIKE '%O' OR CITY LIKE '%U');

```



BASIC SQL PRACTICE

Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.
**Solution**
```sql

SELECT DISTINCT (CITY) FROM STATION WHERE CITY NOT LIKE 'A%' AND CITY NOT LIKE 'E%' AND CITY NOT LIKE  'I%' AND CITY NOT LIKE  'O%' AND CITY NOT LIKE 'U%' ;

```

BASIC SQL PRACTICE

Query the list of CITY names from STATION that do not end with vowels. Your result cannot contain duplicates.
**Solution**
```sql
SELECT DISTINCT(CITY) FROM STATION WHERE  CITY NOT LIKE '%A' AND CITY NOT LIKE '%E' AND CITY NOT LIKE '%I' AND CITY NOT LIKE '%O' AND CITY NOT LIKE '%U';


```

BASIC SQL PRACTICE

Write a query that prints a list of employee names (i.e.: the name attribute) from the Employee table in alphabetical order.

Input Format

The Employee table containing employee data for a company is described as follows:

![MwQdpOb1](https://user-images.githubusercontent.com/124073659/216010357-c151f4db-8357-46ce-bc26-3d3c6e04eb7b.png)
where employee_id is an employee's ID number, name is their name, months is the total number of months they've been working for the company, and salary is their monthly salary

![G6Waetp 2](https://user-images.githubusercontent.com/124073659/216010841-b8a065c7-f8c0-4394-bb99-7fbfb7e1c870.png)

![pATveQL3](https://user-images.githubusercontent.com/124073659/216011224-33aab483-5b70-4131-8d1c-5b2fcd81ae3e.png)

**Solution**
```sql
SELECT NAME FROM EMPLOYEE ORDER BY NAME;

```



