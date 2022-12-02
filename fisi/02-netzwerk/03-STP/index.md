---
title: "STP"
# list or single layouts are possible
layout: single-series # list, list-sidebar, single-series
show_post_thumbnail: true

publishDate: 2021-01-22
date: 2021-01-26
subtitle: "Spanning Tree Protocol"
description: |
  Spanning Tree Protocol
excerpt: 
author: Niclas Edge
show_post_thumbnail: true
show_author_byline: false
show_post_date: false
tags: [Netzwerk, Protokoll]
categories: [FiSi]
---
> Referenz: https://www.youtube.com/watch?v=CEP7uRkBaPI

> Was ist STP? 
> - Protokoll um Redundanzfaktor im Netzwerk zu implementieren

#### 1. Problem mit nicht redundater Verbindung
Wenn 2 switche direkt miteinander verbunden sind -> Single Point Of Failure

#### 2. Problem mit redungander Verbindung
- führen zu Duplizierten Frames
- Host muss vermehrte Frames verabeiten
- Netzwerkaufkommen überflutet
	- Broadcast -> Flooding

#### 3. Spanning Tree Protokoll verhindert Schleifen
- löst von schleifen im Netzwerk
- Blockiert nicht nötige Ports

### Versionen von Spanning Tree
- Plain STP (IEEE 801.1D)
- Rapid STP (IEEE 802.1W)
- Per VLAN STP (Cisco-Proprioetär)
- Rapid-Per-VLAN-STP ("PSVTS+")
- Multiple STP (IEEE 802.1s)

### Funktionsweise von Spanning Tree
- Spannbaum erzeugen, indem eine Wurzel ("root") bestimmt wird
-  Kürzester Pfad zur Root bridge finden
	- Kosten für den kürzesten Pfad bestimmen
- Port Rollen festlegen

### Komunikation bei STP: BPDUs
- erhalten eine Bridge ID
	- setzt sich zusammen aus:
		- Priorität
		- MAC-Adresse
		- Extended System ID
 
### Auswahl der Root Bridge
- Switch mit Nuedrigster Priorität / kleinste MAC-Adresse bei gleichstand

### Port-Rollen
- Root Port
	- der Port mit dem kürzesten Weg zur Root
- Designated
	- leiten den Verkeht weiter, aber kein Root Port
- Alternate
	- löst die Schleife auf, wenn ein Trunk an beiden Enden keine Root Port aufweist
