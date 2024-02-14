# CHECK

Mit dem `CHECK`-Constraint können wir den Wertebereich limitieren.

## CHECK - CREATE TABLE

````SQL
CREATE TABLE Person (
    PersonID INTEGER NOT NULL,
    LastName VARCHAR(255) NOT NULL,
    FirstName VARCHAR(255),
    Age INTEGER,
    City VARCHAR(255),
    CONSTRAINT CK_Person_Age CHECK (Age >= 18)
); 
````

## CHECK - ALTER TABLE

### CHECK-Constraint hinzufügen

````SQL
ALTER TABLE Person
ADD CONSTRAINT CK_Person_Age CHECK (Age >= 18); 
````

### CHECK-Constraint entfernen

````SQL
ALTER TABLE Person
DROP CHECK CK_Person_Age; 
````

