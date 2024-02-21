# Datenbankinformationen auslesen

Die Datenbankinformationen sind in der `information_schema`-Datenbank gespeichert. Diese Datenbank ist auf jedem MySQL Server vorhanden und stellt uns viele Informationen zu Verfügung:

- Vorhandene Datenbanken / Tabellen
- Speichernutzung
- etc.

Um die Informationen auszulesen, können wir folgendes machen:

````SQL
USE information_schema
SHOW TABLES;            -- Namen der Tabellen anzeigen
SELECT * FROM schemata  -- Alle Datenbanken des Servers anzeigen
SELECT * FROM tables    -- Alle Tabellen Anzeigen
````

Eine weiter nützliche Funktion ist das Auslesen der Tabellengrösse:

````SQL
SELECT 
    table_schema AS datenbank
    table_name AS tabelle
    ROUND(((data_length+index_length)/1024/1024), 2) AS size_in_mb
FROM information_schema.tables
WHERE table_schema = "cocktail"
````