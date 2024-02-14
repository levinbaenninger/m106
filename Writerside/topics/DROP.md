# DROP

<show-structure depth="2" />

Mit dem `DROP`-Befehl können wir Datenbanken und Tabellen löschen.

## Datenbank erstellen

### Syntax - Datenbank löschen

Wir können folgende Syntax nutzen, um eine Datenbank zu löschen:

````SQL
DROP DATABASE databasename;
````

### Beispiel - Datenbank löschen

In folgendem Beispiel löschen wir eine Datenbank namens `testDB`:

````SQL
DROP DATABASE testDB;
````

## Tabelle löschen

### Syntax - Tabelle löschen

Wir können folgende Syntax nutzen, um eine Tabelle zu löschen:

````SQL
DROP TABLE table_name;
````

### Beispiel - Tabelle löschen

In folgendem Beispiel löschen wir eine Tabelle namens `Shippers` und all die darin enthaltenen Daten.

`````SQL
DROP TABLE Shipper;
`````

