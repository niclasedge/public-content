---
title: "VPN & IPSec"


publishDate: 2021-01-22

description: |
  Virtual Private Network

featured: false
draft: false
toc: true
reward: false
pinned: false
carousel: false
comment: false

author: Niclas Edge
tags: [netzwerk]
categories:
  - FISI
series:
  - FISI
---

## Pro & Contra
- Vorteil
	- Kostengünstig
	- Sicher
	- Flexibel
- Nachteil
	- Abhängigkeit von der Verfügbarkeit anderer Netzwerke
	- Performance
	- Aufwand zu Erhaltung der Sicherheit

## End-to-Site
![](Bildschirmfoto%202022-11-15%20um%2020.19.57.png)

## Site-to-Site
![](Bildschirmfoto%202022-11-15%20um%2020.20.16.png)

## End-to-End
![](Bildschirmfoto%202022-11-15%20um%2020.20.35.png)

## VPN Alternativen

- Dark Fiber
	- ![](Bildschirmfoto%202022-11-15%20um%2019.57.21.png)
- MPLS (Multi Protocol Label Switching)
	- ![](Bildschirmfoto%202022-11-15%20um%2019.57.03.png)

## VPN Protokolle
> L2TP + IPsec kann zusammen betrieben werden umm alle vorteile der beiden Protokolle zu nutzen

![](Bildschirmfoto%202022-11-15%20um%2020.21.39.png)

### IPsec

- IP Sec IP Security*
- Entwickelt in 1998 von der
- IETF (Internet Engineering Task Force)
- Ursprünglich für IPv6
- Sicherheitsarchitektur für IP - Netze
- Arbeitet auf OSI - Layer 3
- Gewährleistet Vertraulichkeit und Integrität

#### Authentifizierung
- PSK (Pre Shared Key) -> veraltet
- IKEv2 (Internet Key Exchange Protocol)
	- Diffie-Hellmann-Verfahren (Verwendung von X.509 Zertifikaten)
	- UDP Port 500
#### Sicherheit
- AH - Authentication Header
	- Datenintegrität
	- Datenauthenzität
	- Keine Verschlüsselung![](Bildschirmfoto%202022-11-15%20um%2020.40.48.png)
- ESP - Encapsulating Security Payload
	- Funktionalität des AH - Protokolls
	- Verschlüsselung der Pakete (z.B. AES,...)
	- ![](Bildschirmfoto%202022-11-15%20um%2020.41.07.png)
### Transport und Tunnelmodus

![](Bildschirmfoto%202022-11-15%20um%2020.27.11.png)


## IKEv2
> Authentifizierungsmethode für IPsec

![](Bildschirmfoto%202022-11-15%20um%2020.45.53.png)
![](Bildschirmfoto%202022-11-15%20um%2020.46.12.png)![](Bildschirmfoto%202022-11-15%20um%2020.46.32.png)