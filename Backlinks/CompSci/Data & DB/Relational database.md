- Most common type of DB, designed as a set of tables and relations that are linked using ID.
- Each instance is given a primary key to ID, that can be used to related to another DB.
- Normalisation reduces redundancy by breaking up data into separate tables. 
- Often use [[SQL]] for creation, manipulation and management.  
- Used for [[Structured data]]

**Transactional data processing**
- System that records transactions for events that organisation wants to track. - Small unit of work, referred to as Online Transactional Processing (OLTP).
- OLTP relies on DB systems optimised for read and write operations and to support CRUD operations (Create, Retrieve, Update, Delete).
- Normalised- High volume of small transactions.
- SQL, Postgres, MySQL, MariaDB

To ensure integrity of data OLTP enforce transactions with ACID semantics:
- *Atomicity:* Each transaction is treated as single unit that either succeeds or fails.
- *Consistency:* Transactions can only take data in DB from one valid state to another.
- *Isolation:* Concurrent transactions cannot interfere with one another.
- *Durability:* When transactions have happened, they have been done and committed.

**Analytical data processing
- Makes use of read only systems storing data and metrics, looking at historical data
- Denormalise the data.
- Data lake: Common large scale data analytical processing scenario.
- Data warehouse: Way to store data in relational schema optimised for read operations - Queries are done to support reporting and data visualisation.

*Common architecture:*
1. Data is stored in central data lake for analysis. 
2. Extract, Transform and Load (ETL) process copies data from files and OLTP DBs into data warehouse, optimised for read ops.
3. Data from warehouse is pooled and loaded into analytical processing model - Cube. Aggregated measures from pact tables are calculated for intersections of dimensions.
4. Data in data lake, warehouse, and analytical model can be queried to produce reports, visualisations and dashboards.