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
WHERE vend_id != `DLL01` ;
```

To filter to products with a price between 5 and 10:

```
SELECT prod_name, prod_price
FROM Products
WHERE prod_price BETWEEN 5 and 10;
```
