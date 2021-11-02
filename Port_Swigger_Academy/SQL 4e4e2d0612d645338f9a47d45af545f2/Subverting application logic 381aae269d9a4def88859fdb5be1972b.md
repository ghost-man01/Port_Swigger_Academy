# Subverting application logic

## Subverting application logic

If an application uses login credentials :

username: webniare password: bluecheese

The application check the credential by this **SQL query**

> SELECT * FROM users WHERE username = ‘webniare’ AND password = ‘bluecheese’
> 
- * If the query returns the details of user the login is successful.**

Attacker can login as any user without a password simply by using the **SQL COMMENT SEQUENCE** to remove the password check from the WHERE clause of the query.

The attacker use the **administrator’–** as the username

## SQL query

SELECT * FROM users WHERE username = administartor'- -&password = 123456 

**successfully logged attacker as a user.**