# Constraints

Mit Constraints können Regeln für Daten in einer Tabelle spezifiziert werden. Dafür gibt es mehrere Möglichkeiten:

- **`NOT NULL`** - Attributwert muss ausgefüllt werden
- **`UNIQUE`** - Attributwert muss einzigartig sein
- **`PRIMARY KEY`** - Eine Kombination aus `NOT NULL` und `UNIQUE`, identifiziert den Datensatz eindeutig.
- **`FOREIGN KEY`** - Referenziert Primärschlüssel aus einer anderen Tabelle
- **`CHECK`** - Attributwert muss bestimmte Konditionen erfüllen
- **`DEFAULT`** - Setzt einen Standardwert, wenn kein Wert angegeben wird
