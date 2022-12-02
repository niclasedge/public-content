---
title: "WLAN"

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

## TPC und DFS
### DFS
DFS - Dynamic Frequency Selection
- automatischer Kanalwechsel, falls auf dem verwendeten Kanal ein anderes Gerat erkannt wird
- Bei Betrieb muss DFS auf den Kanalen 52-64 und 100-140 benutzt werden
- 19 uberlappungsfrei Kanale in Deutschland

### TPC
TPC - Transmitter Power Controll
- Zweck von TPC:
	- Ist eine Regelung der Sendeleistung bei Funksystemen mit mobilen Teilnehmern. Ziel ist die Reduzierung von Funkstorungen und eine verlangerte Akkulaufzeit.
- Funktionsweise:
	- Es entscheidet anhand von vorgegebenen Schwellwerten ob es seine Sendeleistung verringern, erhohen oder beibehalten soll. Insbesondere wird nicht nur die Empfangsfeldstarke, sondern auch die Qualitat (z. B. Bitfehlerrate) berucksichtigt

## Strahlungsleistungen
- 5 GHz: Zwischen 25 mW und 4000 mW je nach Frequenzband.
- In Europa ist TPC/DFS fur den Betrieb von WLANs vorgeschrieben. 
	- Ohne DFS und TPC sind nur 200 mW und ein eingeschranktes Frequenzband in Kanal-Bandbreite 20 MHz / Kanalabstand 20 MHz Deutschland zugelassen. GHz Bereich

## Vor- & Nachteile 5GHz
- Vorteile:
	- deutlich hohere Ubertragungsrate möglich
	- weniger genutztes Frequenzband, dadurch haufig strungsarmerer Betrieb möglich
	- in Deutschland sind keine uberlappende Kanale erlaubt 
	- höhere Reichweite, da mit 802.11h bis zu 1000 mW Sendeleistung moglich ist das überkompensiert die groere Dampfung der hoheren Frequenzen
- Nachteile:
	- starkere Regulierungen in Europa: auf den meisten Kanalen DFS notig; auf einigen Kanalen kein Betrieb im Freien erlaubt; falls kein TPC benutzt wird, muss die Sendeleistung reduziert werden
	- Ad-hoc-Modus wird von den meisten Geraten nicht unterstutzt
	- Signal wird von Wanden schnell abgeschirmt

## MIMO 
![](Bildschirmfoto%202022-11-12%20um%2016.17.26.png)

## MASH
> Ein WLAN-Mesh ist ein flachendeckendes WLAN, bei dem sich merere Access Points untereinander per WLAN verbinden.

- Vorteile:
	- Nur ein Mesh-Accesspoint benotigt LAN Verbindung.
	- Mesh-Points benotigen nur eine Stromversorgung (POE)
	- Einfaches Roaming, da Clients immer zur besten Funkzelle wechselt (bei AP wechselt der Client erst, wenn die WLAN Verbindung abbricht).
	- Im gesamten Mesh kann mit einer SSID gearbeitet werden.
	- Bei mehreren Mesh-Zellen wird immer der optimale Weg gesucht.
	- In Mesh-Netzen ist die Ubertragungsrate meist hoher, da für die Kommunikation mit Clients und anderen Mesh-Points unterschiedliche Frequenzen (oder LAN-Verabelug) verwendet werden.
