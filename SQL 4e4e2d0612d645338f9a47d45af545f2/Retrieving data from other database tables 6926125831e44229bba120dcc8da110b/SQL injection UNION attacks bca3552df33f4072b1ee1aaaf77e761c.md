# SQL injection UNION attacks

When an application is vulnerable to SQL injection and the results of the query are returned with the applications response, the **UNION** keyword can be used to retrieve data from other tables within the database. The results in an SQL injection UNION attack.

- The **UNION keyword is used let's you execute one or more additional SELECT queries and append the results of the original query.**
- SELECT a, b FROM table1 UNION SELECT c, d FROM table2

> This SQL query will return a single result set with two columns, containing values from columns a and b in table1 and columns c and d in column2
> 

For a UNION query to work, two key requirements must be met:

- The individual queries must return same numbers of columns.
- The data types in each column must be  compatible between the individual queries.

To carry out an SQL injection UNION attacks you need to ensure that your attack meets these two requirements. This generally involves figuring out ?

- How many columns returned from the original query ?
- Which columns returned from the original query are of a suitable datatypes to hold the results from the injected query ?

## Determining the number of columns required in an SQL injection UNION attack

When performing an SQL injection UNION attacks there are two effective methods to determine how many columns are being returned from the original query. 

 

### Method 1 →

Injecting a series of **ORDER BY** clauses and incrementing the specified column index until an error occurs.

For example assuming the injection point is quoted string within **WHERE**  clause of the original query, you would submit :

' ORDER BY 1 - -

' ORDER BY 2 - -

' ORDER BY 3 - -

etc.