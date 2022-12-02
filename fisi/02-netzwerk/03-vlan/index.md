---
title: VLAN


date: 2022-11-10

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
images: [images/vlan.png]
---

> Logische Netzwerke auf Layer 1-4

### Arbeitsweise:
- Ports werden VLANS zugeordnet
- MAC Adresse wird VLAN Zugeordnet
- IP wird VLAN zugeordnet

### Optionen der Zuordnung
- Trunks
- Tagging


### Regel
- Rahmen, die auf Port aus VLAN x eingehen, werden nur auf Ports augsgeben,m wie zu VLAN x gehören




## Was ist ein VLAN

## Vorteile von VLANs
- logische Netztrennung
- bessere Lastenverteilung (Trennung von Broadcast-Domäne)
- Flexibilität, da Gruppenzugehörigkeit einfach und schnell geändert werden kann
- Erhöhte sicherheit der Gruppen
- Datenverkehrpriorisierung (QoS)
- weniger Hardware benötigt
- geringerer Energiebedarf
- flexibel

## Wie erstellt man ein VLAN?

## Welche VLAN Typen
### Statische vs Dynamische VLANs
![](Bildschirmfoto%202022-11-15%20um%2018.25.17.png)

### OSI Layer 1 - portzentisches VLAN
![](Bildschirmfoto%202022-11-15%20um%2018.25.58.png)
### OSI Layer 2 MAC - basierendes VLAN
![](Bildschirmfoto%202022-11-15%20um%2018.27.10.png)
### Osi Layer 3/4 - IP / UDP / TCP - basierendes VLAN
![](Bildschirmfoto%202022-11-15%20um%2018.27.51.png)

## Switchübergreifende Kimmunikation

### Implizite Markierung (kein TAG)
- beispiel: IP-Adresse, MAC-Adresse, Port

### Explizite Markierung (mit TAG)
- beispiel: Tagging nach IEEE 802.1Q (Institute of Electrical and Electronics Engineers)

## Was ist ein VLAN-Trunk
![](Bildschirmfoto%202022-11-15%20um%2018.32.52.png)


## Wie ist ein VLAN-Tag aufgebaut
![](Bildschirmfoto%202022-11-15%20um%2018.45.03.png)
