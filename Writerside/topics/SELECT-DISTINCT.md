# SELECT DISTINCT

<show-structure depth="2" />

Der `SELECT DISTINCT`-Befehl funktioniert ganz ähnlich, wie der `SELECT`-Befehl. Jedoch filtert er Duplikate heraus.

## SELECT DISTINCT - Syntax

````SQL
SELECT DISTINCT column1, column2, ...
FROM table_name;
````

## SELECT DISTINCT - Beispiel

Im folgenden Beispiel wählen wir das Attribut `County` aus der Tabelle `Customer` aus, die einzigartig sind:

````SQL
SELECT DISTINCT Country FROM Customer;
````