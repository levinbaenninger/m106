# MIN

Die `MIN()`-Funktion gibt den kleinsten Wert eines Attributs zurück.$

## MIN() - Syntax

````SQL
SELECT MIN(column_name)
FROM table_name
WHERE condition;
````

## MIN() - Beispiel

````SQL
SELECT MIN(Price) AS SmallestPrice
FROM Products;
````

