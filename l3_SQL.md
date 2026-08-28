# Lecture 3 SQL commands

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

