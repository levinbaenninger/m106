# Datenbank optimieren

Die Performance einer Datenbank ist gerade in der Zeit von Big Data ein nicht zu vernachlässigendes Thema. Eine Datenbank mit mehreren Millionen Datensätzen braucht viel Ressourcen, weshalb es für uns wichtig ist, diese auch sparsam zu verwenden.

Es gibt viele Faktoren, die einen Einfluss auf die Performance haben, wie beispielsweise die Hardware, die Query Komplexität, Datenmenge oder Resultatgrösse um einige zu nennen.

Wir können dem Ressourcenbedarf jedoch auf verschiedene Arten entgegenwirken. Bei jedem Query das wir absetzten, gibt MySQL Workbench im Action Output und die Duration- und Fetch-Zeiten zurück.

**Duration**: Dauer des Queries auf dem Server
**Fetch**: Dauer für das Holen und Übertragen der Daten

Eine hohe Duration weist meist auf ein komplexes Query, eine grosse Datenmenge in der Datenbank oder auf hohe Belastung des Servers hin. Eine lange Fetch-Dauer hingegen weist auf eine grosse Netzwerkbelastung oder Resultatgrösse hin.

Insbesondere bei grossen Datenmengen, können wir mit einem Index auf eine Spalte, die häufig Teil von komplexen Queries ist, die Duration stark reduzieren.
[Hier](https://www.youtube.com/watch?v=kv3jC0P4gOc) hast du eine gute Erklärung zum Sinn und Zweck von Indexes.

Den Fetch hingegen, kann man mit` SELECT values FROM table LIMIT 100` sehr einfach reduzieren. Durch das Limit werden in diesem Fall nur die ersten 100 Resultate zurückgegeben. Wenn die Vollständigkeit des Resultates hohe Priorität hat, ist das keine gute Variante.