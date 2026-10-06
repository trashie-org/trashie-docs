---
layout: page
title: Architektur
permalink: /architecture/
---

## 1. Komponenten

- **App (.NET MAUI):** Foto-Aufnahme, manuelle Auswahl und Anzeige der Entsorgungsempfehlung für das jeweilige Altstoffsammelzentrum (ASZ)
- **Backend (Spring Boot):** stellt die Trennregeln und ASZ-Daten über eine REST-Schnittstelle bereit und bindet das KI-Modell an
- **KI-Modell:** bereits existierendes, stark vortrainiertes Modell, das gezielt auf die Abfallarten des jeweiligen ASZ nachtrainiert (Fine-Tuning) wird
- **Regel-Datenbank:** manuell gepflegte Trennregeln des ASZ, optional ergänzt durch öffentliche Schnittstellen von Entsorgungsunternehmen

## 2. Entscheidungsbegründungen

### 2.1 KI-Modell: Fine-Tuning statt eigenem Training von Grund auf

Wir trainieren kein Modell von Grund auf, sondern verwenden ein bereits existierendes, stark vortrainiertes Bildklassifikationsmodell und trainieren es für die Abfallarten des ASZ nach.

- Vortrainierte Modelle kommen bereits mit schlechter Belichtung, geringer Bildqualität und mehreren Objekten im Bild zurecht. Diese Szenarien selbst abzudecken wäre für unser Team nicht im Projektzeitraum machbar.
- Der Aufwand wird auf die Präzision für die tatsächlich relevanten Abfallarten des ASZ verwendet.
- Für das Nachtrainieren genügt ein deutlich kleinerer Datensatz, was zu den begrenzten (kostenlosen) GPU-Ressourcen passt.

### 2.2 Cross-Platform-Framework: .NET MAUI

Wir haben uns für .NET MAUI entschieden, weil:

- eine gemeinsame C#-Codebasis iOS und Android abdeckt
- das Team die .NET/C#-Umgebung aus dem Unterricht bereits kennt
- Gerätefunktionen wie die Kamera und von uns benötigte Services nativ und direkt zugänglich sind
- die Werkzeugunterstützung (Visual Studio) gut ist

Alternativen wie Flutter oder React Native würden einen Wechsel auf Dart bzw. JavaScript/TypeScript bedeuten. Die Diskussion im Team drehte sich zudem vor allem um .NET Avalonia, das wir gegenüber MAUI wegen der besseren Unterstützung der benötigten Services nicht gewählt haben.

### 2.3 Backend: Spring Boot

Wir haben uns für Spring Boot (Java) gegenüber Express (Node.js) entschieden, weil:

- Spring Boot ein ausgereiftes Framework mit Dependency Injection, Datenzugriff (Spring Data) und Validierung bereits mitbringt, während bei Express diese Bausteine erst aus einzelnen Bibliotheken zusammengestellt werden müssten
- Java mit statischer Typisierung das Backend bei einem wachsenden Regelmodell wartbar und weniger fehleranfällig macht
- Java im Unterricht behandelt wird und das Team es sicher beherrscht
- REST-Schnittstellen, Datenbankanbindung und Tests mit wenig Konfigurationsaufwand umsetzbar sind

---
[← Übersicht]({{ '/' | relative_url }}) · [Projektantrag]({{ '/project-proposal/' | relative_url }}) · [Management]({{ '/management/' | relative_url }})
