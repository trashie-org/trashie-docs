# Projektantrag Trashie (KI-gestützte Mülltrennungs-App)
Kerimcan Yagci, Nico Haider, Milan Nuzdic, Jan Brunner und Mario Solomun

*Schulprojekt im Rahmen des SYP-Unterrichts*

## 1. Ausgangslage

### 1.1 Ist-Situation
Die korrekte Trennung von Abfall ist für viele Menschen im Alltag schwierig, da sich die Regeln je nach Gemeinde bzw. zuständigem Entsorgungsunternehmen unterscheiden. Das führt zu mehreren Problemen wie zum Beispiel:
- Unsicherheit, in welche Tonne oder zu welcher Recyclingstation ein Gegenstand gehört
- uneinheitliche Regeln zwischen einzelnen Gemeinden, z. B. innerhalb von Linz, dem restlichen Oberösterreich und dem Mühlviertel
- dadurch bedingte Fehlwürfe, die das Recycling erschweren und Wertstoffe verloren gehen lassen
- fehlendes zentrales, leicht zugängliches Nachschlagewerk für Privatpersonen
- besondere Unsicherheit bei Personen, die neu in eine Region ziehen oder diese nur vorübergehend nutzen (z. B. Studierende)

### 1.2 Verbesserungsvorschläge
Mithilfe von Trashie, einer KI-gestützten Mülltrennungs-App, kann der Nutzer ein Foto eines Abfallgegenstandes aufnehmen. Die App erkennt mittels eines eigens trainierten KI-Modells, um welche Art von Abfall es sich handelt, bestimmt über GPS den aktuellen Standort und ordnet den Gegenstand anhand der lokal gültigen Regeln der richtigen Tonne bzw. Recyclingstation zu. In der ersten Ausbaustufe liegt der Fokus auf Linz, Oberösterreich und dem Mühlviertel; eine Erweiterung auf weitere Regionen ist danach möglich.

## 2. Zielsetzung
Trashie soll nicht nur die Materialart eines Gegenstandes erkennen (z. B. "Kunststoff"), sondern eine konkrete, standortabhängige Handlungsempfehlung geben: in welche Tonne der Gegenstand in der jeweiligen Gemeinde gehört, bzw. an welche Recyclingstation er abgegeben werden muss, falls er nicht über die Haushaltstonnen entsorgt werden kann.

### Features

#### App:

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

#### Regel-Datenbank:

- **Recherche der lokalen Trennregeln**:
Die Regeln für Linz, Oberösterreich und das Mühlviertel werden online über frei zugängliche Quellen (z. B. Abfallkalender, Gemeinde-Webseiten) recherchiert und in einer eigenen Datenbank gepflegt; es werden keine konkreten Entsorgungsunternehmen als Kooperationspartner genannt.

- **Manuelle Pflege mit optionaler API-Anbindung**:
Die Regeln werden primär in einer manuell gepflegten Datenbank hinterlegt. Sofern ein Entsorgungsunternehmen eine öffentliche Schnittstelle anbietet, kann diese ergänzend zur automatischen Aktualisierung genutzt werden.

- **Regelmäßige Aktualisierung**:
Da sich lokale Vorschriften ändern können, muss die Datenbank periodisch überprüft und aktualisiert werden.

## 3. Chancen und Risiken

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

## 4. Planung

### Meilensteine

*Der genaue Zeitplan ist noch offen und muss vom Team festgelegt werden. Die folgenden Meilensteine dienen als vorläufige Grundlage.*

## 1. Grundfunktionalität (Datum: TODO)
**Ziel:** App-Grundgerüst mit Foto-Aufnahme und Standorterfassung.

**Beschreibung:**
- Aufbau des App-Grundgerüsts mit .NET MAUI
- Implementierung der **Foto-Aufnahme**
- Implementierung der **GPS-Standorterfassung**

## 2. Aufbau der Regel-Datenbank (Datum: TODO)
**Ziel:** Erfassung der lokalen Mülltrennungsregeln für die Pilotregion.

**Beschreibung:**
- Online-Recherche der **Trennregeln für Linz, Oberösterreich und das Mühlviertel**
- Aufbau einer **manuell gepflegten Datenbank**
- Prüfung, ob für einzelne Regionen bereits **öffentliche Schnittstellen** verfügbar sind

## 3. Training und Integration des KI-Modells (Datum: TODO)
**Ziel:** Eigenständige Erkennung von Abfallarten anhand von Fotos.

**Beschreibung:**
- Sammlung/Aufbereitung von Trainingsdaten
- **Training des eigenen KI-Modells** zur Abfallklassifikation
- Integration des Modells in die App

## 4. Verknüpfung von KI, Standort und Regeln (Datum: TODO)
**Ziel:** Automatische Zuordnung zur richtigen Tonne bzw. Recyclingstation.

**Beschreibung:**
- Zusammenführung von **KI-Erkennung**, **GPS-Standort** und **Regel-Datenbank**
- Anzeige der konkreten Entsorgungsempfehlung inklusive Recyclingstationen

## 5. Testing und Optimierung (Datum: TODO)
**Ziel:** Verbesserung der Zuverlässigkeit der App.

**Beschreibung:**
- **Testphase** aller Funktionen (KI-Erkennung, Standortbestimmung, Regelzuordnung)
- Optimierung der **KI-Genauigkeit**
- Behebung von Bugs

## 6. Abschluss, Dokumentation und Präsentation (Datum: TODO)
**Ziel:** Fertigstellung des Projekts im Rahmen des SYP-Unterrichts.

**Beschreibung:**
- Vollständige **Projektdokumentation**
- Vorbereitung der **Abschlusspräsentation**

## 5. Architektur

### Cross-Platform-Framework: .NET MAUI vs. Flutter/React Native

#### Vorteile .NET MAUI
- eine gemeinsame Codebasis (C#) für iOS und Android
- Nutzung der aus dem Unterricht bekannten .NET/C#-Umgebung
- native Performance und Zugriff auf Gerätefunktionen (Kamera, GPS)
- gute Werkzeugunterstützung durch Visual Studio

#### Nachteile
- kleineres Community-Ökosystem und weniger Drittbibliotheken als bei Flutter/React Native
- teils weniger ausgereifte UI-Komponenten
- potenziell größere App-Größe

---

### KI-Ansatz: eigenes trainiertes Modell vs. Cloud-KI-API

#### Vorteile eigenes Modell
- keine laufenden API-Kosten (passend zum Budget von 0 Euro)
- volle Kontrolle über Trainingsdaten und erkennbare Kategorien
- potenziell offline nutzbar
- keine Weitergabe von Nutzerfotos an externe Dienste

#### Nachteile
- höherer Trainingsaufwand, benötigt eigene gelabelte Datensätze
- Genauigkeit anfangs voraussichtlich geringer als bei großen kommerziellen Cloud-Modellen (siehe Risiken)
- Rechenleistung für das Training des Modells nötig

---
*last change: 22.09.2026*
