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



## 3. Nutzen


- **Foto-Analyse mittels KI**:
Der Nutzer fotografiert den Abfallgegenstand, ein eigens trainiertes KI-Modell klassifiziert Material bzw. Objektart.

- **Standorterkennung via GPS**:
Automatische Bestimmung von Gemeinde/Region, um die dort geltenden Trennregeln und das zuständige Entsorgungsunternehmen zu ermitteln.

- **Zuordnung zur richtigen Tonne/Recyclingstation**:
Verknüpfung von KI-Erkennung, Standort und hinterlegten lokalen Regeln zu einer konkreten Entsorgungsempfehlung.

- **Hinweis auf Recyclingstationen**:
Falls ein Gegenstand nicht über die normale Tonne entsorgt werden kann, zeigt die App die passende Sammelstelle an.

- **Zentralles Nachschlagewerk**:
Hier findest du jederzeit schnell, was in welche Tonne gehört, auch ohne Internetverbindung.

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


## 6. Plannung

- Start des Projektes: Anfang 4 Jahrgang.
- Ende des Projektes: März 2028.
- Erster Prototyp: März 2027.

### 6.1 Meilensteine

1. Schreiben des Manifests (Mitte/Ende Oktober 2026).
2. Sammeln der Daten für das KI-Modell (Ende November 2026).
3. Sammeln der Abfalldaten und Gemeinderegeln (Ende November 2026).
4. Aussuchen des basis KI-Modells (Anfang/Mitte Dezember 2026).
5. Frontend und Backend implementierung (Anfang Jänner 2027).
6. Erster Prototyp (Anfang März 2027).
7. Ausweitung des Projektes in Zusammenarbeit mit den ASZs (Anfang September 2027).
8. Fertigstellung der ASZ funktion (Ende Dezember 2027).
9. Fertigstellung des Projektes (Mitte/Ende Februar 2028).


## Einschränkungen

### Rechtliche Einschränkungen

- **Datenschutz (DSGVO / DSG)**:
Standortdaten und Fotos sind personenbezogene Daten. Fotos können Personen, Adressetiketten oder Kfz-Kennzeichen zeigen und enthalten EXIF-Metadaten mit GPS-Position. Die Nutzung erfordert eine Einwilligung, Datenminimierung (Koordinaten nur in Gemeinde umwandeln, nicht speichern) und eine Datenschutzerklärung, die auch von den App Stores verlangt wird. Die KI-Klassifikation sollte daher möglichst direkt am Gerät erfolgen.

- **Urheberrecht bei Trainingsdaten**:
Bilder aus dem Internet dürfen nicht ohne Weiteres zum Training verwendet werden. Öffentliche Datensätze (z. B. TrashNet, TACO) sind nur unter ihrer jeweiligen Lizenz nutzbar. Auf eigenen Fotos dürfen keine erkennbaren Personen abgebildet sein (Recht am eigenen Bild).

- **Lizenzen von Basismodell und Bibliotheken**:
Das gewählte Basismodell und alle Bibliotheken müssen lizenzrechtlich passen, z. B. verpflichtet die AGPL-3.0 (Ultralytics YOLO) zur Offenlegung des eigenen Codes, während Modelle unter Apache 2.0 (MobileNet, EfficientNet) unproblematischer sind.

- **Übernahme von Regel- und Standortdaten**:
Trennregeln als Fakten sind nicht geschützt, Texte, Grafiken und Icons aus Trenn-ABCs der Gemeinden bzw. der Linz AG jedoch schon. Eine systematische Übernahme ganzer Datenbanken kann das Datenbankschutzrecht verletzen. Bevorzugt werden offene Quellen wie data.gv.at oder OpenStreetMap unter Einhaltung ihrer Lizenzbedingungen (Namensnennung).

- **Haftung**:
Falsche Empfehlungen können Schäden verursachen (z. B. Brand durch Lithium-Akkus im Restmüll). Die App benötigt daher einen Hinweis, dass die Angaben ohne Gewähr sind und im Zweifel die Auskunft der Gemeinde bzw. des ASZ gilt. Die App darf nicht den Eindruck einer offiziellen App der Entsorgungsunternehmen erwecken (keine fremden Logos).

- **Sonstiges**:
Prüfung des Namens „Trashie“ auf bestehende Marken, Impressums- bzw. Offenlegungspflicht bei Veröffentlichung, Volljährigkeit als Voraussetzung für App-Store-Entwicklerkonten sowie Klärung der Rechte am Code, insbesondere bei einer Zusammenarbeit mit den ASZs.

### Fachliche und technische Einschränkungen

- **Sich ändernde Regeln**:
Seit 1.1.2025 gilt in Österreich das Einwegpfand, außerdem werden Metallverpackungen gemeinsam mit Leichtverpackungen gesammelt. Solche Änderungen müssen laufend in die Regel-Datenbank übernommen werden.

- **Grenzen der KI-Erkennung**:
Ein Foto zeigt das Objekt, aber nicht immer das Material (z. B. Verbundstoffe wie Tetra Pak, Kunststoffart, Verschmutzung). Die Anzahl der erkennbaren Klassen ist begrenzt, Licht und Hintergrund beeinflussen die Genauigkeit.

- **Regionale Einschränkung**:
Die App funktioniert nur in der Pilotregion Linz, Oberösterreich und Mühlviertel. GPS ist in Gebäuden und an Gemeindegrenzen ungenau.

- **Kosten trotz fehlendem Budget**:
Für die Veröffentlichung fallen Gebühren an (Apple Developer Program 99 USD/Jahr, Google Play einmalig 25 USD). iOS-Builds erfordern einen Mac, das Backend benötigt Hosting und für das KI-Training stehen nur kostenlose GPU-Angebote mit Limits zur Verfügung.

- **Organisatorisch**:
Begrenzte Zeit im Rahmen des SYP-Unterrichts, Koordination im fünfköpfigen Team und eine nicht garantierte Zusammenarbeit mit den ASZs.


---
*last change: 22.09.2026*

---
[← Übersicht]({{ '/' | relative_url }}) · [Management]({{ '/management/' | relative_url }}) · [Architektur]({{ '/architecture/' | relative_url }})
