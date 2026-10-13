---
layout: page
title: Tasks
permalink: /task/
---

# Tasks

Die folgenden Einträge sind aus Sicht der App bzw. des Projektteams formuliert und werden später zu Tasks. Sie sind nach Epics gegliedert und bestehen aus Story, Akzeptanzkriterien, Effort und Priority.

- **Effort:** noch offen, wird später geschätzt
- **Priority:** Hoch, Mittel oder Niedrig

## Epic 9: Regeldaten und Backend

### User Story 9.1 - Abfallkategorien bereitstellen

**Story:** Als App möchte ich die Abfallkategorien über eine REST-Schnittstelle laden, um dieselbe Kategorienliste wie Backend und KI-Modell zu verwenden.

**Akzeptanzkriterien:**

- [ ] Der Endpoint liefert je Kategorie ID, Name, Beschreibung und optionale Hinweise
- [ ] Die Antwort enthält ein Änderungsdatum oder eine Version

**Effort:**

**Priority:** Hoch

### User Story 9.2 - Trennregeln je Gemeinde bereitstellen

**Story:** Als App möchte ich die Trennregeln einer Gemeinde abrufen, um eine Empfehlung anzuzeigen, die zum Standort des Nutzers passt.

**Akzeptanzkriterien:**

- [ ] Der Endpoint liefert je Kategorie Entsorgungsweg, Tonne bzw. Container, Farbe bzw. Symbol, Quelle und Abrufdatum
- [ ] Eine unbekannte Gemeinde führt zu einer definierten Fehlerantwort

**Effort:**

**Priority:** Hoch

### User Story 9.3 - Sammelstellen bereitstellen

**Story:** Als App möchte ich die Sammelstellen einer Gemeinde abrufen, um bei einer ASZ-Abgabe die passende Sammelstelle anzeigen zu können.

**Akzeptanzkriterien:**

- [ ] Der Endpoint liefert Name, Adresse, Koordinaten, Öffnungszeiten und angenommene Abfallarten
- [ ] Jede Sammelstelle ist einer Gemeinde oder Region zugeordnet

**Effort:**

**Priority:** Mittel

### User Story 9.4 - Foto klassifizieren

**Story:** Als App möchte ich ein Foto an das Backend senden und eine Abfallkategorie zurückbekommen, um die Erkennung nicht am Smartphone ausführen zu müssen.

**Akzeptanzkriterien:**

- [ ] Der Endpoint nimmt ein Bild entgegen und antwortet mit Kategorie, Sicherheit und weiteren Vorschlägen
- [ ] Ungültige oder zu große Dateien führen zu einer definierten Fehlerantwort
- [ ] Das Foto wird nach der Klassifikation nicht gespeichert

**Effort:**

**Priority:** Hoch

### User Story 9.5 - Regeln ohne App-Update pflegen

**Story:** Als Projektteam möchten wir Trennregeln und ASZ-Daten zentral pflegen, um geänderte Regeln ohne neue App-Version an die Nutzer auszuliefern.

**Akzeptanzkriterien:**

- [ ] Regeln können im Backend angelegt, geändert und entfernt werden
- [ ] Eine Regel ohne Quelle und Abrufdatum kann nicht gespeichert werden
- [ ] Eine Änderung ist nach der nächsten Aktualisierung in der App sichtbar

**Effort:**

**Priority:** Mittel

### User Story 9.6 - Regeln der Pilotregion erfassen

**Story:** Als Projektteam möchten wir die Trennregeln der Pilotregion recherchieren und erfassen, um für jede Gemeinde eine Empfehlung geben zu können.

**Akzeptanzkriterien:**

- [ ] Für jede Abfallkategorie und jedes Regelgebiet ist eine Zuordnung hinterlegt
- [ ] Es werden nur Fakten übernommen, keine Texte, Grafiken oder Logos der Gemeinden bzw. Entsorgungsunternehmen
- [ ] Lizenzbedingungen offener Quellen (z. B. Namensnennung) sind eingehalten

**Effort:**

**Priority:** Hoch

### User Story 9.7 - KI-Modell austauschbar anbinden

**Story:** Als Projektteam möchten wir das KI-Modell im Backend austauschen können, um ein neu trainiertes Modell ohne Änderung der App einsetzen zu können.

**Akzeptanzkriterien:**

- [ ] Das Backend kapselt den Aufruf des Modells
- [ ] Die verwendete Modellversion ist dokumentiert
- [ ] Die Klassen des Modells stimmen mit der Kategorienliste überein

**Effort:**

**Priority:** Mittel

## Epic 10: Trainingsdaten und KI-Modell

### User Story 10.1 - Abfallklassen festlegen

**Story:** Als Projektteam möchten wir die Abfallklassen festlegen, um in Trainingsdaten, Backend und Frontend dieselben Begriffe zu verwenden.

**Akzeptanzkriterien:**

- [ ] Die Klassenliste enthält ca. 20 bis 30 Kategorien
- [ ] Jede Klasse hat eine kurze Beschreibung mit Beispielen und Abgrenzung zu ähnlichen Klassen
- [ ] Die Label-Konvention ist dokumentiert

**Effort:**

**Priority:** Hoch

### User Story 10.2 - Trainingsbilder sammeln und labeln

**Story:** Als Projektteam möchten wir gelabelte Bilder je Abfallklasse sammeln, um das Modell auf unsere Kategorien nachtrainieren zu können.

**Akzeptanzkriterien:**

- [ ] Je Klasse liegen ca. 300 gelabelte Bilder vor
- [ ] Quelle und Lizenz jedes Datensatzes sind dokumentiert
- [ ] Auf eigenen Fotos sind keine erkennbaren Personen abgebildet
- [ ] Die Aufteilung in Trainings-, Validierungs- und Testdaten ist festgelegt

**Effort:**

**Priority:** Hoch

### User Story 10.3 - Basismodell auswählen

**Story:** Als Projektteam möchten wir ein vortrainiertes Basismodell auswählen, um das Fine-Tuning mit kostenlosen GPU-Ressourcen durchführen zu können.

**Akzeptanzkriterien:**

- [ ] Mindestens zwei Modelle sind verglichen
- [ ] Die Lizenz des gewählten Modells ist geprüft und passt zum Projekt
- [ ] Die Entscheidung ist in der Architektur begründet

**Effort:**

**Priority:** Hoch

### User Story 10.4 - Modell nachtrainieren und bewerten

**Story:** Als Projektteam möchten wir das Basismodell auf unsere Abfallklassen nachtrainieren, um mit der Foto-Erkennung die geforderte Genauigkeit zu erreichen.

**Akzeptanzkriterien:**

- [ ] Das Modell erreicht auf dem Testdatensatz die festgelegte Mindestgenauigkeit
- [ ] Das Training ist reproduzierbar dokumentiert
- [ ] Der Schwellwert für unsichere Erkennungen ist festgelegt und begründet

**Effort:**

**Priority:** Hoch

### User Story 10.5 - Falsch erkannte Klassen analysieren

**Story:** Als Projektteam möchten wir auswerten, welche Klassen häufig verwechselt werden, um gezielt Bilder nachsammeln und die Genauigkeit verbessern zu können.

**Akzeptanzkriterien:**

- [ ] Eine Auswertung der Verwechslungen je Klasse liegt vor
- [ ] Für die schwächsten Klassen sind zusätzliche Bilder gesammelt
- [ ] Die Genauigkeit ist gegenüber dem ersten trainierten Modell verbessert und dokumentiert

**Effort:**

**Priority:** Mittel

---
*last change: 13.10.2026*

---
[← Übersicht]({{ '/' | relative_url }}) · [User Stories]({{ '/user-stories/' | relative_url }}) · [Pflichtenheft]({{ '/specification.html' | relative_url }}) · [Management]({{ '/management/' | relative_url }}) · [Architektur]({{ '/architecture/' | relative_url }})
