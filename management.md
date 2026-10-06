---
layout: page
title: Projektmanagement & Meilensteine
permalink: /management/
---

## 1. Vorgehensmodell

Das Projekt wird nach **Scrum** umgesetzt. Jeder Meilenstein liefert ein **lauffähiges, präsentierbares Inkrement** (MVP-Stufe), das auf dem vorherigen aufbaut. Funktionen werden dadurch nicht „am Ende zusammengesteckt“, sondern die App ist ab Meilenstein 1 durchgehend von Foto/Eingabe bis zur Entsorgungsempfehlung benutzbar und wird schrittweise erweitert.

### 1.1 Rollen

| Rolle         | Person(en) |
|---------------|------------|
| Product Owner | TODO       |
| Scrum Master  | TODO       |
| Dev-Team      | Kerimcan Yagci, Nico Haider, Milan Nuzdic, Jan Brunner, Mario Solomun |

### 1.2 Sprint-Rhythmus

| Element             | Festlegung |
|---------------------|------------|
| Sprint-Länge        | 2 Wochen (TODO: vom Team bestätigen) |
| Sprint Planning     | zu Beginn jedes Sprints, im SYP-Unterricht |
| Daily / Weekly      | kurzer Statusabgleich pro Unterrichtseinheit |
| Sprint Review       | am Sprint-Ende: Demo des Inkrements |
| Retrospektive       | im Anschluss an das Review |
| Backlog-Verwaltung  | GitHub Projects (Issues = User Stories) |

### 1.3 Definition of Done

Eine User Story gilt als erledigt, wenn:

- der Code im `main`-Branch gemergt ist (über Pull Request mit mindestens einem Review)
- die Akzeptanzkriterien der Story erfüllt sind
- die App auf mindestens einem Android- **und** einem iOS-Gerät/Emulator baut und startet
- relevante Tests vorhanden sind und durchlaufen
- die Dokumentation (dieses Repo) bei Bedarf aktualisiert ist

---

## 2. Meilenstein-Übersicht

*Die genauen Termine werden vom Team im Sprint Planning festgelegt.*

| #  | Meilenstein                         | MVP-Stufe | Ergebnis (Inkrement)                                            | Datum |
|----|-------------------------------------|-----------|-----------------------------------------------------------------|-------|
| M0 | Projekt-Setup                       | –         | Leeres, lauffähiges App-Gerüst, Board, CI                       | TODO  |
| M1 | Walking Skeleton                    | MVP 1     | Manuelle Auswahl Abfallart → richtige Tonne bzw. Container im **ASZ** | TODO  |
| M2 | ASZ-Regeln & Backend                | MVP 2     | Backend mit Trennregeln und Abfallarten des **ASZ**, App bindet es an | TODO  |
| M3 | KI-Erkennung                        | MVP 3     | Foto → **nachtrainiertes KI-Modell** erkennt Abfallart → Empfehlung | TODO  |
| M4 | Release Candidate                   | MVP 4     | Getestete, stabile App mit verbesserter KI-Genauigkeit          | TODO  |
| M5 | Abschluss                           | Release   | Finale Version, Dokumentation, Präsentation                     | TODO  |

**Paralleler Strang – Trainingsdaten:** Da das Basismodell für das ASZ nachtrainiert wird und dafür gelabelte Bilder benötigt, startet die Datensammlung bereits ab M1 parallel zur App-Entwicklung, damit in M3 ausreichend Daten zur Verfügung stehen.

---

## 3. Meilensteine im Detail

### M0 – Projekt-Setup

**Ziel:** Das Team kann arbeiten; jede weitere Story kann direkt umgesetzt werden.

**Umfang:**
- .NET-MAUI-Projekt anlegen, Build für Android und iOS
- Git-Repository, Branching-Strategie, Pull-Request-Regeln
- GitHub Projects-Board mit initialem Product Backlog (Epics siehe Abschnitt 4)
- Rollen und Sprint-Rhythmus festlegen

**Akzeptanzkriterien:**
- [ ] Leere App startet auf Android- und iOS-Emulator
- [ ] Jedes Teammitglied kann bauen, pushen und PRs erstellen
- [ ] Backlog enthält die Epics mit ersten User Stories

---

### M1 – MVP 1: Walking Skeleton

**Ziel:** Kleinster durchgängiger Nutzen – der Nutzer erfährt, in welche Tonne ein Gegenstand gehört, zunächst ohne KI.

**User Stories:**
- Als Nutzer möchte ich eine Abfallart aus einer Liste auswählen, damit ich erfahre, in welche Tonne sie gehört.
- Als Nutzer möchte ich die Empfehlung klar und verständlich angezeigt bekommen (Tonne + Farbe/Symbol).

**Umfang:**
- Regel-Datenbank (Datenmodell + Befüllung) für das **ASZ**
- Liste der Abfallkategorien (entspricht später den Klassen des KI-Modells)
- Screen: Kategorie wählen → Ergebnis-Screen mit Tonne
- Start der Trainingsdatensammlung (Kategorien festlegen, Label-Konvention definieren)

**Akzeptanzkriterien:**
- [ ] Für jede definierte Kategorie wird die korrekte Tonne bzw. der korrekte Container im ASZ angezeigt
- [ ] Regeldaten sind mit Quelle (URL, Abrufdatum) hinterlegt
- [ ] Kategorien- und Label-Liste für das KI-Modell ist fixiert

---

### M2 – MVP 2: ASZ-Regeln & Backend

**Ziel:** Die Empfehlung basiert auf den tatsächlichen Regeln des ASZ und wird zentral vom Backend bereitgestellt.

**User Stories:**
- Als Nutzer möchte ich sehen, welche Abfallarten das ASZ annimmt und wohin sie gehören.
- Als Nutzer möchte ich bei Gegenständen, die nicht in eine Haushaltstonne gehören, erfahren, dass sie im ASZ abzugeben sind.

**Umfang:**
- Backend (Spring Boot) mit REST-Schnittstelle für Regeln und Abfallarten
- Regel-Datenbank erweitert um die vollständigen Regeln und Annahmebedingungen des ASZ
- Anbindung der App an das Backend
- Prüfung öffentlicher Schnittstellen von Entsorgungsunternehmen (optional anbinden)

**Akzeptanzkriterien:**
- [ ] App lädt die Regeln über das Backend
- [ ] Alle Abfallarten des ASZ sind mit korrekter Zuordnung hinterlegt
- [ ] Gegenstände, die nicht in eine Haushaltstonne passen, werden als ASZ-Abgabe ausgewiesen

---

### M3 – MVP 3: KI-Erkennung

**Ziel:** Der Nutzer fotografiert den Gegenstand, statt ihn manuell auszuwählen.

**User Stories:**
- Als Nutzer möchte ich einen Gegenstand fotografieren, damit die App die Abfallart automatisch erkennt.
- Als Nutzer möchte ich das Ergebnis korrigieren können, wenn die KI unsicher oder falsch ist.

**Umfang:**
- Aufbereiteter, gelabelter Trainingsdatensatz (Train/Validation/Test-Split)
- Nachtrainieren (Fine-Tuning) eines **bestehenden Basismodells** auf die Abfallarten des ASZ
- Export des Modells in ein in der App nutzbares Format und Integration
- Foto-Aufnahme in der App → Klassifikation → bestehender Empfehlungs-Flow aus M1/M2
- Fallback: bei niedriger Konfidenz wird die manuelle Auswahl angeboten

**Akzeptanzkriterien:**
- [ ] Modell erreicht auf dem Testdatensatz eine Genauigkeit von mindestens TODO %
- [ ] Foto → Empfehlung funktioniert Ende-zu-Ende auf einem echten Gerät
- [ ] Unter einem Konfidenz-Schwellwert wird die manuelle Auswahl angezeigt

---

### M4 – MVP 4: Release Candidate

**Ziel:** Die App ist stabil, zuverlässig und datenschutzkonform.

**Umfang:**
- Systematische Tests aller Funktionen (KI-Erkennung, Regelzuordnung)
- Tests auf mehreren Geräten/Betriebssystemen
- Verbesserung der KI-Genauigkeit (mehr Daten, Fehleranalyse falsch erkannter Klassen)
- Aktualisierung und Prüfung der Regeldaten
- Datenschutz: Umgang mit Fotos prüfen und dokumentieren
- Bugfixing

**Akzeptanzkriterien:**
- [ ] Keine offenen Bugs mit Priorität „hoch“
- [ ] Modell-Genauigkeit gegenüber M3 verbessert und dokumentiert
- [ ] Testprotokoll für Android und iOS vorhanden

---

### M5 – Abschluss

**Ziel:** Fertigstellung und Abgabe im Rahmen des SYP-Unterrichts.

**Umfang:**
- Finale Version der App
- Vollständige Projektdokumentation (inkl. [Architektur]({{ '/architecture/' | relative_url }}))
- Abschlusspräsentation mit Live-Demo

**Akzeptanzkriterien:**
- [ ] Dokumentation vollständig und aktuell
- [ ] Präsentation und Demo erfolgreich durchgeführt

---

## 4. Product Backlog – Epics

| Epic                 | Beschreibung                                           | Meilenstein |
|----------------------|--------------------------------------------------------|-------------|
| App-Grundgerüst      | MAUI-Projekt, Navigation, UI-Grundlayout               | M0, M1      |
| Regel-Datenbank      | Recherche, Datenmodell und Pflege der Trennregeln      | M1, M2      |
| Backend              | Spring-Boot-Backend, ASZ-Regeln, REST-Schnittstelle    | M2          |
| Trainingsdaten       | Sammeln, Labeln und Aufbereiten von Abfallbildern      | M1 – M3     |
| KI-Modell            | Fine-Tuning, Evaluation und Integration des Modells | M3, M4    |
| Qualität             | Tests, Bugfixing, Datenschutz                          | M4          |
| Dokumentation        | Projektdokumentation und Präsentation                  | laufend, M5 |

---
[← Übersicht]({{ '/' | relative_url }}) · [Projektantrag]({{ '/project-proposal/' | relative_url }}) · [Architektur]({{ '/architecture/' | relative_url }})
