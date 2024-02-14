# UPDATE

<show-structure depth="2" />

Mit dem `UPDATE`-Statement kann man existierende Datensätze modifizieren.

## UPDATE - Syntax

Die Syntax von `UPDATE` sieht folgendermassen aus:

````SQL
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
````

> **Wichtig**: Die `WHERE`-Klausel muss unbedingt geschrieben werden, ansonsten werden alle Datensätze gelöscht

{ style="warning" }

## UPDATE - Beispiel

````SQL
UPDATE Customer
SET ContactName = 'Alfred Schmidt', City = 'Frankfurt'
WHERE CustomerId = 1;
````

Im Beispiel wird der Datensatz mit der `CustomerId` 1, modifiziert. Dabei wird der `ContactName` und `City` verändert.