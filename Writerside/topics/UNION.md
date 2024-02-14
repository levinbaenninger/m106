# UNION

Mit dem `UNION`-Operator können wir mehrere Resultate von `SELECT`-Statements kombinieren. Dabei gibt es einige Voraussetzungen:

- Jedes `SELECT`-Statement in der `UNION` muss die gleiche Anzahl Attribute haben
- Zudem müssen die Attribute ähnliche Datentypen haben
- Darüber hinaus müssen die Attribute in jedem `SELECT`-Statement in derselben Reihenfolge sein.

## UNION - Syntax

````SQL
SELECT column_name(s) FROM table1
UNION
SELECT column_name(s) FROM table2; 
````

### UNION ALL - Syntax

Standardmässige wählt der `UNION`-Operator nur einzigartige Werte aus. Um Duplikate zu erlauben, können wir `UNION ALL` nutzen:

````SQL
SELECT column_name(s) FROM table1
UNION ALL
SELECT column_name(s) FROM table2; 
````

## UNION - Beispiele

### UNION

````SQL
SELECT City FROM Customer
UNION
SELECT City FROM Supplier
ORDER BY City;
````

Gibt die Städte zurück, die in der Tabelle `Customer` und in der Tabelle `Supplier` sind (ohne Duplikate).

### UNION ALL

````SQL
SELECT City FROM Customers
UNION ALL
SELECT City FROM Suppliers
ORDER BY City;
````

Gibt die Städte zurück, die in der Tabelle `Customer` und in der Tabelle `Supplier` sind (mit Duplikaten).