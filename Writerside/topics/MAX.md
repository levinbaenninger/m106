# MAX

Die `MAX()`-Funktion gibt einem den grössten Wert eines Attributs zurück.

## MAX() - Syntax

````SQL
SELECT MAX(column_name)
FROM table_name
WHERE condition;
````

## MAX() - Beispiele

````SQL
SELECT MAX(Price) AS LargestPrice
FROM Products;
````

