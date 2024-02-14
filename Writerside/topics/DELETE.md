# DELETE

<show-structure depth="2" />

Mit dem `DELETE`-Statement können wir existierende Datensätze in einer Tabelle löschen.

## DELETE - Syntax

````SQL
DELETE FROM table_name 
WHERE condition;
````

> **Wichtig:** Wenn die `WHERE`-Klausel weggelassen wird, werden alle Datensätze gelöscht

{ style="warning" }

## DELETE - Beispiel

````SQL
DELETE FROM Customer
WHERE CustomerName = 'Alfreds Futterkiste';
````

In diesem Beispiel werden alle Datensätze gelöscht, die den Attributwert `Alfreds Futterkiste` haben.