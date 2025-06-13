# 📘 Maturavorbereitung – NSCS & WMC

---

## 📡 NSCS – Netzwerksysteme und Cybersicherheit

---

### 1. Netzwerktechnologie und Netzwerkdienste

#### 1.1 Grundbegriffe Netzwerktechnik
- Netzwerkkarte
	- 
- CAT-Kabel
- RJ45-Stecker
- Access Point
- Switch / Hub / Router

#### 1.2 ISO/OSI-Modell
- Überblick der 7 Schichten
- Zuordnung realer Protokolle

#### 1.3 Netzwerktopologien
- Stern
	- Zentral ein Hub/Switch, führt von dort aus zu jedem Gerät
	- + Einfach zu erweitern, Einfach zu debuggen, gute Organisation
	- - Single Point of Failure (Fällt das Zentrale Gerät aus - Problem)
- Ring
	- Daten laufen im Kreis von PC-PC, jeder PC hat genau 2 Nachbarn.
	- + Schneller Durchsatz, Geräte sind gleichberechtigt
	- - Wenn ein Gerät o. Kabel ausfällt ist der Ring unterbrochen, Fehlersuche schwierig
- Bus
	- Geräte sind hintereinandergebunden, An den Enden gibt es 2 Abschlusswiderstände
	- + Einfach & Billig aufzubauen, Gut für kleine Netzwerke
	- - Begrenzte Länge & Teilnehmer, Datenkolission möglich
- Vermascht
	- Vollvermascht
		- Jeder Knoten ist mit jedem direkt verbunden
		- + Maximale Redundanz
		- - Viel Aufwand
	- Teilvermascht
		- Wichtige Verbindungen sind mehrfach vorhanden
		- ~ Kompromiss aus Sicherheit & Aufwand

#### 1.4 Netzwerkpakete
- Aufbau
- Header
- Inhalt
- Checksummen

#### 1.5 TCP/IP
- Schichtenmodell (Links OSI, Rechts TCP/IP)
 ![[Pasted image 20250604152536.png|362x243]]
- Vergleich mit OSI
	- OSI ist viel detaillierter während TCP/IP die einzelnen Grenzen nicht so streng nimmt und eher übergreifend gestaltet.
	- In der Praxis wird TCP/IP verwendet, für den Aufbau von Netzwerken und der Theorie OSI
- IP-Adressen...
	- identifizieren Geräte eindeutig
	- sind auf Layer 3 (Network Layer) angesiedelt
	- ermöglichen die Kommunikation über verschiedene Netzwerke
- TCP/UDP
	- Transmission Control Protocol (Verbindungsorientiert)
		- TCP sorgt dafür, dass Pakete ankommen, unzwar in der richtigen Reihenfolge
		- Gehen Pakete verloren werden diese erneut versendet
	- User Datagram Protocol (Verbindungslos)
		- Kein Verbindungsaufbau -> Daten werden einfach abgeschickt
		- Daten können teilweise nicht ankommen oder in der falschen Reihenfolge vorliegen
- Ports
	- Nummerische Adressen, 16 Bit, 0-65535
	- Helfen dabei Daten in einem Gerät an die Richtige Applikation weiterzuleiten
	- Unterteilung in Well-Known, Registered und Dynamic Ports
	- Man braucht sie damit mehrere Applikationen gleichzeitig über das Netzwerk kommunizieren können

#### 1.6 Ethernet
- Topologie
	- 
- CSMA/CD
- Halb-/Vollduplex
- Kabellängen
- Dämpfung
- Komponenten: Hub/Switch/Router

#### 1.7 WLAN
- CSMA/CA
- Unterschiede zu LAN
- Frequenzen
- Radiowellen
- Sniffing
- Verschlüsselung

#### 1.8 Ausfallssicherheit
- Redundanz
- Replikation
- USV

#### 1.9 Protokolle
- Was ist ein Protokoll?
- Wichtige Protokolle

#### 1.10 Verzeichnisdienste & Zugriffskontrolle
- Verzeichnisdienste
- Gruppen
- Zugriffskontrollmatrix

#### 1.11 Multithreading

#### 1.12 Codeversionierung und CI
- Git
- Continuous Integration

---

### 2. Netzwerkplanung und Netzwerkmanagement

#### 2.1 Subnetze

#### 2.2 DHCP - Dynamic Host Control Protocol
- Ein Netzwerkprotokoll durch das Geräte im Netzwerk automatisch eine IP zugewiesen bekommen
- Ohne DHCP müsste jede IP manuell zugewiesen werden
- Verteilt: IP, Subnetzmaske, Gateway (Router Adresse), DNS Server Adresse, optional weiteres
- Funktion:
	- Gerät kommt ins Netzwerk und sendet eine Anfrage (DHCP Discover)
	- DHCP Server antwortet mit einer IP-Adresse (DHCP Offer)
	- Gerät bestätigt die Adresse mit (DHCP Request)
	- Server bestätigt mit (DHCP Acknowledge)
	- Gerät nutzt diese Adresse für eine bestimmte Zeit (Lease-Time)


#### 2.3 DNS - Domain Name System

#### 2.4 NAT - Network Adress Translation
- Mehrere Geräte können über eine einzige öffentliche Adresse ins Internet.
- z.B im Netzwerk gibt es 192.168.0.1-x.x.x.255, die gehen alle über 86.71.98.20 oderso ins netz, somit werden Adressen gespart.
- Theoretisch nichtmehr notwendig bei IPv6 wegen der hohen Adressbereiche

#### 2.5 IPv6
- IPv4 Adressen unterscheiden sich von IPv6 Adressen in:
	- Addressgröße (32vs128 Bit)
	- d.e Adressanzahl (4,3 Milliarden vs 340 Sextillionen)
	- Darstellung - Ipv4 wird Dezimal dargestellt, ipv6 in hex (192.168.0.1 vs 2001:0db8:85a3::8a2e:0370:7334)

#### 2.6 Rechenzentrum / Serverraum

#### 2.7 Single Point of Failure / Redundanz
- Der "SPOF" beschreibt eine Komponente eines Systems deren Ausfall das gesamte Systm lahmlegen oder stark beeinträchtigen kann.
- Bsp:
	- Ein einziger Router für die Firma -> Ausfall -> Keiner hat mehr Internet
	- Nur ein DB Server für alle Kunden -> Er fällt aus -> Websiten und Apps können nichtmehr darauf zugreifen
- Bei der Redundanz geht es darum diese Kernkomponenten (Deren Ausfall starken Einfluss auf den weiteren Verlauf hätte) abzusichern, beispielsweise durch Server Cluster, einer Batterie für das Gebäude bei Stromausfall oder ähnlichem

#### 2.8 Fehlertoleranz

#### 2.9 Monitoring
- Beim Monitoring geht es darum Anwendungen, Systeme, Ressourcen etc. zu überwachen um frühzeitig Probleme oder Mängel zu erkennen und Fehler oder Engpässe bestmöglich zu vermeiden oder zu beheben.
- Wird unterteilt in bspw:
	- System-Monitoring: Zustand von Geräten, Servern, Betriebssystemen
	- Netzwerk-Monitoring: Überwachung von Verbindungen und Datenverkehr
	- Security-Monitoring: Angriffsversuche, anomalien

---

### 3. Netzwerk- und Systemsicherheit

#### 3.1 Einführung in Security
- Herausforderungen
- Risiko
- Schutzziele
- Angriffe
- Angriffsphasen
- Grundbegriffe

#### 3.2 Netzwerksicherheit
- 

#### 3.3 SSL/TLS / HTTPS / SSH / VPN

#### 3.4 Intrusion Detection

#### 3.5 Authentifizierung
- Hashes & Signaturen
- PKI
- Zertifikate
- SSL

#### 3.6 Firewalls

#### 3.7 Virtualisierung
- VM vs. Container
- Sicherheitsvorteile
- Container & Cloud
- Kubernetes

---

## 🌍 WMC – Web- und Mobilcomputing

---

### 4. Architektur verteilter Systeme

#### 4.1 PWA – Progressive Web Apps
- Kennzeichen
- Web APIs
- Service Worker
- Offlinefähigkeit

#### 4.2 Pushnachrichten via HTTP
- Technologische Basis
- Ablauf
- Problem mit HTTP 1.1

#### 4.3 Verteilte Systeme (Foliensatz)

#### 4.4 REST (Foliensatz)

#### 4.5 Softwarearchitekturen
- Definition
- Monolithisch
- 2-tier / 3-tier

#### 4.6 Plattformproblematik PWA
- Desktop vs. Mobil
- Responsiveness
- Android vs. iOS
- App Manifest

---

### 5. Technologien für verteilte Systeme

#### 5.1 Kommunikation & Serialisierung
- Foliensätze
- Interoperabilität

#### 5.2 Motivation für Tests
- Manuell vs. Automatisiert
- Testarten

#### 5.3 Buildprozess
- Build Management Tools
- Qualitätsprüfungen

#### 5.4 HTTP + Sessions + JWT

#### 5.5 Frameworks / Middleware
- Logging
- ORM
- Dependency Injection

---

### 6. Entwicklung von Web- und Mobilapplikationen

#### 6.1 Sicheres Programmieren

#### 6.2 Sicheres Testen

#### 6.3 Usability

#### 6.4 HTML5 & Web APIs
- Native App vs. HTML5
- Native App vs. PWA

#### 6.5 Web Basics
- HTML
- CSS
- JavaScript
- Responsive Web Design

#### 6.6 Cookies & HTML5 Web Storage

#### 6.7 Spring Security

---
