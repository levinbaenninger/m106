# Unterabfragen

Unterabfragen sind einfach gesagt verschachtelte DQL und DQL Queries. Bei Subqueries gibt es keine Syntax, wie beispielsweise bei Joins, aber es gibt gewisse Regeln, welche in den Beispielen visualisiert werden.

## Beispiele - Unterabfragen

### Einfacher Subquery mit WHERE

````SQL
SELECT name FROM ort
WHERE id IN (
    SELECT ort_id FROM kunde
    WHERE vorname LIKE 'F%'
);
````

### Einfacher Subquery mit FROM

````SQL
SELECT AVG(anzahl_zutaten) FROM (
    SELECT COUNT(zutat_id) AS anzahl_zutaten FROM pizza_zutat
    GROUP BY pizza_id
) T;
````

### Einfacher Subquery mit JOIN

````SQL
SELECT strasse, o.plz, o.name FROM kunde
JOIN ort AS o ON kunde.ort_id = o.id
WHERE kunde.id IN (
    SELECT kunde_id FROM bestellung
    WHERE id = 3
);
````

### Fortgeschrittener Subquery mit WHERE

````SQL
SELECT name FROM zutat
WHERE id IN (
    SELECT zutat_id FROM pizza_zutat
    WHERE pizza_id IN (
        SELECT id FROM pizza
        WHERE preis = (
            SELECT MAX(preis) FROM pizza
        )
    )
);
````

### Komplizierter Subquery mit FROM & WHERE

````SQL
SELECT name FROM zutat
WHERE id IN (
    SELECT zutat_id
    FROM (SELECT zutat_id, COUNT(*) as anzahl
          FROM pizza_zutat GROUP BY zutat_id) T
    WHERE anzahl = (
        SELECT MAX(anzahl)
        FROM (SELECT zutat_id, COUNT(*) as anzahl
              FROM pizza_zutat GROUP BY zutat_id) TT
    )
);
````
