# SQL

## Inbox

- order of operations

---

## Log

20220926 - mode tutorial SQL Like statement  
20220927 - finished mode basic sql tutorial  
20220928 - intermediate tutorial - finished AVG  
20220930 - intermediate tutorial - finished  GROUP BY  
20221004 - intermediate tutorial - working on CASE inside an aggregate function (pivot)

---

## Notes

### Resources - Websites

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

### Resources - Courses

- Stanford DB Course [https://www.edx.org/course/databases-5-sql](https://www.edx.org/course/databases-5-sql)  

### What is SQL?

- Structured Query Language
- Designed for managing data in a relational database

### Precision

- the number of digits in a number
- in SQL Server the maximum precision of decimal and numeric types is 38

### Scale

- the number of digits to the right of the decimal point

### Aggregate Functions

- performs operations across entire columns
- COUNT
- SUM
- MIN
- MAX
- AVG
- calculated before limits, if a 100 row limit is set, the aggregated numbers will contain all rows, even if only 100 are displayed

### AND

- logical operator
- allows you to select multiple rows that satisfy certain conditions

### AS (alias)

- used to rename a column or table with an alias
- only exists in the query, does not change the table
- if the alias name contains a space it needs to be in double quotes

```SQL
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

### AVG

- calculates average of a selected group
- can only be used on numerical columns
- ! it ignores nulls completely, if you want nulls to be zero this will need to be handled in the statement

### Between

- logical operator that allows you to select rows between a specific range
- it must be paired with the AND operator
- it is inclusive and will include the bounds of the range

### Case

- SQL way of using if/then logic
- a CASE statement needs to be followed by a pair of WHEN THEN statements and finish with END
- it can use an optional else statement

```SQL
SELECT year, name 
    CASE WHEN year = 2022 THEN '22'
         ELSE NULL END as year_ab
    from table
```

- the case statement above will check each row the year 2022 
- a column named year_ab is created
- anytime the case statement is true the column get a 22 if not it gets a null
- it is possible to chain multiple CASE WHEN statements together
- it is also possible to have an AND statement inside a CASE
- Case with aggregate functions
  - useful functionality
  - can use to count rows that meant a condition
  - can be tricky
  - write out the case statement first then add aggregation and group by

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

### COUNT

- counts the number of non-null rows in a particular column

### GROUP BY

- used to aggregate only parts of a table
- will group aggregations by selected column(s)

```SQL
SELECt * from table_name
  GROUP BY year, month
```

- the order of the column names does not matter
- can be combined with an order by to change how the output is displayed

### HAVING

- used to filter aggregated columns when you can't filter with a WHERE

### Logical Operators

`LIKE` match similar values instead of exact ones  
`IN` specify if a value is in a list of values  
`BETWEEN` select rows in a certain range  
`IS NULL` select rows with no value in a certain column  
`AND` chain multiple conditions  
`OR` select rows that satisfy one condition or another  
`NOT` select rows that do not match a condition

### LIKE

- logical operator
- allows matching on similar values not exact ones
- is case sensitive
- can use wildcards % to reference any character or set of characters, _ is for one character
- ILIKE can be used to ignore case

### LIMIT

- limits how many rows the query returns

```SQL
SELECT *
    FROM table_name
    LIMIT 100
```

### MIN / MAX

- return the highest or lowest value in a column
- can be used on non numerical data
- return the lowest number, earliest date, alphabetical closest to A

### IN

- logical operator
- specify a list of values to include in the results

### IS NULL

- logical operator
- allows you to exclude rows with null values from your results
- column = NULL does not work

### NOT

- logical operator
- can be placed before any conditional statement to select rows in which the statement is false
- can be used to identify non null rows with is `IS NOT NULL`

### FROM

- Always required in a query along with SELECT
- Identifies the table in which the columns you are selecting are located

### OR

- Logical operator
- allows you to select rows that satisfy either or two conditions
- can be combined with AND using parenthesis

```SQL
SELECT * 
    FROM table
  WHERE col_1 = 1
    AND (col_2 = 2 OR col_3 = 3)
```

### ORDER BY

- sorts data based on one or more columns
- defaults to ascending order, can use DESC to sort in descending order

```SQL
SELECT *
    FROM table
  WHERE col_1 = 1
  ORDER BY col_1 DESC
```

- can be used to order by multiple columns
  - columns should be separated by commas
  - a DESC operator will only apply to the column that precedes it
  - sorted in the order in which the columns appear
- ORDER BY is executed before a LIMIT

### SELECT

- Always required in a query, along with FROM
- Indicates the names of the column you want to view
- If you want to see every column then use SELECT *

### SUM

- sum values of a numerical column

### WHERE

- Filter query data using a WHERE clause

```SQL
SELECT *
    FROM table_name
    WHERE  table_column = 100
```

- This will only return results where the table_column has a value of 100
- Can be used with any comparison operator

### Formatting

- SQL treats one space, multiple spaces or line breaks as being the same

### Best practices

- always capitalize key words
- table names should not contain spaces so they do not need to be in double quotes

### Misc.

- double quotes refers to a column name "group", (GROUP is also a function)
- only use double quotes when naming an alias with spaces if necessary, ideally should use underscores
- single quotes - identify a string

### Comments

- a single line comment is preceded by --
- multi line comments are enclosed with `/* */`

---

## END

_---
