# cheatsheats_SQL
```
DISTINCT- убирает лишние повторяющиеся строки и формирут
SELECT - выбор колонки 
FROM- выбор строчки из колонки 
COUNT- выводит общие количество строк совмещается с DISTINCT
```
### Посчитать среднее значение

```
SELECT AVG (ship_via)
FROM orders WHERE ship_country = 'USA'
```


### Выбрать нужное по слову( пример сотрудника, товар, ..)
```
SELECT last_name, first_name 
FROM employees
WHERE first_name LIKE '%n'
```

### Сделать выборку (можно выбирать число строк которое хотим видеть)
```
SELECT product_name, unit_price
FROM products
LIMIT 10
```

### Найти все записи где = NULL ( IS NOT NULL)
```
SELECT ship_city, ship_region, ship_country
FROM orders
WHERE ship_region IS NULL
```
### Сортировка по кол-ву
```
SELECT ship_country, COUNT(*)
FROM orders
WHERE freight >50
GROUP BY ship_country
ORDER BY  COUNT(*) DESC
```
