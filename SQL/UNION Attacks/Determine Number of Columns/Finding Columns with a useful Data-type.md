# Reason
* Reason for performing the SQL UNIOIN attack is to retrieve data from injected query.
* Generally the data that we want to retrieve is string form.
* So you need to find out one or more column in the original query result, whose data-type is or compatible with, string data.

### Work

* If you already determined the columns, then **you can probe each column** to test whether it can hold a *string* data
* by submitting a *UNION SELECT* payload that **place a string value into each column in turn.**


#### Example

We determined that application has four columns, then we construct an attack like:

>' UNION SELECT NULL,NULL,NULL,NULL--     **It determined the column**
>' UNION SELECT 'a' ,NULL,NULL,NULL--
>' UNION SELECT NULL, 'a' ,NULL,NULL--
>'UNION SELECT NULL,NULL, 'a' ,NULL--
>' UNION SELECT NULL,NULL,NULL, 'a'--
>

* We use the near comma just before or after NULL never before or after *string* 'a'
* There is a **space** between *NULL and string*


#### Database Error

If the data-type of column is not compatible with string then there is an error occurs from database.

If 'a' is **int data-type then conversion is failed.**

But if an error doesn't occur, the application's response contains some **additional content including injected string value**, then relevant column is suitable for retrieving data.

