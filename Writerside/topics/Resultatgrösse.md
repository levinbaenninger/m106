# Resultatgrösse

Je mehr Daten auf dem Server gelesen und an den Client gesendet werden müssen, desto langsamer die Abfrage.

Dabei gibt es zwei Möglichkeiten das zu optimieren:

- `SELECT * FROM...` vermeiden und nur die nötigen Attribute laden
- Anzahl Datensätze mit [`LIMIT`](LIMIT.md) limitieren 