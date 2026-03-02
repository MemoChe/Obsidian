-Table_name: The name of the table where the data will be updated.
-column1, column2, ...: The columns to be updated.
-value1, value2, ...: The new values to set.
-Condition: Specifies which rows should be updated. It’s crucial to use a WHERE clause to avoid updating all rows in the table.
```mysql
UPDATE `table_name`
SET `column1` = `value1`, `column2` = `value2`, ...
WHERE `condition`;

UPDATE `products`
SET `price` = 29.99
WHERE `productID` = 1;

UPDATE products SET price = price * 1.1;

UPDATE `products`
SET `name` = 'New Product Name', `quantity` = 50
WHERE `productID` = 2;
```
