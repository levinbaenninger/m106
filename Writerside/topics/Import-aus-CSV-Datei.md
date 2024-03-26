# Import aus CSV-Datei

Am häufigsten werden Daten aus einer CSV-Datei in eine Datenbank migriert. Dafür gibt uns MySQL einige Tools an die Hand. Jedoch müssen davor einige Vorbereitungen getroffen werden.

> **Wichtig:** Das CSV-File muss in der UTF-8 Codierung sein. Darüber hinaus darf es nicht UTF-8-BOM sein, da BOM mit den meisten Binaries nicht kompatibel ist.

{ style="warning" }

## Syntax - CSV-Import

### Dateipfad

Als Erstes müssen wir herausfinden, wo wir die zu importierenden Dateien ablegen müssen. Dazu nutzen wir folgenden Query:

````SQL
SHOW VARIABLES LIKE 'secure_file_priv';
````

In dem daraus resultierenden Pfad müssen wir unsere Dateien ablegen.

### Alte Daten löschen

Als Nächstes müssen bzw. können wir alle Tabellen leeren. Dabei sollte man ein wenig auf die Reihenfolge achten: Zuerst Child-Tabellen leeren, danach Parent-Tabelle.

````SQL
DELETE FROM person;
DELETE FROM firma;
DELETE FROM ort;
````

Gleichzeitig können wir, wenn nötig, `AUTO_INCREMENT` auf 1 zurücksetzen. Dies verhindert, dass beim Import der Daten noch alte Foreign Keys referenziert werden.

````SQL
ALTER TABLE person AUTO_INCREMENT = 1;
ALTER TABLE firma AUTO_INCREMENT = 1;
ALTER TABLE ort AUTO_INCREMENT = 1;
````

### Foreign-Key Check ausschalten

Um beim Import nicht mit Fehlern, bezüglich Relationen bombadiert zu werden, sagen wir, dass Foreign-Keys nicht überprüft werden sollen:

````SQL
SET foreign_key_checks = 0;
````

### Import

Beim Import selbst müssen wir ein paar Parameter festlegen, bspw. den Pfad, oder den Zeichensatz:

````SQL
LOAD DATA INFILE 
'C:\\ProgramData\\MySQL\\MySQL Server 8.0\\Uploads\\firmen.csv' -- Path des Infiles
INTO TABLE firma 			                                    -- Tabelle in der Datenbank
CHARACTER SET utf8mb4 		                                    -- Codierung in der Datenbank -> Wichtig das im CSV auch auf UTF8 eingestellt ist
FIELDS TERMINATED BY ';' 	                                    -- Trennzeichen zweier Werte im CSV
LINES TERMINATED BY '\r\n'	                                    -- Zeilenumbruch im CSV
ignore 1 rows 				                                    -- Erste Zeile mit Attributen soll nicht geladen werden
(id, firmenname, Inhaber, ort_id);				                -- Namen wie in Datenbank, Reihenfolge wie in CSV
````

### Foreign-Key Check aktivieren

Nachdem alle Files importiert wurden, aktivieren wir den Foreign-Key Check wieder:

````SQL
SET foreign_key_checks = 1;
````