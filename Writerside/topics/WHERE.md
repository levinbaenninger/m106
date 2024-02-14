# WHERE

<show-structure depth="2" />

Die `WHERE`-Klausel wir benutzt, um Datensätze zu filtern.

## WHERE - Syntax

````SQL
SELECT column1, column2, ...
FROM table_name
WHERE condition;
````

> Die `WHERE`-Klausel wird nicht nur bei `SELECT`-Statements, sondern auch bei `UPDATE`, `DELETE`, etc. verwendet

## WHERE - Beispiel

````SQL
SELECT * FROM Customer
WHERE Country = 'Mexico';
````

In diesem Beispiel werden alle Kunden von Mexiko ausgewählt.

## Operatoren in der `WHERE`-Klausel

Folgende Operatoren können in der `WHERE`-Klausel verwendet werden:

| Operator | Beschreibung                         |
|----------|--------------------------------------|
| =        | Gleich                               |
| >        | Grösser als                          |
| <        | Kleiner als                          |
| >=       | Grösser oder gleich                  |
| <=       | Kleiner oder gleich                  |
| <>       | Nicht gleich                         |
| BETWEEN  | Zwischen einer bestimmten Reichweite |
| LIKE     | Nach einem Muster suchen (RegEx)     |
| IN       | Mehrere mögliche Werte spezifizieren |
