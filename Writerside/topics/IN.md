# IN

Der `IN`-Operator ist ein Shorthand für mehrere `OR`-Konditionen.

## IN - Syntax

````SQL
SELECT column_name(s)
FROM table_name
WHERE column_name IN (value1, value2, ...); 
````

Dazu gibt es noch eine zweite Syntax:

````SQL
SELECT column_name(s)
FROM table_name
WHERE column_name IN (SELECT STATEMENT); 
````

## IN - Beispiele

Alle Kunden, die nicht von Deutschland, Frankreich oder England sind:

````SQL
SELECT * FROM Customer
WHERE Country NOT IN ('Germany', 'France', 'UK');
````

Alle Kunden, die vom selben Land sind wie der Lieferant:

````SQL
SELECT * FROM Customers
WHERE Country IN (SELECT Country FROM Suppliers);
````

