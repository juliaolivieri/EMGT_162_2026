# Lecture 3 SQL commands

These commands work with the TYSQL.sqlite database (found on Canvas or here: https://github.com/juliaolivieri/EMGT_162_2026/blob/461f7e214763c2678073d107d72eca0bdb302879/TYSQL.sqlite) 

## SELECT

The `SELECT` keyword retrieves information from one or more relations.

To return the full contents of the `Products` relation:

```
SELECT *
FROM Products;
```

To return just the `prod_name` column of the `Product` relation:

```
SELECT prod_name
FROM Products;
```

To return the `prod_id`, `prod_name`, and `prod_price` columns of the `Product` relation:

```
SELECT prod_id, prod_name, prod_price
FROM Products;
```

To return only distinct combinations of attributes, include `DISTINCT`  after `SELECT`:

```
SELECT DISTINCT prod_price
FROM Products;
```

### Questions

1. Find all the information about each customer.
2. Find the name and address of each customer.
3. List the distinct countries where vendors come from.
4. List every unique combination of vendor and price.


## ORDER BY

The `ORDER BY` keyword allows us to sort by one or more attributes.

To order customers by name in alphabetical order:

```
SELECT cust_name
FROM Customers
ORDER BY cust_name;
```

To order customers by zip code in descending order:

```
SELECT *
FROM Customers
ORDER BY cust_zip DESC;
```

### Questions
1. Find an alphabetically sorted list of products
1. Sort just the product names by price
1. Sort all product information by vendor id, then product price
1. Sort all product information by product price in descending order
1. Sort all product information by vend id in ascending order, then product price in descending order

## LIMIT / OFFSET

The `LIMIT`  keyword allows us to only output the first $x$ rows of the resulting relation.

To output the first three products:

```
SELECT *
FROM Products
LIMIT 3;
```

We can combine the `LIMIT` keyword with the `OFFSET`  keyword to skip the first $y$ rows:

```
SELECT *
FROM Products
LIMIT 3 OFFSET 2;
```

### Questions
1. Find the five most expensive products
2. Find the next five most expensive products
3. Sort by product description and find the third, fourth, and fifth product from this sorted order



## WHERE

The `WHERE` keyword filters data based on specified criteria. The `WHERE`  clause should directly follow the `FROM`  clause.

To filter to only products with a price of 3.49:

```
SELECT prod_name, prod_price
FROM Products
WHERE prod_price = 3.49;
```

To filter to products with price less than or equal to 10:

```
SELECT prod_name, prod_price
FROM Products
WHERE prod_price <= 10;
```

To filter to products with a specific vendor id:

```
SELECT vend_id, prod_name
FROM Products
WHERE vend_id != 'DLL01' ;
```

To filter to products with a price between 5 and 10:

```
SELECT prod_name, prod_price
FROM Products
WHERE prod_price BETWEEN 5 and 10;
```

### Questions

1. Find all products with a price of 3.49
1. Find all products with a price less than 10, sorted by price
1. Find all products not made by vendor DLL01:
1. Find all products with prices between 3.49 and 8.99 (inclusive)
1. Find all customers without an email address in the database
1. Find products where the vendor id is DLL01 and the price is less than or equal to 4
1. Find products where the vendor id is DLL01 or BRS01
1. Find products where the vendor id is DLL01 or BRS01, and the price is greater than or equal to 10
1. Find products where the vendor id is DLL01, or the vendor id is BRS01 and the price is greater than or equal to 10

### Advanced questions

1. Find all products that start with the word "Fish"
1. Find all products that include the phrase "bean bag"
1. Find all products that begin with F and end with y
1. Find all products with names that end with "inch teddy bear"
1. Find all products with names that match "__ inch teddy bear" (where underscore can be any character)

