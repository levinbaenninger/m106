# AUTO INCREMENT

Mit `AUTO_INCREMENT` können wir eine einzigartige Zahl automatisch generieren, wenn ein neuer Datensatz erstellt wird. Es wird oftmals in Kombination mit dem Primärschlüssel verwendet.

## Beispiel

````SQL
CREATE TABLE Person (
    PersonID INTEGER AUTO_INCREMENT,
    LastName VARCHAR(255) NOT NULL,
    FirstName VARCHAR(255),
    Age INTEGER,
    CONSTRAINT PK_Person PRIMARY KEY (PersonID)
); 
````