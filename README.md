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

Sample Input

For example, CITY has four entries: DEF, ABC, PQRS and WXY.

Sample Output

ABC 3
PQRS 4

Explanation

When ordered alphabetically, the CITY names are listed as ABC, DEF, PQRS, and WXY, with lengths  and . The longest name is PQRS, but there are  options for shortest named city. Choose ABC, because it comes first alphabetically.

Note
You can write two separate queries to get the desired output. It need not be a single query.

**Solution**
```sql

*/select top 1 city, len(city) from station order by len(city) ASC, city ASC; 
select top 1 city, len(city) from station order by len(city) DESC, city ASC;
```

BASIC SQL PRACTICE 8

Query the Name of any student in STUDENTS who scored higher than 75 Marks. Order your output by the last three characters of each name. If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID.

Input Format

The STUDENTS table is described as follows:

![aeV5qC44](https://user-images.githubusercontent.com/124073659/216286131-ac6e932d-5463-4385-ba6b-993c87410d69.png)

Sample Output

Ashley
Julia
Belvet
Explanation

Only Ashley, Julia, and Belvet have Marks > 75. If you look at the last three characters of each of their names, there are no duplicates and 'ley' < 'lia' < 'vet'.

**Solution**
```sql
*/SELECT NAME FROM STUDENTS WHERE MARKS>'75' ORDER BY RIGHT(NAME,3),ID ASC;

```











































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

BASICE SQL PRACTICE

Write a query that prints a list of employee names (i.e.: the name attribute) for employees in Employee having a salary greater than 20000 per month who have been employees for less than 10 months. Sort your result by ascending employee_id.

**Solution**
```sql
*/SELECT NAME FROM EMPLOYEE WHERE SALARY >'2000' AND MONTHS <'10' ORDER BY EMPLOYEE_ID ASC;


```

BASIC SQL PRACTICE

Query the sum of Northern Latitudes (LAT_N) from STATION having values greater 38.7880 than  and less than 137.2345 . Truncate your answer to 4 decimal places.

Input Format

The STATION table is described as follows:

![tNqhUve6](https://user-images.githubusercontent.com/124073659/216449258-5bd7b3cc-07df-4a65-9d4e-a998e025e5fb.png)

**Solution**
```sql
*/SELECT ROUND(SUM(LAT_N),4) FROM STATION WHERE LAT_N > '38.7880' AND LAT_N< '137.2345';

```






