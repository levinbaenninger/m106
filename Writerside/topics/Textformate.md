# Textformate

| Datentyp     | Eigenschaft                                                         |
|--------------|---------------------------------------------------------------------|
| `CHAR(m)`    | Eine Zeichenkette fester Länge mit max. 255 Zeichen                 |
| `VARCHAR(m)` | Eine Zeichenkette variabler Länge mit max. 65'535 Zeichen           |
| `TEXT`       | Längere Texte, variabler Länge, extern gespeichert, etwas langsamer |
| `LONGTEXT`   | Ein Text mit variabler Länge, max. 4.2GB                            |

## Verschlüsselung

In SQL ist es möglich Daten mit dem SHA256 bzw. SHA512 Algorithmus zu verschlüsseln. Das sieht so aus:

````SQL
INSERT INTO user (name, password) 
VALUES
    ('marco',  sha2('Passwort123', 512)),
    ('martin', sha1('Hallo0987'));
````

Der Wert sieht im Feld dann beispielsweise so aus: `5bf77a370c08f5f5b20fab75849116...`