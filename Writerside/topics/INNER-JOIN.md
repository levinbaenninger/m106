# INNER JOIN

Das `INNER JOIN`-Keyword wählt alle Datensätze aus, Werte in beiden Tabellen vorkommen.

## INNER JOIN - Syntax

````SQL
SELECT column_name(s)
FROM table1
INNER JOIN table2 ON table1.column_name = table2.column_name;
````

## INNER JOIN - Beispiel

Dieser Query wählt alle Bestellungen aus mit Informationen zum Kunden:

````SQL
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
````

> Das `INNER JOIN`-Keyword wählt alle Datensätze von beiden Tabellen aus, solange Werte in beiden Tabellen vorkommen.
> 
> Beispiel: Wenn es Datensätze in Bestellungen gibt, welche keine Übereinstimmung mit der Tabelle `Customers` haben, dann werden diese Bestellungen nicht angezeigt.

### Mehrere Tabellen

Man kann mit Joins auch mehr als zwei Tabellen miteinander verbinden, bspw. so:

````SQL
SELECT Orders.OrderID, Customers.CustomerName, Shippers.ShipperName
FROM ((Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID)
INNER JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID);
````

