# INSERT

<show-structure depth="2" />

Das `INSERT INTO`-Statement wird verwendet, um Datensätze in eine Tabelle einzufügen.

## INSERT INTO - Syntax

Es gibt zwei Arten, um Daten in eine Tabelle einzufügen. In der folgenden spezifizieren wir sowohl die Attribute, als auch die Werte: 

````SQL
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
````

Im anderen Fall fügen wir Daten für alle Attribute ein. Bei dieser Syntax muss jedoch die Reihenfolge der Werte mit der, der Tabelle übereinstimmen.

````SQL
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
````

## INSERT INTO - Beispiel

````SQL
INSERT INTO Customer (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES 
('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway'),
('Wolski', 'Zybesk', 'ul. Filtrowa 68', 'Walla', '01-012', 'Poland');
````

In diesem Beispiel fügen wir zwei Datensätze in die Tabelle `Customer` ein. Das einzige Feld, welches wir nicht explizit definieren ist die `CustomerId`. Denn diese ist ein `AUTO_INCREMENT` Feld, es wird also automatisch ausgefüllt.

Wir können aber auch Daten nur in spezifischen Feldern einfügen:

````SQL
INSERT INTO Customer (CustomerName, City, Country)
VALUES ('Cardinal', 'Stavanger', 'Norway');
````

Alle Attribute, die nicht ausgefüllt wurden, werden mit `NULL` ausgefüllt.