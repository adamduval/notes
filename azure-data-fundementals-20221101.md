# Azure data fundamentals online course Nov 1, 2 2022

## Inbox

--

## Log

--

## Notes

- transactional vs analytical data stores
- transactional
  - high volume, tracks specific transactions
  - online transactional processing system (OLTP)
  - normalized
  - allows separation of tables and speeds up transactions
  - make querying difficult due to separation
- analytical
  - collection of data from various sources
  - storage of data
  - data processing
  - data visualization
- processing
- batch
  - can be grouped and processed on a schedule or triggered by a certain amount
- streaming
  - each piece of data is processed as it arrives
- data roles
  - database administrator
    - manage and maintain databases and servers
  - data engineer
    - maintaining and managing data privacy
    - ensure data performance
  - data analyst
    - design and maintain scalable business models using data
    - turn raw data into insights and action
- concepts of relational data
  - tables (relational)
    - consist of rows and columns
  - normalization
    - avoid duplication
    - #TODO missing info
  - index
    - optimizes retrieval
    - consumes additional storage space
    - indexes need to be maintained with additions, deletes and modifications on a table  
    - trade offs in performance
  - view
    - a virtual table
    - comes with predefined joins
  - non relational data
    - multiple entities in a collection
    - non tabular schema
    - defined by labeling it with the name is represents
    - example: json data
    - entities need unique key values
    - difficult to iterate through entire database
    - can use advanced non relational concepts to query (cosmos)
  - semi-structured data
    - defined by the actual fields and sub fields
  - unstructured
    - does not contain fields
    - BLOB, binary large objects
    - files, video, audio, files, etc.
  - NoSQL
    - loose term to describe non relational
    - key-value store, document based, column family db, graph db (nodes and edges)
- concepts of data analytics
  - processing
    - convert raw data into a business model
  - ETL
    - continuous pipeline of operations
    - suitable for simple models with little dependency between items
  - ELT
    - iterative approach
    - suitable for complex models using multiple database items
    - more scalable in the cloud
    - suitable for stream processing
- azure data services
  - infrastructure as a service or platform as a service to host databases
  - IaaS
    - virtual structure in the cloud that creates virtual machines to mimic on prem database
    - still requires management
  - PaaS
    - resources are specified and azure will do all creation, automation, all managed by azure
    - azure handles all scaling
  - moving away from on prem reduces costs, and lowers administration effort
- querying relation data in azure
  - DML data manipulation language
    - select, insert, update, delete
  - DDL data definition language
    - create, modify, alter database objects
  - DCL data control language
    - 

## End
