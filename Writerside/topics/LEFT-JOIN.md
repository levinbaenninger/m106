# LEFT JOIN

Das `LEFT JOIN`-Keyword gibt alle Datensätze aus der linken Tabelle, und die übereinstimmenden Datensätze von der rechten Tabelle, zurück. 

## LEFT JOIN - Syntax

````SQL
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
````

## LEFT JOIN - Beispiel

````SQL
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID
ORDER BY Customers.CustomerName;
````

> Das `LEFT JOIN`-Keyword gibt alle Datensätze aus der Tabelle `Customers` zurück, auch dann wenn es keine Übereinstimmung mit der Tabelle `ORDERS` gibt.