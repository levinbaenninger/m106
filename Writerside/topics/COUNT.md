# COUNT

Die `COUNT()`-Funktion gibt die Anzahl Datensätze zurück, die dem Kriterium entsprechen.

## COUNT() - Syntax

````SQL
SELECT COUNT(column_name)
FROM table_name
WHERE condition;
````

## COUNT() - Beispiel

````SQL
SELECT COUNT(*)
FROM Product;
````

> `NULL`-Werte werden nicht gezählt