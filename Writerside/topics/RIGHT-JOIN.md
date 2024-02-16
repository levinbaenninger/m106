# RIGHT JOIN

Das `RIGHT JOIN`-Keyword gibt alle Datensätze aus der rechten Tabelle, und die übereinstimmenden Datensätze von der linken Tabelle, zurück. 

## RIGHT JOIN - Syntax

````SQL
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;
````

## RIGHT JOIN - Beispiel

````SQL
SELECT Orders.OrderID, Employees.LastName, Employees.FirstName
FROM Orders
RIGHT JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID
ORDER BY Orders.OrderID;
````

> Das `RIGHT JOIN`-Keyword gibt alle Datensätze aus der Tabelle `Employees` zurück, auch dann, wenn es keine Übereinstimmung mit der Tabelle `ORDERS` gibt.