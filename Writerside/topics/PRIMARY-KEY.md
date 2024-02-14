# PRIMARY KEY

Das `PRIMARY KEY`-Constraint erstellt einen Primärschlüssel in der Tabelle. Eine Tabelle kann dabei nur einen Primärschlüssel haben.

## PRIMARY KEY - CREATE TABLE

````SQL
CREATE TABLE Person (
    PersonID INTEGER NOT NULL,
    LastName VARCHAR(45) NOT NULL,
    FirstName VARCHAR(45),
    Age INTEGER,
    CONSTRAINT PK_Person PRIMARY KEY (PersonID)
); 
````

## PRIMARY KEY - ALTER TABLE

### PRIMARY KEY hinzufügen

````SQL
ALTER TABLE Person
ADD CONSTRAINT PK_Person PRIMARY KEY (PersonID, LastName); 
````

> Hier erstellen wir einen Primärschlüssel, welcher aus zwei Werten besteht (zusammengesetzter Primärschlüssel). 
> 
> Zudem ist wichtig zu beachten, dass wenn man `ALTER TABLE` nutzt, dass die Werte nicht `NULL` sind.

### PRIMARY KEY entfernen

````SQL
ALTER TABLE Person
DROP PRIMARY KEY; 
````