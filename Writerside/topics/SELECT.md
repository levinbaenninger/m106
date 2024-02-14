# SELECT

Das `SELECT`-Statement wird benutzt um bestimmte Daten aus einer Datenbank auszuwählen.

## SELECT - Syntax

````SQL
SELECT column1, column2, ...
FROM table_name;
````

Um alle Attribute auszuwählen, kann man den `*` benutzen.

## SELECT - Beispiel

Im folgenden Beispiel wählen wir alle Attribute aus der Tabelle `Customer` aus:

````SQL
SELECT * FROM Customer;
````