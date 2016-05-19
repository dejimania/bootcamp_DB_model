

## some basic SQL statement
```sql
1. INSERT INTO `customer`(`first_name`, `last_name`, `email`, `active`) VALUES('Sola', 'Dele', 'solad@gmail.com');
```
```sql
2. SELECT * FROM `customer` WHERE `last_name` = 'Dele";
```
```sql
3. DELETE FROM `customer` WHERE `customer_id` = 1;
```
```sql
4. UPDATE `country` SET `country_name`= 'Nigeria' WHERE country_id = 1;
```
```sql
5. ALTER TABLE `city` ADD `state_abr` varchar(15) NOT NULL;
```
```sql
6. SELECT * FROM `address` where `city_id` = 2 desc;
```
```sql
7. INSERT INTO customer (first_name, address, city_id)
VALUES ('Idrees',
(SELECT address1 FROM address WHERE district = 'Wuse' AND postal_code = '238006'),
(SELECT city_id FROM city WHERE city_name = 'Abuja'));
```
```sql
8. SELECT DISTINCT a.* FROM country AS a JOIN city WHERE a.id = country_name;
```
```sql
9. SELECT * FROM country WHERE country id IN (SELECT country_name FROM city);
```
```sql
10. SELECT CONCAT(last_name, ', ', first_name) AS full_name, district
FROM customer AS a JOIN address AS b ON a.customer_id = customer ORDER BY full_name, district;
```
```sql
11. SELECT last_name, first_name, phone_number
FROM customer AS a LEFT JOIN address AS b ON a.customer_id = customer
WHERE last_name LIKE 'B%'
ORDER BY last_name, first_name, phone_number;
```

