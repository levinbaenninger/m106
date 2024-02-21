# Fragmentierung

Mit dem **Ändern** und **Löschen** von Datensätzen können die entsprechenden Daten wie ein Dateisystem fragmentiert werden. 

Mit folgendem Befehl können wie die Fragmentierung überprüfen:

````SQL
SHOW TABLE STATUS;
    Data_Length     -- Grösse der eigentlichen Daten
    Index_Length    -- Grösse der Indizies
    Data_Free       -- Freier Speicher zwischen den Daten
````

Oben sind die wichtigsten Daten in dieser Tabelle beschrieben. Um die Tabellen nun zu optimieren, machen wir folgendes:

````SQL
OPTIMIZE TABLE tablename;
````
