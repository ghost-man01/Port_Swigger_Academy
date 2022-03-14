# Knew before
If you know how to determine number of columns and found which column can hold *string data* from original query. You are now able to retrieve interesting data.

Suppose that :

 * The original query returns two columns, both of which can hold string data.
 * The injection point is quoted string within the *WHERE* clause.
 * The database contains the table called *users* with the columns called *username* and *password*

**Attack**

>' UNION SELECT username, password FROM users--

* Retrieve the contents of users table by submitting the input.

* Crucial information is required like *users* table columns *username, password*.
* In fact, all modern databases provide ways of examining the database structure, to determine what tables and columns it contains.

