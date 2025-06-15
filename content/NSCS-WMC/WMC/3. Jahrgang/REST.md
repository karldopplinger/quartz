#wmc #matura #Rest


**REST**
- Architekturstil für Web-APIs
- Ziel: Einheitliche Schnittstelle über die Clients mit Servern über HTTP kommunizieren
- Fast immer mit HTTP + JSON umgesetzt
- Wichtig:
	- Zustandslosigkeit (Stateless): Server merkt sich nichts über den Client zwischen zwei Anfragen; Jeder Request muss alle Infos enthalten (z.B Session Token); Einfach Skalierbar
	- Client-Server-Trennung: Der Client und der Server sind unabhängig


**HTTP Methoden**
	Wichtig
- GET: Lädt eine Ressource
- POST: Sendet Daten
- PUT: Hochladen einer Datei auf eine URL
- DELETE: Löscht eine Ressource
	Nicht Wichtig
- HEAD: Wie 'GET', liefert aber nur HTTP-Header
- TRACE: Gibt Anfrage wie vom Server empfangen
- OPTIONS: Liste von Optionen von Server


**Uniform Resource Identifier (URI)**

> Die URI ist eine Zeichenfolge und dient der eindeutigen Identifikation einer Ressource

**GET-Anfrage**
```
GET <URL> <Parameter> |HTTP Version|
```

**HTTP Statuscodes**
- 1xx - Informationen
- 2xx - Erfolgreiche Operation
- 3xx - Umleitung
- 4xx - Client-Fehler
- 5xx - Server-Fehler

**Representational State Transfer (REST)**
- Ziel: Einheitliche Schnittstelle
- Zustandslosigkeit (Jede Anfrage in sich geschlossen)