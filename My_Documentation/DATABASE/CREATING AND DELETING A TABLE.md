```mysql
mysql> CREATE DATABASE Southwind;

mysql> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| southwind          |
| ......             |

mysql> USE southwind;
Database changed

mysql> DROP TABLE IF EXISTES Southwind;

mysql> CREATE TABLE IF NOT EXISTS products (
productID INT UNSIGNED NOT NULL AUTO_INCREMENT,
productCode CHAR(3) NOT NULL DEFAULT '',
name VARCHAR(30) NOT NULL DEFAULT '',
quantity INT UNSIGNED NOT NULL DEFAULT 0,
price DECIMAL(7,2) NOT NULL DEFAULT 99999.99,
PRIMARY KEY (productID)
);
mysql> SHOW TABLES;
+---------------------+
| Tables_in_southwind |
+---------------------+
| products            |
+---------------------+

![[Pasted image 20240731183557.png]]

![[Pasted image 20240731183719.png]]
```

To delete columns use the word drop followed by the column name
```mysql
DROP DATABASE IF EXISTS southwind;
DROP TABLE IF EXISTS products;
```
To delete all the data in a table but keep the structure, use the DELETE command.
```mysql
DELETE FROM products /*Deletes all rows in a table*/
DELETE FROM products WHERE productId = 1001;
```

