# LIKE

Mit dem `LIKE`-Operator können wir nach einem Muster suchen: RegularExpression.

## LIKE - Syntax

````SQL
SELECT column1, column2, ...
FROM table_name
WHERE column LIKE pattern; 
````

## LIKE - Beispiele

````SQL
SELECT * FROM Customers
WHERE CustomerName LIKE 'a%'; 
````

Wählt alle Datensätze aus, die mit `a` starten.

````SQL
SELECT * FROM Customers
WHERE CustomerName LIKE '_r%';
````

Wählt alle Datensätze aus, die ein `r` an zweiter Stelle haben.