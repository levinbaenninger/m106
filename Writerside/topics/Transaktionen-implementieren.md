# Transaktionen implementieren

**Wichtig**: Die folgenden Statements können nur mit DML-Commands, wie `INSERT`, `UPDATE` und `DELETE` verwendet werden.

## Transaktion starten

Um eine Transaktion zu starten, machen wir Folgendes:

````SQL
START TRANSACTION
````

## COMMIT

Wenn mit den Statements alles in Ordnung ist, werden alle Änderungen zusammen gespeichert. Der `COMMIT`-Command speichert alle Transaktionen in der Datenbank.

````SQL
COMMIT;
````

## ROLLBACK 

Wenn irgendwelche Fehler in den gruppierten SQL-Statements auftreten, müssen alle Änderungen rückgängig gemacht werden. Das geht mit dem `ROLLBACK`-Command:

````SQL
ROLLBACK;
````