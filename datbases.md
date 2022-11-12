# Databases

## Inbox

- referential integrity
- ddl, dml

--

## Log

--

## Notes

### Normalization

- a database design technique that reduces data redundancy and eliminates insertion, update and deletion anomalies
- divides larger tables into smaller tables and links them using relationships
- SQL has normal forms 1-6
- 1st normal form rules
  - each table 'cell' should only contain one value
  - each record needs to be unique
- 2nd normal form rules
  - must be already in 1st normal form
  - each record requires a single column primary key that is not dependent on a relationship between the key and data
  - using a foreign key will ensure that the primary must exist in the parent table
- 3rd normal form rules
  - must already be in end normal form
  - has not transitive functional dependencies (see definition below)

### Key

- a value used to identify records (tuples, rows) in a table uniquely
- usually a single column, can be a combination of columns
- identifies data and helps establish relationships with multiple tables

### Foreign Key

- a key that references the primary key of another table
- can have a different name than the primary key
- do not have to be unique and most often aren't
- can be null

### Primary Key

- cannot be null
- must be unique
- should rarely be changed
- must be assigned when a record is created

### Transitive functional dependency

- when changing a non key column may cause any of the other non key columns to change

### DBMS

- database management system
- software to create and manage databases
- comprised of a storage system, metadata catalog, database access language, optimization engine, query processor, log manager and other data utilities

--

## End
