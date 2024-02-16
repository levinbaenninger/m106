# Zugriffsrechte entziehen

Um Zugriffsrechte zu entziehen, nutzen wir den `REVOKE`-Befehl.

## REVOKE - Syntax

````SQL
REVOKE rechteliste
ON db.tabelle
FROM benutzer@hostname;
````

## REVOKE - Beispiele

````SQL
REVOKE ALL
ON firma.mitarbeiter
FROM hr_manager@localhost;
````