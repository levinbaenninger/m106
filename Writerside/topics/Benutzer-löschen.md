# Benutzer löschen

Es gibt zwei Möglichkeiten einen User zu löschen, einerseits mit `DROP USER`, andererseits den Datensatz in der Tabelle `[MYSQL.]USER` löschen.

## DROP USER

### DROP-USER - Syntax

````SQL
DROP USER benutzer@hostname;
````

### DROP USER - Beispiel

````SQL
DROP USER
hr_manager@localhost;
````

## Datensatz löschen

### Datensatz löschen - Syntax

````SQL
DELETE FROM mysql.user
WHERE user = benutzername;
````

### Datensatz löschen - Beispiel

````SQL
DELETE FROM mysql.user
WHERE user = 'hr_manager';
````