# GROUP BY

Das `GROUP BY`-Statement gruppiert Datensätze mit den gleichen Werten.

Es wird oft zusammen mit Aggregatsfunktionen genutzt, um das Resultat zu gruppieren.

## GROUP BY - Syntax

````SQL
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
ORDER BY column_name(s);
````

## GROUP BY - Beispiel

````SQL
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
ORDER BY COUNT(CustomerID) DESC;
````