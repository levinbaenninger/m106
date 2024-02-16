# JOINS und Aggregatsfunktionen

Dieses Kapitel fasst mehrere Themen zusammen. Abfragen über mehrere Tabellen, Gruppieren von Ausgaben und sowie Aggregatsfunktionen.

Wenn wir Abfragen über mehrere Tabellen absetzten möchten. können wir diese mit `JOIN` verbinden. Mit `JOIN` wird der Primary und der Foreign Key zweier Tabellen aufgelöst und Werte beider Tabellen können im Output abgerufen werden. Ein einfaches Beispiel dafür wäre:

````SQL
SELECT m.name as Name, f.name AS Firma
FROM mitarbeiter AS m
JOIN firma AS f ON m.firma_id = f.id;
````

Speziell gibt es noch den `RIGHT` / `LEFT` `JOIN`. Diese unterscheiden sich von einem normalen `JOIN` darin, die Tabelle Links oder Rechts vom Join (Wortwörtlich im Query Links/Rechts) vollständig ausgeben, auch wenn ein Foreign Key nicht aufgelöst werden kann.

Das `GROUP BY` wird dafür verwendet, um Werte in einem Output anhand einer Spalte, bzw. einem Attribut zu Gruppieren.

Mit den Aggregatsfunktionen können wir verschiedene Mathematische Funktionen auf unserem Output durchführen. Beispielsweise `COUNT(column)`, `SUM(column)`, `AVG(column)`, uvm. Insbesondere in Kombination mit `GROUP BY`, sind die Aggregatsfunktionen häufig in Verwendung.

