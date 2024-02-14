# LIMIT

Mit `LIMIT` können wir die Anzahl Datensätze, die uns eine Abfrage zurückgibt, limitieren.

## LIMIT - SYNTAX

````SQL
SELECT column_name(s)
FROM table_name
WHERE condition
LIMIT number; 
````

## LIMIT - Beispiel

In folgendem Beispiel werden nur 3 Datensätze zurückgegeben:

````SQL
SELECT * FROM Customer
LIMIT 3; 
````

Was aber, wenn wir die Datensätze 4 bis 6 haben wollen? Kein Problem:

````SQL
SELECT * FROM Customer
LIMIT 3 OFFSET 3; 
````
