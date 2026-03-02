Rollups are like making automatic summaries of your data at different levels. Imagine you have a large list of sales and you want to see the totals in different ways without having to make many separate queries.
```mysql
CREATE TABLE ventas ( 
	id INT PRIMARY KEY, 
	region VARCHAR(50), pais VARCHAR(50), 
	ciudad VARCHAR(50), 
	monto DECIMAL(10, 2) ); 
	
INSERT INTO ventas VALUES 
	('Norte', 'Laptop', 2023, 1, 100), 
	('Norte', 'Teléfono', 2023, 1, 150), 
	('Sur', 'Laptop', 2023, 1, 80), 
	('Sur', 'Teléfono', 2023, 1, 120), 
	('Norte', 'Laptop', 2023, 2, 110), 
	('Norte', 'Teléfono', 2023, 2, 140), 
	('Sur', 'Laptop', 2023, 2, 90), 
	('Sur', 'Teléfono', 2023, 2, 130);
	
SELECT region, producto, SUM(cantidad) as total_ventas FROM ventas GROUP BY region, producto WITH ROLLUP;

+---------+----------+--------------+
| region  | producto | total_ventas |
+---------+----------+--------------+
| Norte   | Laptop   |          210 |
| Norte   | Teléfono |          290 |
| Norte   | NULL     |          500 |
| Sur     | Laptop   |          170 |
| Sur     | Teléfono |          250 |
| Sur     | NULL     |          420 |
| NULL    | NULL     |          920 |
+---------+----------+--------------+


SELECT 
	IFNULL(region, 'NULL') AS region,
	IFNULL(producto, 'NULL') AS producto,
	IFNULL(CAST(año AS CHAR), 'NULL') AS año,             SUM(cantidad) AS total_ventas 
FROM ventas GROUP BY region, producto, año
WITH ROLLUP 
ORDER BY IFNULL(region, 'zzz'), 
         IFNULL(producto, 'zzz'), 
         IFNULL(CAST(año AS CHAR), 'zzz');

+---------+----------+------+--------------+
| region  | producto | año  | total_ventas |
+---------+----------+------+--------------+
| Norte   | Laptop   | 2023 |          210 |
| Norte   | Laptop   | NULL |          210 |
| Norte   | Teléfono | 2023 |          290 |
| Norte   | Teléfono | NULL |          290 |
| Norte   | NULL     | NULL |          500 |
| Sur     | Laptop   | 2023 |          170 |
| Sur     | Laptop   | NULL |          170 |
| Sur     | Teléfono | 2023 |          250 |
| Sur     | Teléfono | NULL |          250 |
| Sur     | NULL     | NULL |          420 |
| NULL    | NULL     | NULL |          920 |
+---------+----------+------+--------------+
```
As you can see the subtotals start with the last subtotal until you reach the main subtotal