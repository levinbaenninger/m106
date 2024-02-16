# ALTER

<show-structure depth="2" />

Das `ALTER`-Statement wird benutzt, um bei einer existierenden Tabelle Attribute hinzuzufügen, zu löschen oder zu modifizieren. 

## Attribut hinzufügen

### Syntax - Attribut hinzufügen

Wir benutzen folgende Syntax, um ein Attribut in einer bereits existierenden Tabelle hinzuzufügen:

````SQL
ALTER TABLE table_name
ADD COLUMN column_name datatype;
````

### Beispiel - Attribut hinzufügen

Im folgenden Beispiel fügen wir der Tabelle `Customer` das Attribut `Email` hinzu. 

````SQL
ALTER TABLE Customer
ADD COLUMN Email VARCHAR(50);
````

## Attribut löschen

### Syntax - Attribut löschen

Um ein Attribut in einer Tabelle zu löschen, benutzen wir folgende Syntax:

````SQL
ALTER TABLE table_name
DROP COLUMN column_name;
````

### Beispiel - Attribut löschen

Im folgenden Beispiel wird in der Tabelle `Customer` das Attribut `Username` entfernt.

````SQL
ALTER TABLE Customer
DROP COLUMN Username;
````

## Datentyp ändern

### Syntax - Datentyp ändern

Um den Datentyp eines Attributs zu ändern, benutzen wir folgende Syntax:

````SQL
ALTER TABLE table_name
MODIFY COLUMN column_name datatype;
````

### Beispiel - Datentyp ändern

In diesem Beispiel ändern wir den Datentypen von `DateOfBirth` von `DATE` auf `YEAR`:

````SQL
ALTER TABLE Person
MODIFY COLUMN DateOfBirth YEAR;
````

## Attribut umbenennen

### Syntax - Attribut umbenennen

````SQL
ALTER TABLE table_name
CHANGE oldColumnName newColumnName dataType;
````

### Beispiele - Attribut umbenennen

````SQL
ALTER TABLE Person
CHANGE Name Surname VARCHAR(45);
````

