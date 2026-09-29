---
layout: page
title: Projektantrag Trashie (KI-gestützte Mülltrennungs-App)
permalink: /project-proposal/
---
Kerimcan Yagci, Nico Haider, Milan Nuzdic, Jan Brunner und Mario Solomun

*Schulprojekt im Rahmen des SYP-Unterrichts*

## 1. Ausgangslage

### 1.1 Ist-Situation
In Österreich ist die Abfallentsorgung auf Gemeindeebene organisiert. In Oberösterreich sind dafür die Gemeinden bzw. die jeweiligen Bezirksabfallverbände zuständig, in Linz übernimmt dies die Linz AG. Die Haushalte trennen ihren Abfall in mehrere Fraktionen, typischerweise Restmüll, Bioabfall, Altpapier, Leichtverpackungen (Gelbe Tonne bzw. Gelber Sack) sowie Altglas. Welche Fraktionen direkt beim Haushalt abgeholt und welche zu Sammelinseln gebracht werden, legt jede Gemeinde selbst fest.

Gegenstände, die nicht über die Haushaltstonnen entsorgt werden dürfen, etwa Elektroaltgeräte, Batterien, Problemstoffe, Sperrmüll oder Altholz, werden in Altstoffsammelzentren (ASZ) bzw. Recyclinghöfen abgegeben. Diese befinden sich an unterschiedlichen Standorten und haben jeweils eigene Öffnungszeiten.

Informationen zur richtigen Trennung erhalten Bürgerinnen und Bürger derzeit vor allem über:
- Abfallkalender und Trennblätter bzw. Trenn-ABCs der Gemeinden oder Abfallverbände (gedruckt oder als PDF)
- Webseiten der Gemeinden, Bezirksabfallverbände und Entsorgungsunternehmen
- regionale Abfall-Apps, die hauptsächlich Abholtermine und Erinnerungen anbieten
- Aufdrucke und Symbole auf Verpackungen
- persönliche Auskunft beim Personal der Altstoffsammelzentren

Die Zuordnung eines konkreten Gegenstandes erfolgt dabei durch die Person selbst, indem sie in diesen Quellen nachschlägt oder sich auf ihr bisheriges Wissen verlässt.



## 2. Problemstellung
Die korrekte Trennung von Abfall ist für viele Menschen im Alltag schwierig, da sich die Regeln je nach Gemeinde bzw. zuständigem Entsorgungsunternehmen unterscheiden. Das führt zu mehreren Problemen wie zum Beispiel:
- Unsicherheit, in welche Tonne oder zu welcher Recyclingstation ein Gegenstand gehört
- uneinheitliche Regeln zwischen einzelnen Gemeinden, z. B. innerhalb von Linz, dem restlichen Oberösterreich und dem Mühlviertel
- dadurch bedingte Fehlwürfe, die das Recycling erschweren und Wertstoffe verloren gehen lassen
- fehlendes zentrales, leicht zugängliches Nachschlagewerk für Privatpersonen
- besondere Unsicherheit bei Personen, die neu in eine Region ziehen oder diese nur vorübergehend nutzen (z. B. Studierende)



### 3. Nutzen

#### 3.1 App:

- **Foto-Analyse mittels KI**:
Der Nutzer fotografiert den Abfallgegenstand, ein eigens trainiertes KI-Modell klassifiziert Material bzw. Objektart.

- **Standorterkennung via GPS**:
Automatische Bestimmung von Gemeinde/Region, um die dort geltenden Trennregeln und das zuständige Entsorgungsunternehmen zu ermitteln.

- **Zuordnung zur richtigen Tonne/Recyclingstation**:
Verknüpfung von KI-Erkennung, Standort und hinterlegten lokalen Regeln zu einer konkreten Entsorgungsempfehlung.

- **Hinweis auf Recyclingstationen**:
Falls ein Gegenstand nicht über die normale Tonne entsorgt werden kann, zeigt die App die passende Sammelstelle an.

- **Manuelle Korrektur/Auswahl**:
Falls die KI unsicher ist oder keine Internetverbindung besteht, kann der Nutzer die Abfallart manuell auswählen.

## 4. Chancen und Risiken

### Risiken:
- Genauigkeit der KI-Erkennung könnte anfangs nicht ausreichen, wodurch Gegenstände falsch zugeordnet werden
- online recherchierte Standort- und Regeldaten könnten ungenau, unvollständig oder veraltet sein, da keine offizielle Kooperation mit Entsorgungsunternehmen besteht
- begrenzte Ressourcen, da kein Budget zur Verfügung steht und nur kostenlose/Open-Source-Werkzeuge genutzt werden können
- Zeitdruck im Rahmen des SYP-Unterrichts
- Koordination im fünfköpfigen Team
- unterschiedliches Verhalten der App auf verschiedenen Geräten/Betriebssystemen trotz Cross-Platform-Ansatz
- Datenschutz bei Standort- und Fotodaten

### Chancen:
- positive Umweltwirkung durch weniger Fehlwürfe und bessere Mülltrennung
- Sensibilisierung der Nutzer für Recycling und Nachhaltigkeit
- Skalierbarkeit auf weitere Regionen nach erfolgreicher Pilotphase in Linz, OÖ und Mühlviertel
- Lerneffekt im Team im Bereich KI/Computer Vision und Cross-Platform-Entwicklung
- kostengünstige Umsetzung durch konsequenten Einsatz kostenloser/Open-Source-Technologien


## 5. Rahmenbedingungen 

- Team aus 5 Personen.
- Zeitaufwand: Bis März 2028
- Frontend: C# mit MAUI
- Backend: Sprint Boot Java


---
*last change: 22.09.2026*

---
[← Übersicht]({{ '/' | relative_url }}) · [Management]({{ '/management/' | relative_url }}) · [Architektur]({{ '/architecture/' | relative_url }})
