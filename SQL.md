# SQL

- CSV file,text file, excel file are all flat files
- Databases are easy to traverse and use for information access and manipulation.
- Databases use a technique called indexing with simple and easy to use language called SQL to achieve faster result.
- This is done using query language.
- Databases backup the data at multiple places to increase reliability.
- Eg; oracle, mysql, sql server


## Relational and non relational databases
- Relational databases (Traditional DBs from 1970s) , stores data in structured tables with rows and columns using predefined schemato clearly define relationships between data points.
- Eg; oracle, mysql, sql server


- Non relational Databases like mongodb offers more flexibility by storing data in various formats like documents, key-value pairs or graphs allowing for less structured and more dynamic data sets.

- RDB are ideal for highly structured data with complex queries, which non-relational databases excel in handling large volumes of diverse dat with rapid scalability needs

## Tables
- In RDB, data is stored across multiple tables TO AVOID DATA DUPLICATION.
- There is a primary key associated with each table.
 -  EG: imagine 3 tables
   <br> table1= movie_id, movie_name, year
    	<br>Primary key is movie_id
    <br>table2=actor_id,actor_name,gender
     	<br>Primary key is actor_id
    <br>table3=movie_id, actor_id
    <br>Here the movie_id and actor_id are Unique.

- SQL stands for structured query language
- Does 4 main actions- Create Read Update Delete or CRUD
- SQL is not a general purpose programming language, it is a domain specific language.
- Sql is used by data scientists, ML engineers , software engineers etc.
- SQL is a Declarative programming language whereas c++,python etc are procedural programming language, step by step instruction is provided
- Execution of an sql statement
 <br> The execution follows the following steps:
   <br> SQL-> Parser,compiler
    <br>Parser: tries to understand the query
    <br>Compiler: query optimiser (optimal way to execute) & generates code
    <br>->query executer->DB->results

* Refer SQLITE ipynb file

Eg: READ ing in sql

## Order of ease of learning: SELECT-DISTINCT-FROM-WHERE-ORDER BY-LIMIT-OFFSET
![](https://github.com/Gauthamnair-Ronin/ICTAK-1/blob/main/sql%20pics/pic1.png)


  - SELECT name FROM world;
<br>     - o/p= name column
  - SELECT name,population FROM world;
 <br>       - o/p= name column and pop column
  - SHOW tables;
 <br>       - o/p= shows all tables in db
  - DESCRIBE world;
 <br>       - o/p=shows the schema of the db
  - SELECT * FROM world LIMIT 2;
<br>        - op= shows 1st 2 rows from the table
  - SELECT * FROM world LIMIT 2 OFFSET 2;
 <br>       - op= shows 2 rows after numbr of offset rows
  - SELECT population FROM world WHERE name = 'France';
  <br>      - op=shows population of france
  - SELECT population,gdp  FROM world ORDER BY population DESC;
  <br>      - OP=shows pop and gdb in desc order  
  - SELECT name,gdp  FROM world  ORDER BY gdp LIMIT 5;
<br>        - OP= top 5 name and gdp in asc order 

  - SELECT DISTINCT continent FROM world  ;
    <br>    - op=unique continent names
  - SELECT name,continent FROM world WHERE continent<>'Asia';
<br>        - <> is not equal to. Comparing string need single quotes
  - SELECT * FROM world WHERE area<5000 AND population<2000
  - SELECT * FROM world WHERE name IN {‘Brazil’, ‘Russia’, ‘India’, ‘China’}
  - SELECT name, area FROM world  WHERE area BETWEEN 250000 AND 300000
  <br>      - BETWEEN is inclusive
  - SELECT name, population FROM world WHERE name LIKE "Al%"
   <br>       - op= name and pop where name starts with AI and can have any letters after that
    - SELECT name,length(name) FROM world WHERE length(name)=5 and region='Europe'
    <br>    - op=name and length of name from europe where length is to be 5
  - SELECT first_name FROM actors WHERE first_name LIKE ‘Agn_s’;
    <br>      - _ implies only at most one character
- If we want to match % or _ we should use backslash as an escape character: \% and \_

## Logical Operators
- AND, OR, NOT, ALL, ANY, BETWEEN, EXIST,IN, LIKE, SOME

<br>  - SELECT name, year, rankscore FROM movies WHERE rankscore>9 AND year> 200

# ___________________________________________________________________________________________________

The functions SUM, COUNT, MAX and AVG are "aggregates", each may be applied to a numeric attribute resulting in a single row being returned by the query. (These functions are even more useful when used with the GROUP BY clause.)

### Having

GROUP BY and HAVING
<br>By including a GROUP BY clause functions such as SUM and COUNT are applied to groups of items sharing values. When you specify GROUP BY continent the result is that you get only one row for each different value of continent. All the other columns must be "aggregated" by one of SUM, COUNT ...
The HAVING clause allows use to filter the groups which are displayed. The WHERE clause filters rows before the aggregation, the HAVING clause filters after the aggregation.
If a ORDER BY clause is included we can refer to columns by their position.
- e.g. SELECT year, COUNT(year) year_count FROM movies GROUP BY year HAVING year_count>1000;

# Order of KEYWORDS
 - https://dev.mysql.com/doc/refman/8.4/en/select.html


 - SELECT * FROM WHERE G-H-O-L






### Order of execution
- Group by to create grps
- Apply aggregate
- Apply having condition
### JOIN
  -combine data in multiple tables
- INNER join

Eg:
SELECT TableA_ID, TableA_name,Table_Course 
FROM TableA
INNER JOIN TableB
ON TableA_ID=TAbleB_ID

- Left join
- Right join
- Full outer join
- Natural join
      - Same as inner join but we dont have to mention which columns to join


SELECT m.name, g.genre
FROM movies m
JOIN movie_genre g
ON m.id=g.movie_id
LIMIT 20;

  - here m and g are table alises
    - Natural join: a join where the same column-names across two tables
    - T1: C1, C2
    - T2: C1, C3, C4
    - SELECT * FROM T1 JOIN T2;
    - SELCECT * FROM T1 JOIN T2 USING (C1);
    - returns C1, C2, C3, C4


* USE HACKERRANK SQL SECTION * 

- Nested QUERY
	SELECT actor_id FROM roles WHERE movie_id IN (SELECT id FROM movies WHERE name=’Schindlers List’)
IN, NOT IN, EXISTS, NOT EXISTS, ANY, ALL, Comparison operators
ANY operator returns true if any of the subquery values meet the condition
ALL operator returns true if all of subquery values meet the condition

### CREATE, READ, UPDATE, DELETE (CRUD)

- CREATE
    - CREATE TABLE table_name (
    col1 col1_dtype,
    col2 col2_dtype,
    );

CREATE TABLE students (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    grade CHAR(1)
);

###  INSERT

   - INSERT INTO movies(id, name, year, rankscore) VALUES (412321, 'Thor', 2011, 7);

  - INSERT INTO movies(id, name, year, rankscore) VALUES (412321, 'Thor', 2011, 7),
                                                           (412322, 'Iron Man', 2008, 7.9),
                                                           (412323, 'Iron Man 2', 2010, 7);

###  UPDATE

  - UPDATE <TableName> SET col1=val1, col2=val2 WHERE condition;
    - UPDATE movies SET rankscore=9 where id=412321;
    - Can be used to update multiple rows at once



### ALTER: 

The ALTER TABLE statement is used to modify the structure of the table.
    - Adding new columns
        - ALTER TABLE students 
          ADD email VARCHAR(100);
    - Rename column
        - ALTER TABLE students 
         RENAME COLUMN grade TO final_grade;




### DELETE
  - DELETE FROM movies WHERE id=412321


### DROP
  - Deletes both tableand all of the data permanently
    - DROP TABLE Tablename;
    - DROP TABLE tablename IF EXISTS;

### TRUNCATE
- TRUNCATE delete the contents of the table but the not the table
    - where as DROP deletes the whole table itself
    - TRUNCATE TABLE tablename;


# EXAMPLES
![](https://github.com/Gauthamnair-Ronin/ICTAK-1/blob/main/sql%20pics/pic2.png)
