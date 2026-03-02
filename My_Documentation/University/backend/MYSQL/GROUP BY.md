Group by is a very useful function that allow us to calculate some required data on repeating parameters.
```mysql
CREATE TABLE clients ( 
	id INT PRIMARY KEY, 
	name VARCHAR(50), 
	city VARCHAR(50), 
	age INT 
); 
INSERT INTO clients (id, name, city, ag) 
VALUES (1, 'Juan', 'Lima', 25), 
	   (2, 'María', 'Lima', 30), 
	   (3, 'Pedro', 'Arequipa', 28), 
	   (4, 'Ana', 'Trujillo', 26), 
	   (5, 'Luis', 'Lima', 32);
```

```mysql
SELECT ciudad, COUNT(*) AS cantidad_clientes
FROM clientes
GROUP BY ciudad;
+-----------+------------------+
| ciudad    | cantidad_clientes|
+-----------+------------------+
| Lima      | 3                |
| Arequipa  | 1                |
| Trujillo  | 1                |
+-----------+------------------+
```

```mysql
CREATE TABLE ventas (
	id INT PRIMARY KEY, 
	region VARCHAR(50), 
	country VARCHAR(50), 
	city VARCHAR(50), 
	mount DECIMAL(10, 2) 
); 
INSERT INTO ventas (id, region, country, city, mount) VALUES (1, 'Asia', 'Japón', 'Tokio', 5000.00), 
	   (2, 'Asia', 'Japón', 'Osaka', 3000.00), 
	   (3, 'Asia', 'China', 'Beijing', 4000.00), 
	   (4, 'Asia', 'China', 'Shanghai', 6000.00), 
	   (5, 'Europa', 'Francia', 'París', 7000.00),           (6, 'Europa', 'Francia', 'Lyon', 3000.00), 
	   (7, 'Europa', 'Italia', 'Roma', 4000.00), 
	   (8, 'Europa', 'Italia', 'Milán', 2000.00);
	   
SELECT region, pais, ciudad, SUM(monto) AS total_venta
FROM ventas
GROUP BY region, pais, ciudad;
```
We realize that all the Tokios were added if there are any repeats, it is useful for calculating sales in certain databases.
```
+---------+----------+-----------+-------------+
| region  | pais     | ciudad    | total_venta |
+---------+----------+-----------+-------------+
| Asia    | Japón    | Tokio     | 5000.00     |
| Asia    | Japón    | Osaka     | 3000.00     |
| Asia    | China    | Beijing   | 4000.00     |
| Asia    | China    | Shanghai  | 6000.00     |
| Europa  | Francia  | París     | 7000.00     |
| Europa  | Francia  | Lyon      | 3000.00     |
| Europa  | Italia   | Roma      | 4000.00     |
| Europa  | Italia   | Milán     | 2000.00     |
+---------+----------+-----------+-------------+
```