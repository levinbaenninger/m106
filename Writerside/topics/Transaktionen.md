# Transaktionen

Eine Transaktion fässt mehrere Arbeitsschritte zusammen und sorgt dafür, dass diese alle zusammen ausgeführt werden, oder alle zusammen nicht ausgeführt werden (Alles-oder-nichts-Prinzip).

Wenn irgendeine Aufgabe fehlschlägt, fehlt die gesamte Transaktion fehl. Somit werden keine fehlerhaften Daten geschrieben.

## ACID

Eine Transaktion muss immer diese vier Eigenschaften erfüllen:

- **Atomic**: Die komplette Transaktion muss erfolgreich sein, ansonsten werden alle Änderungen rückgängig gemacht
- **Consistency**: Datenbank muss bei einer Transaktion in einem gültigen Zustand bleiben
- **Isolation**: Gleichzeitige Transaktionen sind isoliert voneinander, somit können dieselben Daten nicht von verschiedenen Transaktionen bearbeitet werden
- **Durability**: Mit Commit abgeschlossene Änderungen sind persistent