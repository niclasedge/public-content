---
title: "Routing"

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

## Statisches Routing

### 3 Schitte des Routings

#### Schritt 1 - Addressierung laut Regelsatz

> Regelsatz Addressierung:
>
> - Client-Addressen werden von der niedrigstmöglichen Host-Adresse an aufwärts vergeben
> - Router Adressen werden von der höchstmöglichen Host-Adresse an abwärts vergbeben
> - Der Router, hinter dem sich die meisten Ziele befinden, bekommt die höchste Adresse im jeweilgen Subnetz

[![](image-1664301359889.jpeg)](image-1664301359889.jpeg)

#### Schritt 2 - Ergänzung der IP-Addressen durch Subnetting

[![](image-1664301715434-01-26.png)](image-1664301715434-01-26.png)

#### Schritt 3 - Erstellung der Routingtabelle

[![](image-1664302198399-09-51.png)](image-1664302198399-09-51.png)

[![Bildschirmfoto 2022-10-13 um 09.56.28.png](bildschirmfoto-2022-10-13-um-09-56-28.png)](bildschirmfoto-2022-10-13-um-09-56-28.png)

## Dynamische Routingprotokolle
> Beim dynamischen Routing tauschen die Router untreinander die Routinginformationn aus und beeche daraus die Routingtabellen. Beim Ausfall einer Route kann durch das Routingprotokoll eine Ersatzroute automatisch eingesetzt werden.


### RIP & OSPF
![](Bildschirmfoto%202022-11-12%20um%2016.09.23.png)



## IHK Fragen zu Routing

- Erstellen Sie eine Routing Tabelle
- finden Sie den Fehler in einer vorhandenen Routing Tabelle
- Tabelle ergänzen
