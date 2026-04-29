# 🚌 Abfahrten-Board

**Farbcodiertes Echtzeit-Abfahrtssystem für den Kölner ÖPNV** – ein browserbasierter Prototyp von Christian Sysa.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-brightgreen)](https://cs15801.github.io/abfahrten-board/)
[![HTML](https://img.shields.io/badge/Built%20with-HTML%2FCSS%2FJS-orange)](https://github.com/CS15801/abfahrten-board)

---

## 🔗 Demo

**➡️ [Direkt ausprobieren: cs15801.github.io/abfahrten-board](https://cs15801.github.io/abfahrten-board/)**

Einfach den Link öffnen – keine Installation, kein Account, kein technisches Wissen nötig.

---

## 💡 Warum ich das gebaut habe

Als jemand, der täglich den Kölner ÖPNV nutzt, kenne ich das Problem: Man steht an der Haltestelle, schaut auf eine lange Liste von Abfahrten – und muss dann erst suchen, welche Linie tatsächlich bald kommt. Die klassische Anzeigetafel listet alles chronologisch auf, aber das Auge muss jedes Mal neu scannen.

Meine Idee war simpel: **Was wäre, wenn die Dringlichkeit sofort sichtbar wäre?** Nicht durch Zahlen, sondern durch Farbe. Das Board soll auf einen Blick zeigen, was gleich kommt – ohne dass man aktiv lesen oder nachdenken muss. Ein System, das für alle verständlich ist: für Pendler, Touristen und Menschen, die Abfahrtspläne sonst schwer lesen.

---

## ⚙️ Technische Komponente

Das Abfahrten-Board ist eine reine **Client-Side-Applikation** – es läuft komplett im Browser, ohne Server oder Backend.

| Technologie | Einsatz |
|---|---|
| **HTML / CSS / JavaScript** | Vollständige Umsetzung ohne Frameworks |
| **KVB / VRS API** | Echtzeit-Abfahrtsdaten per Fetch-Request |
| **Intervall-Refresh** | Automatische Aktualisierung alle 30 Sekunden |
| **CSS-Variablen & Flexbox** | Responsives Layout für alle Bildschirmgrößen |
| **GitHub Pages** | Kostenloses Hosting direkt aus dem Repository |

Die Abfahrtsdaten werden live von der öffentlichen API des Kölner Verkehrsverbunds abgerufen und direkt im Browser verarbeitet – keine Daten werden gespeichert oder weitergeleitet.

---

## 🎨 Farbwahl & ihre Bedeutung

Die Farbcodierung folgt einem intuitiven Ampelprinzip – angelehnt an universelle Warnsysteme, die jeder kennt:

| Farbe | Bedeutung | Abfahrt in |
|---|---|---|
| 🔴 **Rot** | Sofort – jetzt losrennen! | 0–2 Minuten |
| 🟠 **Orange** | Bald – zügig zur Haltestelle | 3–5 Minuten |
| 🟡 **Gelb** | Noch Zeit – kein Stress | 6–10 Minuten |
| 🟢 **Grün** | Entspannt – Zeit zum Warten | 11+ Minuten |

Das Ziel: **Kognitive Last reduzieren.** Man soll nicht rechnen oder lesen müssen – die Farbe kommuniziert den Handlungsbedarf unmittelbar. Rot bedeutet überall Dringlichkeit, Grün bedeutet Ruhe. Dieses Prinzip funktioniert sprachübergreifend und ist barrierefrei verständlich.

---

## 👤 Über den Autor

Erstellt von **Christian Sysa** – Fotograf, Medienstratege und Gründer von [Sysa Media](https://synamedia.de).

Dieses Projekt ist ein persönlicher Prototyp im Rahmen meiner Auseinandersetzung mit nutzerfreundlicher Informationsdarstellung und browserbasierter Webentwicklung.
