# Komplexe Queries

`JOIN`-, `WHERE`- und `GROUP BY`-Operationen sind fast immer notwendig, erfordern jedoch viel Rechenleistung.

Diese Operationen können mit dem Setzen von **Indizes** optimiert werden:

## Index erstellen

````SQL
CREATE INDEX index_name
ON table_name (column1, column2, ...)
````

## DROP INDEX

````SQL
ALTER TABLE
DROP INDEX index_name
````

