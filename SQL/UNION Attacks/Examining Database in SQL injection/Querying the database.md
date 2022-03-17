# Why ?

- It's necessary to often get some information about the database.
-  This includes the version and type of database.
- The contents of the database in which terms of which tables and columns it contains.

## Querying the database and it's version
- Different type of database provide different types of ways querying their database.
- We have to find out one that works, allowing you to determine both type and version of the database software.

||
--|--
**Database** | **Query**
MySQL, Microsoft | SELECT @@version
Oracle | SELECT * FROM v$version
PostgreSQL | SELECT version()

### Example

>' UNION SELECT @@version--

This return the output confirming that database is Microsoft SQL Server and it's version.


# Listing the contents of database

Most database types ( with the notable exception of oracle ) have a set of views called **information schema** which provide information about the database.

We can query *information_schema.tables* to list tables in the database.

> SELECT * FROM information_schema.tables

This results the output like :

||
--|--|--|--
Table_Catalog | Table_Schema |  Table_Name | Table_Type
MyDatabase | dbo | Products | Base Table
MyDatabase | dbo | Users | Base Table
MyDatabase | dbo | Feedback | Base Table


There are three table *Products, Users, Feedback*

We can query the column *information_schema.columns* to list the columns in individual tables

> SELECT * FROM information_schema.columns WHERE table_name = 'Users'


This output like:

||
--|--|--|--
Table_Catalog | Table_Schema | Table_Name | Column_Name | Data_Type
MyDatabase | dbo | Users | UserId | int
MyDatabase | dbo | Users | Password | varchar
MyDatabase | dbo | Users | Username | varchar







