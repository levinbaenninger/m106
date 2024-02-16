# Zugriffsrechte vergeben

Um Zugriffsrechte zu vergeben, nutzen wir das `GRANT`-Statement. Dabei ist zu beachten, dass nur der **`root`**-User Rechte vergeben kann.

## GRANT - Syntax

````SQL
GRANT rechteliste 
ON db.tabelle
TO benutzer@hostname;
````

## GRANT - Beispiele

Alle Rechte vergeben für die Datenbank `firma` und Tabelle `mitarbeiter`:

````SQL
GRANT ALL 
ON firma.mitarbeiter
TO hr_manager@localhost;
````

Bestimmte Zugriffsrechte verteilen:

````SQL
GRANT SELECT, INSERT, DELETE
ON firma.mitarbeiter
TO hr_manager@localhost;
````

