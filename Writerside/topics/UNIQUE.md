# UNIQUE

Das Constraint `UNIQUE` versichert uns, dass alle Werte in einem Attribut einzigartig sind.

## UNIQUE - CREATE TABLE

````SQL
CREATE TABLE Person (
    PersonID INTEGER NOT NULL,
    LastName VARCHAR(45) NOT NULL,
    FirstName VARCHAR(45),
    Age INTEGER,
    CONSTRAINT UQ_Person_LastName UNIQUE (LastName)
); 
````

## UNIQUE - ALTER TABLE

### UNIQUE-Constraint hinzufügen

````SQL
ALTER TABLE Person
ADD CONSTRAINT UQ_Person_LastName UNIQUE (LastName); 
````

### UNIQUE-Constraint entfernen

````SQL
ALTER TABLE Person
DROP INDEX UQ_Person_LastName; 
````

