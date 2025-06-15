---
title: NSCS
draft: false
tags:
  - NSCS
  - security
  - matura
---
**CSMA/CA - Carrier Sense Multiple Access with Collision Avoidance**
- Zugriffsverfahren bei 802.11 Wlan
- Der Sender "Hört" den Kanal ab "Carrier Sense" und sendet erst wenn frei ist, außerdem wartet er eine Zufallszeit bevor er sendet
- Ziel: Gleichzeitiges senden verhindern anstatt kollissionen zu erkennen wie bei csma/cd (ethernet)


**DHCP - Dynamic Host Configuration Protocol**
- Server vergibt IP-Adressen automatisch an Geräte im Netzwerk (DHCP handshake)
	1. DHCP Discover (Client -> Broadcast)
	2. DHCP Offer (Server -> Client)
	3. DHCP Request (Client -> gewählten Server)
	4. DHCP Acknowledge (Server bestätigt Zuweisung)
- Wenn es mehrere DHCP Server gibt könnte ein Client mehrere Offers bekommen, das kann zu Inkonsistenz führen - etwa wie doppelten Adressvergaben, falsche Gateway Konfigurationen oder DNS Problemen. Deshalb pro Subnet nur einer!

**MAC Adresse**
- Schicht 2 (Sicherung)
- Eindeutige Hardware-Adresse, 48 Bit
- Nur Innerhalb eines LAN sichtbar


**IP Adresse**
- Schicht 3 (Netzwerk)
- Logische Adresse zur Identifikation im Netzwerk, 32 Bit
- Wird übers Internet verwendet


**VLAN - Virtual Local Area Network**
- Ermöglicht ein physisches Netzwerk in mehrere logische Netzwerke zu unterteilen
- Geräte in verschiedenen VLANs können sich nicht gegenseitig sehen auch wenn sie am selben Switch hängen.
- VLANS werden über switches konfiguriert (Layer 2 oder Layer 3)


**DMZ Demilitarized Zone**
- Ist ein Bereich zwischen dem internen Netzwerk und dem internet
- Meist Webserver, Mailserver, FTP-Server
- Ziel: Angreifer sollen nur bis zur DMS vordringen können, nicht ins interne LAN
- Umsetzung: Zwei Firewalls (Zwischen internet und dmz, zwischen dmz und internen lan)





