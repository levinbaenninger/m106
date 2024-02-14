# AND, OR, NOT

<show-structure depth="2" />

Die `WHERE`-Klausel kann mit den `AND`, `OR` und `NOT` Operatoren kombiniert werden.

Sie funktionieren gleich wie in den bekannten Programmiersprachen.

## Syntax

### AND - Syntax

````SQL
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2 AND condition3 ...;
````

### OR - Syntax

````SQL
SELECT column1, column2, ...
FROM table_name
WHERE condition1 OR condition2 OR condition3 ...;
````

### NOT - Syntax

````SQL
SELECT column1, column2, ...
FROM table_name
WHERE NOT condition;
````

## Beispiele

### AND - Beispiel

Alle Kunden, die aud Deutschland sind **und** aus Berlin kommen

````SQL
SELECT * FROM Customer
WHERE Country = 'Germany' AND City = 'Berlin';
````

### OR - Beispiel

Alle Kunden, die aus Berlin **oder** Stuttgart sind

````SQL
SELECT * FROM Customer
WHERE City = 'Berlin' OR City = 'Stuttgart';
````

### NOT - Beispiel

Alle Kunden, die **nicht** aus Deutschland kommen

````SQL
SELECT * FROM Customer
WHERE NOT Country = 'Germany';
````

### Kombination - Beispiel

````SQL
SELECT * FROM Customer
WHERE Country = 'Germany' AND (City = 'Berlin' OR City = 'Stuttgart');
````

Alle Kunden, die von Deutschland kommen **und** aus Berlin **oder** Stuttgart sind.
