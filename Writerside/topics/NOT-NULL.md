# NOT NULL

Standardmässig kann ein Attributwert den Wert `NULL` bekommen. Um das zu verhindern, gibt es das `NOT NULL`-Constraint.

## NOT NULL - CREATE TABLE

````SQL
CREATE TABLE Person (
    PersonID INTEGER NOT NULL,
    LastName VARCHAR(45) NOT NULL,
    FirstName VARCHAR(45) NOT NULL,
    Age INTEGER
); 
````

## NOT NULL - MODIFY TABLE

````SQL
ALTER TABLE Person
MODIFY Age INTEGER NOT NULL; 
````