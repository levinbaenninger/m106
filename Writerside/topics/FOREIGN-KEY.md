# FOREIGN KEY

Mit dem `FOREIGN KEY`-Constraint können wir auf den Primärschlüssel in einer anderen Tabelle verweisen. Die Tabelle mit dem Fremdschlüssel wird **Child-Table** genannt, die Tabelle mit dem Primärschlüssel wir **Parent-Table** genannt.

## FOREIGN KEY - CREATE TABLE

````SQL
CREATE TABLE Order (
    OrderID INTEGER NOT NULL,
    OrderNumber INTEGER NOT NULL,
    PersonID INTEGER,
    CONSTRAINT FK_Order_PersonOrder_Person FOREIGN KEY (PersonID) REFERENCES Person(PersonID)
); 
````

## FOREIGN KEY - ALTER TABLE

### FOREIGN KEY hinzufügen

````SQL
ALTER TABLE Order
ADD CONSTRAINT FK_Order_PersonOrder_Person FOREIGN KEY (PersonID) REFERENCES Person(PersonID); 
````

### FOREIGN KEY löschen

````SQL
ALTER TABLE Order
DROP FOREIGN KEY FK_Orer_PersonOrder_Person; 
````