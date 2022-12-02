---
title: "SNMP"


date: 2021-01-26

featured: false
draft: false
toc: true
reward: false
pinned: false
carousel: false
comment: false

description:
author: Niclas Edge
tags: [netzwerk]
categories:
  - FISI
series:
  - FISI
---

> Protokoll zum überwachen des Netzwerkes


### Was ist SNMP
- Überwachung von Netzwerkgeräten  
- Osi-Schichten 5-7  
- UDP  
- 3 Komponenten (verwaltete Geräte – Agenten – NMS) • Sammlung von Daten in einer Datenbank
- MIB I + II (Managment Information Base) • Bei Bedarf Abruf der MIBs vom NMS
-   Beispiele: Datenpakete eines Routers
	-   oder Füllstand einer Festplatte
-   Weltweite Identifizierung OID (Objekt Identifier) Alphanumerisch oder Numerisch
	-   Beispiel Cisco: 1.3.6.1.4.1.9
-   Port 161 + 162 
	-   Abruf bei Bedarf über 161 UDP
	-   Bei Fehlermeldungen sofort über 162 TCP

### SNMP Befehle
- GET/RESPONSE  
	- Dabei fragt das Management System den Client aktiv ab. Dies ist eine einmalige Abfrage. Will eine Management Software daher eine Grafik der Netzwerkbelastung aufbauen, dann muss Sie regelmäßig die Variable auslesen, in der die Anzahl der übertragenen Bytes stehen. (Polling)
- SET  
	- Wenn ihre Management Anwendung sich am SNMP-Dienst korrekt autorisieren kann, dann ist es auch möglich, Parameter zu schreiben, z.B.: einen Port zu deaktivieren etc.
- TRAP  
	- Zuletzt muss eine Management Station nicht permanent ein Gerät abfragen. Das Gerät kann auch einen "TRAP" an eine andere Station senden, um dringende Dinge zu melden, z.B.: Anmeldung mit falschem Kennwort oder ein verlorener Link

- WALK (Bulk ab SNMPv2) 
	- Mehrere Get-Anfragen an ein Objekt