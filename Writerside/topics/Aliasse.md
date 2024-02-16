# Aliasse

Mit Aliassen können wir Tabellen oder Attributen einen temporären Namen zu geben. Oft werden sie genutzt, um Attributnamen leserlicher zu machen.

Sie existieren nur während der Zeit des Queries, danach werden sie wieder gelöscht.

## Aliasse - Syntax

### Attribute - Syntax

````SQL
SELECT column_name AS alias_name
FROM table_name;
````

### Tabellen - Syntax

````SQL
SELECT column_name(s)
FROM table_name AS alias_name;
````

## Aliasse - Beispiele

### Attribute - Beispiele

Beim folgenden Beispiel setzen wir zwei Aliasse:

````SQL
SELECT CustomerName AS Customer, ContactName AS "Contact Person"
FROM Customer;
````

Beim folgenden Beispiel werden vier Attribute zusammengenommen und unter einem Namen gespeichert:

````SQL
SELECT CustomerName, CONCAT_WS(', ', Address, PostalCode, City, Country) AS Address
FROM Customers;
````

### Tabellen - Beispiel


````SQL
SELECT o.OrderID, o.OrderDate, c.CustomerName
FROM Customers AS c, Orders AS o
WHERE c.CustomerName='Around the Horn' AND c.CustomerID=o.CustomerID;
````