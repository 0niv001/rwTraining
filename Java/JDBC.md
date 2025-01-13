Classes and interfaces for connecting to databases and executing SQL Queries. 

JDBC has drivers for most DBs. Used in both small scale and enterprise applications. 

Download driver and add to Java project class path. 

Establish connection by specifying JDBC URL, username and password. 

SQL Queries using Statement and PreparedStatement class in JDBC. 

Statement: Basic interface, SQL Queries without parameters with no input required
PreparedStatement: More advanced, where input parameters are required. 

SQL Exceptions need to be properly handled, use SQL exceptions rather than generic ones. 

Use parameterised INSERT and DELETE statements to avoid SQL Injections.

When deleting make sure to double check with users. 

**Interfaces**
Drives: Comms with the server and executing queries. 
Connection: Session to the DB, providing methods. 
Prepared statements. 
CallableStatement: Execute SQL stored procedures, extends prepared statement. 
ResultSet: Results of a DB query. 

By printing connection, we can check that it is valid.

Use `throws SQLException` when building main method. 

Try with resources ensures connection is closed when we finish our task. preventing damage to the DB, closing all implementations as well. 

Set up string vars for connection parameters. 

**PreparedStatements**
- Read and Write DB using SQL instructions
- Using ExecuteUpdate (Insert,Delete, alter), ExecuteQuery (View info), Execute (Multiple statements) method to manipulate DB. 

**Parameters**
- Use ? in query string. 
- Parameters have a type. 
- Each ? is set by its position. 

use if to check object against a data type. 
Objects can use all data types. 

```java
if (dataChecked instanceof datatype) new Var = (datatype)dataChecked;

if (titleV instanceof String) title = (String)titleV;
if (yearV instanceof Integer) year = (Integer)yearV;
```