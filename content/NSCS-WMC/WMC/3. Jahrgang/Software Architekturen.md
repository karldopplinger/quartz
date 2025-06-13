#wmc #matura #Software #Architektur

> Software Architektur befasst sich mit der Aufteilung des Programmcodes in verschiedene Komponenten und deren Zusammenwirkung

Software Architekturen sind notwendig um Code zu organisieren, skalierbar zu entwickeln, ihn performant zu machen und dessen Komplexität zu beherrschen.

Monolithischer Aufbau (alles in eine Anwendung), ist schlecht weil dadurch die Skalierbarkeit geschadet wird, die Wartbarkeit und Weiterentwicklung erschwert wird, die Fehlertoleranz steigt etc.

**Seperation of Concern**
- Einteilung in Client, Server, Service
- Definieren von Schichten (layering)
- Implementierung und aufteilen auf Komponenten

**Datenkapselung (Information Hiding)**
- Zugriff nur über Schnittstellen
- Direkter Zugriff auf Impl nicht möglich

**Client / Server Kommunikation**
- Server wartet permanent auf Anfragen
![[Pasted image 20250610121103.png|344x134]]

**Schichtarchitektur** Tba

**Dao (Data Access Object)-Layer**
 - Trennt Applikation von der Datenbank
 - Enthält Code für DB-Zugriff
 - Sorgt für saubereren Code

**Web Controller**
- Zuständig für Kommunikation zwischen Browser und Backend
- REST-API gängig

**Framework vs Library**
- Library: Sammlung von Funktionen und Klassen die Aufgaben lösen
- Framework: Halbfertiger Satz von Funktionalitäten mit grundlegender Struktur

**Inversion of Control**
- Traditionell: Code wird ausgeführt und führt Funktionen etc aus externen libs aus wenn er sie braucht
- IOC (Framework): Das Framework führt alles aus, die Kontrolle geht vom Developer auf das Framework über.
- Vorteil: Strukturierung, Standardisierung, Erweiterbarkeit

