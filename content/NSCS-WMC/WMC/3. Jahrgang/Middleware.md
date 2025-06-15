#wmc #matura #Middleware

> Middleware bietet Applikationsinfrastruktur für Anwendungen zur Laufzeit

Bdt. Middleware ist nicht dasselbe wie eine Libary, kommt dem ganzen aber relativ nahe.
Middleware ist beispielsweise eine externe Authentifikation.
1. Main Programm erhält login Daten
2. Gibt die Daten an die Middleware weiter
3. Erhält Feedback (Ähnlich einer Funktion)
4. Arbeitet weiter

Genaue Abgrenzung zwischen Library und Middleware -> unbekannt

**Typische Geschäftsanwendungen haben...**
- 70-80% Applikationsinfrastruktur die sich von Anwendung zu Anwend. kaum unterscheidet
- 20-30% spezifisch für die Anwendung

**Middleware Services**
- Konkrete Funktionen o. Dienste die bereitgestellt werden
- Erleichtern Skalierbarkeit
- Services für DB Zugriff
- Security: Authentifizierung, Berechtigungen etc.

**Framework**

> Programmiergerüst, dass einen Rahmen zur Verfügung stellt, innerhalb dessen der Programmierer eine Anwendung erstellt

- Häufige, wiederauftretende Probleme werden in Frameworks gelöst
- Der Entwickler muss nur die für seine Anwendung spezifischen Teile implementieren
- Frameworks ersparen arbeit, geben allerdings oft die Architektur der Anwendung vor

**Logging Frameworks...**
- Loggen den Programmablauf weil normales System.Out oder Console.Writeline zu based ist
- Haben fancy Logging Levels (Debug, Info, Trace...) (Debug, Trace nur für Entwickler wg Größe)
- Normalerweise 1 File / Tag

**Dependency Injection**
- Abhängigkeiten sollen entfernt werden, der Code muss dynamischer sein
- Passwörter, Usernames etc sollen nicht einfach in den Code sondern werden in externe Config Files geschrieben und richtig annotiert - vom Framework erkannt und so verwendet

**Object Relational Mapper (ORM)**
- Erlauben es in OOP Sprachen Objekte direkt mit Tables in der DB zu verknüpfen
- EF Core in C# (User angelegt, db migrations, danach is user.pw, user.name etc available)


**JWT Json Web Token**
- Ein sicherer kompakter Token in JSON Format
- Verwendet für Auth zwischen Client und Server
- Besteht aus Header, Payload und Signatur -> Verhindert Manipulationen

