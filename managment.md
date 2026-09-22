---
layout: page
title: Management
permalink: /management/
---

## 1. Planung

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

## 2. Architektur

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
[← Übersicht]({{ '/' | relative_url }}) · [Projektantrag]({{ '/project-proposal/' | relative_url }})
