# Performance messen

In MySQL Workbench können wir in der sog. **Output View**, die Duration und Fetch einsehen:

- **Duration**: Dauer des Queries auf dem Server
- **Fetch**: Dauer für das Holen und Übertragen der Daten

Um eine genaue Analyse eines Queries anzuzeigen, können wir das `EXPLAIN`-Statement vor das Query setzen.

````SQL
EXPLAIN SELECT name FROM ort
WHERE id IN (
	SELECT ort_id FROM Kunde
	WHERE vorname LIKE "F%"
);
````
