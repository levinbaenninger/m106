# Datenschutz und Berechtigungen

Das Datenschutzgesetz bildet die gesetzliche Grundlage bzgl. Datenschutz, auch im Cyberraum. Zwei Artikel haben da für dich als Entwickler oder Systemadministrator besondere Bedeutung.

> **Bundesverfassung Art.13**
> 
> <sup>1</sup> Jede Person hat Anspruch auf Achtung ihres Privat-
> und Familienlebens, ihrer Wohnung sowie ihres Brief-, Post- und Fernmeldeverkehrs.
>
> <sup>2</sup> Jede Person hat Anspruch auf Schutz vor Missbrauch ihrer persönlichen Daten.

> **Datenschutzgesetz Art. 7**
> 
> Personendaten müssen durch angemessene technische
und organisatorische Massnahmen gegen unbefugtes Lesen und Bearbeiten geschützt werden.

Konkret heisst das, dass wir für die sichere Aufbewahrung der Daten unserer Benutzer verantwortlich sind. Wir sind dazu verpflichtet angemessene Schutzmassnahmen zu treffen.

## DCL

Um Datenschutz und Berechtigungen zu Verwalten nutzen wir eine weitere Sprachschicht von SQL, die **Data Control Language** kurz DCL.

Mit DCL können wir Benutzer hinzufügen / entfernen:

**`CREATE`** / **`DROP USER`**

und Rechte hinzufügen bzw. entfernen:

**`GRANT`** / **`REVOKE`**