# 🚌 Farbcodiertes Echtzeit-Warnsystem für Bus- und Bahnanzeigen

**Farbcodiertes Echtzeit-Abfahrtssystem für BVG Berlin** – ein browserbasierter Prototyp von Christian Sysa.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-brightgreen)](https://cs15801.github.io/abfahrten-board/)
[![HTML](https://img.shields.io/badge/Built%20with-HTML%2FCSS%2FJS-orange)](https://github.com/CS15801/abfahrten-board)

---

## 🔗 Demo

**➡️ [Direkt ausprobieren: cs15801.github.io/abfahrten-board](https://cs15801.github.io/abfahrten-board/)**

Einfach den Link öffnen – keine Installation, kein Account, kein technisches Wissen nötig.

---

## 💡 Warum ich das gebaut habe

Als jemand, der regelmäßig öffentliche Verkehrsmittel nutzt, kenne ich das Problem: Man geht in Richtung Haltestelle und erkennt von Weitem, wenn überhaupt, ob die Zeitanzeige ein- oder zweistellig ist. Hat man nun 2 oder 8 Minuten? Diese Unwissenheit könnte durch ein Farbcodiertes Echtzeit-Warnsyste aus der Welt geschaffen werden.

Meine Idee war simpel: **Was wäre, wenn die Dringlichkeit sofort sichtbar wäre?** Nicht durch Zahlen, sondern durch Farbe. Das Board soll auf einen Blick zeigen, was gleich kommt – ohne dass man aktiv lesen oder nachdenken muss. Ein System, das für alle verständlich ist: für Pendler, Touristen und Menschen, die Abfahrtspläne sonst schwer lesen.

---

## ⚙️ Technische Komponente

Das Abfahrten-Board ist eine reine **Client-Side-Applikation** – es läuft komplett im Browser, ohne Server oder Backend.

| Technologie | Einsatz |
|---|---|
| **HTML / CSS / JavaScript** | Vollständige Umsetzung ohne Frameworks |
| **v6.bvg.transport.rest API** | Echtzeit-Abfahrtsdaten für Berlin/Brandenburg per Fetch-Request (Community-Projekt von Jannis R., basierend auf BVG-HAFAS) |
| **Intervall-Refresh** | Automatische Aktualisierung alle 30 Sekunden |
| **CSS-Variablen & Flexbox** | Responsives Layout für alle Bildschirmgrößen |


Die Abfahrtsdaten werden live von der öffentlichen Community-API `v6.bvg.transport.rest` abgerufen und direkt im Browser verarbeitet – keine Daten werden gespeichert oder weitergeleitet. Kein API-Schlüssel erforderlich.

---

## 🎨 Farbwahl & ihre Bedeutung

Die Farbcodierung folgt einem intuitiven Warnsystem, das auf **Barrierefreiheit und visuelle Unterscheidbarkeit** optimiert ist – nicht nur für normalsichtige Personen, sondern auch für Menschen mit Farbsehschwäche (Deuteranopie, Protanopie).

Die Farben wurden nach **WCAG 2.2** und der deutschen **BITV 2.0** ausgewählt:

| Status | Hintergrundfarbe | Schriftfarbe | Kontrast | Bedeutung |
|---|---|---|---|---|
| 🔴 **Kritisch** | `#CC0066` (Magenta-Rot) | `#FFFFFF` (Weiß) | **5,4:1 (AA)** | Abfahrt in **0–2 Minuten** oder **Ausfall** |
| 🟠 **Warnung** | `#FFAA00` (Amber) | `#000000` (Schwarz) | **11:1 (AAA)** | Abfahrt in **3–5 Minuten** oder **Verspätung** |
| ⚫ **Pünktlich** | `#0A0A0A` (Fast-Schwarz) | `#FFD700` (Gold) | **14:1 (AAA)** | Abfahrt in **mehr als 5 Minuten**, pünktlich |

### Warum diese Farben?

Das größte Problem klassischer Rot-Gelb-Grün-Systeme: **Rot-Grün-Schwäche** (Deuteranopie, Protanopie) betrifft ca. 8% aller Männer – für sie sind reines Rot und Orange kaum zu unterscheiden.

Die gewählte Farbpalette löst dies durch **unterschiedliche Leuchtkraft (Luminanz)** statt nur unterschiedliche Farbtöne:

- **Magenta-Rot (`#CC0066`)** enthält einen Blauanteil, der es von Amber klar trennt – auch für Protanopen erscheint es als helles Pink, nicht als Braun.
- **Amber (`#FFAA00`)** liegt im Gelbbereich, der einzige Farbton, den alle Typen von Farbblindheit zuverlässig wahrnehmen. Schwarz auf Amber übertrifft WCAG AAA deutlich.
- **Fast-Schwarz mit Gold (`#0A0A0A` / `#FFD700`)** ist das klassische Split-Flap-Design (Anzeigetafeln in Bahnhöfen). Hohe Lesbarkeit bei schlechten Lichtverhältnissen und auf Distanz.

Zusätzlich werden nach **WCAG 1.4.1** alle Statusinfos nicht nur durch Farbe, sondern auch durch eindeutige **Symbole und Textlabel** kommuniziert (⚠️ Kritisch, ⚠️ Warnung, ❌ Ausfall), sodass die Tafel auch in Graustufen und für Screenreader vollständig nutzbar bleibt.

**Das Ziel: Kognitive Last reduzieren.** Man soll nicht rechnen oder lesen müssen – die Farbe kommuniziert den Handlungsbedarf unmittelbar. Dieses Prinzip funktioniert sprachübergreifend und ist barrierefrei verständlich.

---

## 👤 Über den Autor

Erstellt von **Christian Sysa** – Fotograf & Medienstratege aus Köln.

Dieses Projekt ist ein persönlicher Prototyp im Rahmen meiner Auseinandersetzung mit nutzerfreundlicher Informationsdarstellung und browserbasierter Webentwicklung.

**Kontakt:**
- LinkedIn: [linkedin.com/in/christiansysa](https://linkedin.com/in/christiansysa)
- E-Mail: christian.sysa@web.de

---

## 📝 Lizenz & Urheberrecht

© 2026 Christian Sysa. Alle Rechte vorbehalten.

**Datenquelle:** [v6.bvg.transport.rest](https://v6.bvg.transport.rest/) – BVG Community-API (Open-Source, kein API-Schlüssel erforderlich)
