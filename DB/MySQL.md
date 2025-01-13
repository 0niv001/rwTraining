---
sticker: lucide//database
---
[[Relational database]]
## Create
```MySQL
CREATE DATABASE dbName;

CREATE TABLE tName (
	column1 INT DEFAULT val, # add data type
	column2 VARCHAR (50) UNIQUE,
	column3 DECIMAL (5,2) # Max digits and precision
	column4 DATE NOT NULL; # contraint enuring value cannot be empty
	column5 TIME
	column6 DATETIME
);

INSERT INTO tname VALUES (First_row),(second_row); # Insert row in table 
```
## Selection
```MySQL
SELECT * FROM tName; # Select everything from table

SELECT col1, col2 FROM tName; # Select columns from table

WHERE col1 = conditions ; # Filter results based on condtion

WHERE col1 IS NULL;

WHERE col1 IS NOT NULL;
```
## Read
```MySQL
USE dbName;
```
## Update
```MySQL
RENAME TABLE tName TO newName;
	   COLUMN col_name TO new_col;

ALTER TABLE tName ADD new_col VARCHAR (50); # adds new column
				  MODIFY COLUMN new_col VARCHAR (100); 
				  AFTER new_col; # Move column after specified one

UPDATE tName SET col1 = {condtition} WHERE {Condtion}
# Omit WHERE clause to update all of the columns at once 
```
## Delete
```MySQL
DROP DATABASE database_name;

DROP TABLE tName;

DROP COLUMN col_name;

DELETE FROM tName WHERE col_name = {Condtion};
```
## Permission
```MySQL
ALTER DATABASE {name} READ ONLY = 1; #Can access data, but no modifications

ALTER DATABASE {name} ENCRYPTION = "Y"; #Add encryption
```
## Auto commit and rollback 
- Set to ON automatically
```MySQL
SET AUTOCOMMIT = OFF; # Transactions will no longer save automatically
COMMIT; # Saves current db state 
ROLLBACK; # Restore transactions to previous commit
```
## Functions
```MySQL
CURRENT_DATE(); # Returns current date, can + or - for different days
CURRENT_TIME(); # Returns current time
NOW(); # Returns current date time - Good for transactions 
```
## Constraints
- Primary keys are unique and cannot be null, should have one on each table. 

```MySQL
col1 INT UNIQUE # When creating table

ALTER TABLE tName ADD CONSTRAINT UNIQUE (col2); # Adding to existing table

CONSTRAINT constraint_name CHECK (conditions > 1); # give check a name
```
## Auto Increment
- Automatically increment keys - Primary keys. 
```MySQL

```