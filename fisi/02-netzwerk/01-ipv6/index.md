---
title: 'IPv6'

date: 2021-01-02

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
## IPv6 Aufbau
- 128 Bit  
- ≈ 340 Sextillionen Adressen - Hexadezimal Notation  
- Trennzeichen :  
- 8 x 4 Hexadezimale Stellen
- 1 Nabble = 4 Bit = 1 Hex Zahl

## IPv6 Netzgrößen für Geschäftskunden /48
![](Bildschirmfoto%202022-11-10%20um%2009.58.18.png)

## IPv6 Netzgröße für Privatkunden / 56 - 64
![](Bildschirmfoto%202022-11-10%20um%2009.59.06.png)

## IPv6 Adress Typen
![](Bildschirmfoto%202022-11-10%20um%2009.59.36.png)



## Bestimmung der Präfixadresse IPv6:
3 Schwierigkeitsstufen

### Schwierigkeitsstufe 1
- wenn präfix glatt durch 16 teilbar  (48/)

1. präfixgrenze nach dem 48. bit einzeichnen
![](Bildschirmfoto%202022-11-16%20um%2018.37.25.png)
2. wert hinter präfix auf 0 setzen
3. verkürzen
![](Bildschirmfoto%202022-11-16%20um%2018.39.03.png)
- erste IP präfixadresse / netz id


### Schwierigkeitsstufe 2
- wenn präfix nicht duch 16 teilbar
- aber glatt durch 4 teilbar

1. verkürzte 0 einschreiben
2. grenze einzeichnen
![](Bildschirmfoto%202022-11-16%20um%2018.39.43.png)
3. nachführende 0 mit angeben, falls vorhanden
4. mit 0 auffüllen
![](Bildschirmfoto%202022-11-16%20um%2018.40.05.png)

### Schwierigkeitsstufe 3
- muss innerhalb eines nibbles geteilt werden

## Unicast Typen
### Link Local Unicast 
fe80 - febf /10
### Unique Local Unicast (wie private ipv4)
fc - fd /7
### Global Unicast
2:: - 3::

## Multicast Typen
ff00::/10

![](Bildschirmfoto%202022-11-16%20um%2019.35.06.png)

## Anycast Adresse
- sucht den Server mit wen wenigsten hops zum ziel

# Aufbau eines IPv6 Suffix
> der hintere 64 bit Teil der Adresse
## SLAAC
> erstellung der Adresse anhand einer von 3 Methoden

- **EUI-64-Format**: Hier wird die Interface-ID mit Hilfe der MAC-Adresse gebildet.
- **Privacy Extensions**: Diese Methode erstellt eine garantiert eindeutige Interface-ID, die keine Rückschlüsse auf die MAC-Adresse des Knotens zulässt.
- **Random Identifier**: Windows-Systeme erstellen einmalig eine zufällige Interface-ID.

### EUI64 convertierung
![](Bildschirmfoto%202022-11-16%20um%2020.22.14.png)
