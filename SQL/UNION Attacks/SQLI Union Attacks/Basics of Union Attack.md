# Basic

When an application vulnerable to SQL injection and the result of the query return within the application's response.
- *UNION* used to retrieved data from other tables within the database.
- UNION let's you execute one or more addition SELECT queries and append the results to the original query.

> SELECT a, b FROM table1 UNION SELECT c, d FROM table2 

*For UNION query to work :*

* The individual queries must return same number of columns.
* The data types in each column must be compatible between two individual queries.

*For SQL injection UNION attack the requirements are :*

* How many columns are being returned from the original query*
* Which columns returned from the original query are of a suitable data type to hold the results from the injected query?
 
