# Oracle

* Every *SELECT* query must use the *FROM* keyword and specify a valid table.
* On oracle *Dual*  is a specified table, which can be used for this purpose.

 #### Query on Oracle
 
 >' UNION SELECT NULL FROM DUAL--

* The payload use the double-dash sequence to comment out the remainder original query following the injection point.

# MYSQL

* On MySQL, double-dash sequence is followed by a space.
* Alternatively the hash character # can be used to identify a comment.

[SQL injection Cheat sheet](https://portswigger.net/web-security/sql-injection/cheat-sheet)
