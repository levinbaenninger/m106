# HAVING

Die `HAVING`-Klausel wurde zu SQL hinzugefügt, da das `WHERE`-Keyword nicht mit den Aggregatsfunktionen genutzt werden kann.

## HAVING - Syntax

````SQL
SELECT column_name(s)
FROM table_name
WHERE condition
GROUP BY column_name(s)
HAVING condition
ORDER BY column_name(s);
````

## HAVING - Beispiel

Dieser Query listed die Anzahl Kunden in jedem Land auf, absteigend sortiert. Zudem inkludiert es nur Länder mit mehr als 5 Kunden:

````SQL
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5
ORDER BY COUNT(CustomerID) DESC;
````