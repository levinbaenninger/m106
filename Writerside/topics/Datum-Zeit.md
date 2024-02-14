# Datum/Zeit

| Datentyp    | Format              | Gültigkeitsbereich                                  |
|-------------|---------------------|-----------------------------------------------------|
| `DATE`      | YYYY-MM-DD          | '1000-01-01' bis '9999-12-31'                       |
| `TIME`      | [h]hh:mm:ss         | '838:59:59' bis '838:59:59'                         |
| `DATETIME`  | YYYY-MM-DD hh:mm:ss | '1000-01-01 00:00:00' bis '9999-12-31 23:59:59'     |
| `TIMESTAMP` | YYYY-MM-DD hh:mm:ss | '1970-01-01 00:00:00' bis '2038-01-19 03:14:07' UTC |

## CURRENT_DATE

In SQL gibt es noch die Variable `CURRENT_DATE` diese gibt uns das aktuelle Datum zurück im `TIMESTAMP`-Format. Das ist beispielsweise für Abfragen praktisch:

````SQL
SELECT * FROM foo 
WHERE BirthDate < CURRENT_DATE;
````

## TIMESTAMP

Ein Timestamp ist beispielsweise praktisch für solche Tabellen:

````SQL
CREATE TABLE user (
	id INT PRIMARY KEY AUTO_INCREMENT,
	name VARCHAR(40) NOT NULL,
	password VARCHAR(256) NOT NULL,
	created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
	updated_at TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
);
````