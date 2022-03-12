Subverting means Cracking or Destroying

If an application has login functionality

**username, password** are two parameters.

> SELECT * from users WHERE username='ghost' AND  password='hello'


Attacker construct an attack not to enter password and login : 

> SELECT  * FROM users WHERE username='administrator'--' AND password='1234'

- [ ]  After username password got commented by double dash sequence.
- By using this Subverting logic attacker can logged in as without password.

