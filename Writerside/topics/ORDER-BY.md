# ORDER BY

<show-structure depth="2" />

Das `ORDER BY`-Keyword wird benutzt, um das Resultat in aufsteigender oder absteigender Reihenfolge zu sortieren.

Standardmässig sortiert das `ORDER BY`-Keyword in aufsteigender Reihenfolge.

## ORDER BY - Syntax

````SQL
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
````

## ORDER BY - Beispiele 

### Aufsteigende Reihenfolge

````SQL
SELECT * FROM Customer
ORDER BY Country;
````

### Absteigende Reihenfolge

````SQL
SELECT * FROM Customer
ORDER BY Country DESC;
````