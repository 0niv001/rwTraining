**Core Components**
Data Definition Language (DDL)
```SQL
CREATE
		INDEX (INDEX) ON (TABLE) 
ALTER
DROP
TRUNCATE - Clears data inside table
COMMENT
EXEC sp_rename
CREATE VIEW
```

Data Manipulation Language (DML)
```SQL
SELECT {cols } FROM {tables} WHERE {condition}
INSERT INTO 
UPDATE {Tables} SET {Col = new_value} WHERE {condition};
DELETE FROM {Tables} WHERE {condition};
```

Data Query Language (DQL) - Specifically for data. 
```SQL
SELECT {Col} FROM {TABL} ORDER BY {SELECTION} ASC / DESC

SELECT DISTINCT - gets rid of duplicates 

LIKE 'K_y%'; way of filtering results further

SUBQUERIES

JOIN
```

Data Control Language (DCL) - Manage access, for DBAs
```SQL
GRANT {Privilege} ON {object} TO {user}

REVOKE

PRIVILEGES 

OBJECT LEVEL - DATABASE / TABLE / COLUMN

USERS & ROLES 
```

!!!USE DEMO DATA WHEN DELETING OR UPDATING!!!

Binary strings used for images, vids and other kinds of files 

Data types
- XML
- Geometry and geography
- Cursor
- User defined tables
- sql_variant 
- Money
- Small money 

Foreign key references (table(column)) - Always make the table foreign key references first.

Table constraint - Uses more than one rule inside the table. 

## Views
```sql
create view 
```

**Inner / Left / Right join**
Join two tables together
Match columns based on the primary and foreign keys

**Full Outer**
- Keep records from all tables

## Subqueries
- Scalar - Returns a single value used in the expression. 
```SQL
SELECT productname, price, (SELECT AVG(price) FROM products) AS 'Average Price' FROM products
```

- Column - Fields
```SQL
SELECT customername,

(SELECT COUNT(*)

FROM orders

WHERE orders.customerid = customers.customerid)

AS 'order count'

FROM customers
```

Row - Records
```sql
SELECT customername

FROM customers

WHERE

(SELECT COUNT(*)

FROM orders

WHERE orders.customerid = customers.customerid)

>= 2;
```

Table - scalable, returns a table. 
```sql
SELECT * FROM

(SELECT customername, country FROM customers)

AS customerdetails

WHERE customerdetails.country = 'UK'
```

Having
```sql
SELECT CustomerID,

COUNT(Orderid) AS OrderCount

FROM orders

GROUP BY CustomerID

HAVING COUNT(OrderID) > (SELECT AVG(Ordercount)

FROM (

SELECT customerid,

count(orderid) as OrderCount

FROM orders

GROUP BY customerid)

as CustomerOrderCounts

)
```

Design DB that has movies listed in it. 
What tables can be built around it. 
Genre, actors, directors, writers, description, 
10 movies. 