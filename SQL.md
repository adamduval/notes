# SQL

# Log
20220926 - mode tutorial SQL Like statement

# Resources
## Websites
- Mode [mode.com/sql-tutorial](http://mode.com/sql-tutorial)  
- SQLBolt [sqlbolt.com](http://sqlbolt.com/)  
- SQLCourse [sqlcourse.com](http://sqlcourse.com/)  
- SQL-ex [sql-ex.ru](http://sql-ex.ru/)  
- SQLZoo[https://sqlzoo.net](https://sqlzoo.net)    
- Modern SQL [modern-sql.com](http://modern-sql.com/)  
- PostgreSQL Exercises [pgexercises.com](http://pgexercises.com/)  
- The PostgreSQL Docs [https://www.postgresql.org/docs/9.2/sql.html](https://www.postgresql.org/docs/9.2/sql.html)  
- Select Star SQL [selectstarsql.com](http://selectstarsql.com/)  
- Use the index Luke [use-the-index-luke.com](http://use-the-index-luke.com/)  
- Schemaverse [schemaverse.com](http://schemaverse.com/)  
- SQL Teaching [sqlteaching.com](http://sqlteaching.com/)  
- W3Schools [w3schools.com/sql](http://w3schools.com/sql)

## Courses
- Stanford DB Course [https://www.edx.org/course/databases-5-sql](https://www.edx.org/course/databases-5-sql)  

# What is SQL?
- Structured Query Language 
- Designed for managing data in a relational database

# SQL Syntax

## Keywords

### AS (alias)
- used to rename a column or table with an alias
- only exists in the query, does not change the table
- if the alias name contains a space it needs to be in double quotes  
```
SELECT west AS "West_Zone"  
    FROM table_name
```
- if the alias name needs capital letters it must also be in double quotes

### Arithmetic Operators
`+` addition  
`-` subtraction  
`*` multiplication  
`/` division  
`%` modulo (gives remainder)  
- typical math operations  
- can be used with numerical or non numerical data
- can only be used on values in a given row
- aggregate operations must be used to add values across multiple rows

### Comparison Operators
`=` equal to  
`<>`, `!=` not equal to
`>` greater than  
`<` less than
`>=` greater than or equal to
`<=` less than or equal to
- work as expected with numerical data
- if using non numerical data then the comparison value must be in single quotes
- non numerical data works best with the equal operator
- other operators work but SQL will filter based on alphabetical order  
    - think about dictionary order Ja > J so 'value' > J would include Ja and so on

### Logical Operators
`LIKE` match similar values instead of exact ones  
`IN` specify if a value is in a list of values  
`BETWEEN` select rows in a certain range  
`IS NULL` select rows with no value in a certain column  
`AND` chain multiple conditions  
`OR` select rows that satisfy one condition or another  
`NOT` select rows that do not match a condition  

### LIMIT
- limits how many rows the query returns
```
SELECT *
    FROM table_name
    LIMIT 100
```

### FROM
- Always required in a query along with SELECT
- Identifies the table in which the columns you are selecting are located

### SELECT
- Always required in a query, along with FROM
- Indicates the names of the column you want to view
- If you want to see every column then use SELECT *

### WHERE
- Filter query data using a WHERE clause
```
SELECT *
    FROM table_name
    WHERE  table_column = 100
```
- This will only return results where the table_column has a value of 100
- Can be used with any comparison operator

# Formatting
- SQL treats one space, multiple spaces or line breaks as being the same

# Best practices
- always capitalize key words
- table names should not contain spaces so they do not need to be in double quotes
