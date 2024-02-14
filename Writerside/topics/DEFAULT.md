# DEFAULT

Das `DEFAULT`-Constraint wird verwendet, um einen Standardwert zu setzen, falls keiner spezifiziert wird.

## DEFAULT - CREATE TABLE

````SQL
CREATE TABLE Order (
    OrderId INTEGER NOT NULL,
    OrderNumber INTEGER NOT NULL,
    OrderDate date DEFAULT CURRENT_DATE()
); 
````

## DEFAULT - ALTER TABLE

### DEFAULT-Constraint hinzufügen

````SQL
ALTER TABLE Person
ALTER City SET DEFAULT 'New York'; 
````

### DEFAULT-Constraint entfernen

````SQL
ALTER TABLE Person
ALTER City DROP DEFAULT; 
````
