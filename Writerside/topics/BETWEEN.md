# BETWEEN

Mit dem `BETWEEN`-Operator können wir Werte in einem bestimmten Wertebereich auswählen. Das können Zahlen, Texte oder Daten sein.

> Der Operator ist teilweise inklusiv, heisst der Startwert ist auch im Wertebereich

## BETWEEN - Syntax

````SQL
SELECT column_name(s)
FROM table_name
WHERE column_name BETWEEN value1 AND value2; 
````

## BETWEEN - Beispiel

````SQL
SELECT * FROM Product
WHERE Price BETWEEN 10 AND 20;
````