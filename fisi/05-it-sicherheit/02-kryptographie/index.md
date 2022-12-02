---
title: Kryptographie

subtitle: Verschlüsselungsarten, Signaturen und Zertifikate

date: 2022-10-30T23:00:00+00:00

featured: false
draft: false
toc: true
reward: false
pinned: false
carousel: false
comment: false
author: Niclas Edge
tags: [IT-Sicherheit]
categories:
  - FISI
series:
  - FISI

images: [images/asymetrisch.png]
---

## Sicherheitsziele


![](Bildschirmfoto%202022-10-31%20um%2019.19.54.png)

### Verfügbarkeit

> Daten werden im Rahmen festgelegter Zeiten zur Verfügung gestellt

* Redundanz
  * Five Nine = 99,999%
  * Six Nine = 99,9999%
* ![](Bildschirmfoto%202022-10-31%20um%2019.01.17.png)

### Vertraulichkeit

> Daten können nur durch Befugte genutzt werden

* Verschlüsselung

### Integrität

> Keine Unbefugten Veränderungen

* Hashwert

### Authentizität

> Identität der Datenherkunft ist sichergestellt

* Digitale Signatur

### Verbindlichkeit

> Garantieren, dass die Daten zu einem Nutzer gehören

* Digitales Zertifikat

## Verschlüsselungsverfahren

> Sicherheitsziel: **Vertraulichkeit**
>
> * Symetrisch -> verschlüsselt Daten
> * Asymetrisch -> verschlüsselt wir ausschließlich Sysmetrische Schlüssel

### Symetrische Verschlüsselung

**Vorteile**:

* Schnelle Ver- und Entschlüsselung
* Geringe CPU-Last
* Einfache mathe. Methoden
  **Nachteile**:
* Schlüsselweitergabe
  ![](Bildschirmfoto%202022-10-31%20um%2019.09.31.png)

![](Bildschirmfoto%202022-10-31%20um%2019.15.43.png)
![](Bildschirmfoto%202022-10-31%20um%2019.16.05.png)

### Asymetrische Verschlüsselung

**Vorteile**:

* Sichere Schlüsselweitergabe
  **Nachteile**:
* Langsam, nicht für große Datenmengen

![](Bildschirmfoto%202022-10-31%20um%2019.20.16.png)

![](Bildschirmfoto%202022-10-31%20um%2019.16.27.png)

### Hybride Verschlüsselung

![](Bildschirmfoto%202022-10-31%20um%2020.21.47.png)

## Prüfsummen / Hashfunktion

> Sicherheitsziel: **Integrität**

* bei kleinster Änderung, soll sich der Haswert möglichst stark verändern
* Eine Rückführung von Hashwert zu Quelltext muss ausgeschlossen sein
* Es soll zu Verschiedenen Quelltexten nicht den gleichen haswert geben
	* Rainbow Tables: Kombination aus Datei+Hashwert in einer Datenbank
* Der Hashwert soll vom Empfänder schnell überprüft werden

![](Bildschirmfoto%202022-10-31%20um%2019.30.54.png)

![](Bildschirmfoto%202022-10-31%20um%2019.18.54.png)

![](Bildschirmfoto%202022-10-31%20um%2020.38.02.png)

## Digitale Signatur

> Sicherheitsziel: **Authentizität der nachricht + integrität des inhalts**

Sender:
1. hashwert aus klartext erzeugen
2. der hashwert mit privatem schlüssel des Senders  verschlüsselt
3. klartext + verschlüsselter hash = klartext mit signatur
Empfänger:
4. Das Digital signierte Dokument wird zum Empfänger gesendet
5. sigatur mit öffentlichem schlüssel des Senders entschlüsseln
6. vergleichen mit neu generiertem hash aus klartext
7. vergleich der beiden hash werte
8. wenn beide hash werte gleich, ist die signatur gültig und das dokument wurde nicht verändert

![](Bildschirmfoto%202022-10-31%20um%2019.34.06.png)
![](Bildschirmfoto%202022-10-31%20um%2019.33.53.png)

![](Bildschirmfoto%202022-10-31%20um%2019.19.11.png)

## PKI - Public Key Infrastructure

Authentizität der Schlüssel:
* PKI garantiert, dass der Schlüssel zu einem bestimmen User gehört und korrekt ist Sperrung von Schlüsseln:
* PKI kann einen public key Schlüssel sperren Verbindlichkeit:
* PKI garantiert, dass der Schlüssel zu einem bestimmen User gehört

![](Bildschirmfoto%202022-10-31%20um%2019.36.17.png)

### PKI Trustcenter

> Unabhängige Instanz zu Schafen, dem beide Parteien vertrauekn müssen

![](Bildschirmfoto%202022-10-31%20um%2019.45.41.png)

## Digitale Zertifikate

Inhalte eines Zertifikates:

* Aussteller (CA)
* Inhaber
* Gültigkeit
* Public Key (CA)
* Version
  ![](Bildschirmfoto%202022-10-31%20um%2019.41.33.png)

### Überprüfung eines Digitalen Zertifikates

1. Das digitale Zertifikat enthalt die Signatur der CA
2. Diese Signatur ist ein Hashwert uber das Zertifikat, welche mit dem privaten Key der CA verschlusselt wurde
3. Diesen Hashwert kann der Empfanger mit dem offentlcher Schlussel (im Zertifikat) der CA entschlüsseln
4. Der Empfanger bildet ebenfalls enen Hashwet und vergleicht diesen mit dem Ursprungs Hashwert
5. Sind beide gleich ist das Zertifikat oder der Text gultig bzw. unverandert.

![](Bildschirmfoto%202022-10-31%20um%2019.44.44.png)


## Vertrauensmodelle
### Direct Trust
### Web of Trust

### Hirachical Trust
