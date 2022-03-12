SQL query returned response within application's response.  An attacker can take benefit  an SQL injection vulnerability to retrieve data from Other tables.

- Which can be done by using **UNION** keyword, which let's you execute an additional query and append the result to the original query.

##### Shopping website category is game with their description

>SELECT name, description FROM products WHERE category = 'games'

###### An attacker can submit

>' UNION SELECT username, password FROM users--

- This query will cause to return all the username and password along with the name and description of products.

 