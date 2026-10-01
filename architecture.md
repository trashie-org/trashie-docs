---
layout: page
title: Architektur
permalink: /architecture/
---

## 1. Komponenten

- **App (.NET MAUI):** Foto-Aufnahme, GPS-Standorterfassung, manuelle Auswahl und Anzeige der Entsorgungsempfehlung
- **KI-Modell:** eigens trainiertes Modell zur Klassifikation der Abfallart anhand eines Fotos
- **Regel-Datenbank:** manuell gepflegte Trennregeln und Recyclingstationen für Linz, Oberösterreich und das Mühlviertel, optional ergänzt durch öffentliche Schnittstellen von Entsorgungsunternehmen

## 2. Cross-Platform-Framework: .NET MAUI vs. Flutter/React Native

### Vorteile .NET MAUI
- eine gemeinsame Codebasis (C#) für iOS und Android
- Nutzung der aus dem Unterricht bekannten .NET/C#-Umgebung
- native Performance und Zugriff auf Gerätefunktionen (Kamera, GPS)
- gute Werkzeugunterstützung durch Visual Studio

### Nachteile
- kleineres Community-Ökosystem und weniger Drittbibliotheken als bei Flutter/React Native
- teils weniger ausgereifte UI-Komponenten
- potenziell größere App-Größe

---
[← Übersicht]({{ '/' | relative_url }}) · [Projektantrag]({{ '/project-proposal/' | relative_url }}) · [Management]({{ '/management/' | relative_url }})
