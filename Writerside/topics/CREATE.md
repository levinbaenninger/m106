# CREATE

<show-structure depth="2" />

Mit dem `CREATE`-Befehl können wir Datenbanken und Tabellen erstellen.

## Datenbank erstellen

### Syntax - Datenbank erstellen

Wir können folgende Syntax nutzen, um eine Datenbank zu erstellen:

````SQL
CREATE DATABASE databasename;
````

### Beispiel - Datenbank erstellen

In folgendem Beispiel erstellen wir eine Datenbank namens `testDB`:

````SQL
CREATE DATABASE testDB;
````

## Tabelle erstellen

### Syntax - Tabelle erstellen

Wir können folgende Syntax nutzen, um eine Tabelle zu erstellen:

````SQL
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
   ....
);
````

### Beispiel - Tabelle erstellen

In folgendem Beispiel erstellen wir eine Tabelle namens `Person` mit verschiedenen Attributen, wie Vorname und Nachname.

`````SQL
CREATE TABLE Person (
    PersonID int,
    LastName varchar(50),
    FirstName varchar(50),
    Address varchar(50),
    City varchar(50)
);
`````

