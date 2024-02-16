# Benutzer erstellen

Mit `CREATE USER` können wir einen Benutzer erstellen.

## CREATE USER - Syntax

````SQL
CREATE USER
benutzername@hostname
IDENTIFIED BY password;
````

## CREATE USER - Beispiele

Hier erstellen wir einen User nur für den `localhost`.

````SQL
CREATE USER
hr_manager@localhost
IDENTIFIED BY 'secret';
````

Um einen User für alle Hosts zu verwenden, können wir folgendes machen:

````SQL
CREATE USER
hr_manager@'%'
IDENTIFIED BY 'secret';
````