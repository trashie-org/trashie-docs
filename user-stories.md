---
layout: page
title: User Stories
permalink: /user-stories/
---

# User Stories

Die Stories sind nach Epics gegliedert. Jede Story besteht aus Story, Akzeptanzkriterien, Effort und Priority.

- **Effort:** noch offen, wird später geschätzt
- **Priority:** Hoch, Mittel oder Niedrig

## Epic 1: Bilderkennung

### User Story 1.1 - Gegenstand fotografieren

**Story:** Als Nutzer möchte ich einen Abfallgegenstand direkt in der App fotografieren, um ihn nicht selbst benennen und nachschlagen zu müssen.

**Akzeptanzkriterien:**

- [ ] Die Kamera ist die Startansicht der App
- [ ] Ein Tipp auf den Auslöser nimmt das Foto auf und sendet es zur Klassifikation an das Backend
- [ ] Während der Analyse ist ein Ladezustand sichtbar
- [ ] Bevor die Kamera aktiviert wird muss ein pop up auftauchen, wo der Nutzer bestätigt, dass er die Kamera verwenden will.

**Effort:**

**Priority:** Hoch

### User Story 1.2 - Erkannte Abfallart mit Sicherheit sehen

**Story:** Als Nutzer möchte ich sehen, welche Abfallart erkannt wurde und wie sicher sich die KI ist, um einschätzen zu können, ob ich dem Ergebnis vertrauen kann.

**Akzeptanzkriterien:**

- [ ] Die Ergebnisansicht zeigt die erkannte Abfallkategorie
- [ ] Die Sicherheit der Erkennung wird als Prozentwert angezeigt

**Effort:**

**Priority:** Hoch

### User Story 1.3 - Schnelles Ergebnis

**Story:** Als Nutzer möchte ich das Ergebnis innerhalb weniger Sekunden erhalten, um für das Nachschauen nicht länger zu brauchen als für das Wegwerfen.

**Akzeptanzkriterien:**

- [ ] Zwischen Auslösen und Anzeige der Empfehlung vergehen auf einem Mittelklasse-Smartphone höchstens 3 Sekunden
- [ ] Antwortet das Backend nicht rechtzeitig, erscheint eine verständliche Fehlermeldung. (Direkt nachschlagen oder weiter warten)

**Effort:**

**Priority:** Mittel

### User Story 1.4 - Unsichere Erkennung

**Story:** Als Nutzer möchte ich bei einer unsicheren Erkennung keine falsche Empfehlung bekommen, um meinen Abfall nicht aufgrund eines geratenen Ergebnisses falsch zu entsorgen.

**Akzeptanzkriterien:**

- [ ] Liegt die Sicherheit unter dem festgelegten Schwellwert, wird keine Empfehlung angezeigt
- [ ] Stattdessen wird die manuelle Auswahl angeboten
- [ ] Der Nutzer erfährt, dass der Gegenstand nicht sicher erkannt wurde

**Effort:**

**Priority:** Hoch

### User Story 1.5 - Foto wiederholen

**Story:** Als Nutzer möchte ich ein misslungenes Foto sofort wiederholen können, um bei einem unscharfen oder schlecht belichteten Bild einen zweiten Versuch zu haben.

**Akzeptanzkriterien:**

- [ ] Aus der Ergebnisansicht führt ein Schritt zurück zur Kamera
- [ ] Das vorherige Foto und Ergebnis werden dabei verworfen

**Effort:**

**Priority:** Mittel

### User Story 1.6 - Fotografieren ohne Internet

**Story:** Als Nutzer möchte ich ohne Internetverbindung einen klaren Hinweis statt einer endlosen Ladeanzeige bekommen, um zu wissen, warum die Erkennung nicht funktioniert.

**Akzeptanzkriterien:**

- [ ] Ohne Verbindung zeigt die App, dass die Foto-Analyse eine Internetverbindung benötigt
- [ ] Die manuelle Auswahl wird als Alternative angeboten
- [ ] Die App stürzt nicht ab und bleibt bedienbar

**Effort:**

**Priority:** Mittel

### User Story 1.7 - Bild aus der Galerie wählen

**Story:** Als Nutzer möchte ich ein bereits aufgenommenes Bild aus meiner Galerie analysieren lassen, um einen Gegenstand auch später zuordnen zu können.

**Akzeptanzkriterien:**

- [ ] In der Kameraansicht kann ein Bild aus der Galerie gewählt werden
- [ ] Das Bild durchläuft denselben Ablauf wie ein neu aufgenommenes Foto
- [ ] Der Zugriff auf die Galerie erfolgt erst nach Zustimmung

**Effort:**

**Priority:** Niedrig

### User Story 1.8 - Tipps für ein gutes Foto

**Story:** Als Nutzer möchte ich bei einer fehlgeschlagenen Erkennung einen kurzen Tipp bekommen, um beim nächsten Versuch ein besser erkennbares Foto aufzunehmen.

**Akzeptanzkriterien:**

- [ ] Bei unsicherer Erkennung erscheint ein Hinweis (z. B. nur ein Gegenstand, ruhiger Hintergrund, genug Licht)
- [ ] Der Hinweis blockiert die manuelle Auswahl nicht

**Effort:**

**Priority:** Niedrig


### User Story 1.9 - Foto machen in der App

**Story**: Als Nutzer möchte ich in der App ein Foto machen, um das Bild in der App zu sehen.

**Akzeptanzkriterien**

- [ ] Es gibt ein Fotofenster in der App.
- [ ] Es gibt einen Foto-Button in der App.
- [ ] Das Foto wird, nachdem auslösen angezeigt.

**Effort**

**Priority**: Hoch

## Epic 2: Manuelle Auswahl und Korrektur

### User Story 2.1 - Abfallart manuell auswählen

**Story:** Als Nutzer möchte ich eine Abfallart aus einer Liste auswählen, um auch ohne Foto eine Entsorgungsempfehlung zu bekommen.

**Akzeptanzkriterien:**

- [ ] Die manuelle Auswahl ist von der Kameraansicht aus erreichbar
- [ ] Die Liste der Abfallkategorien ist durchsuchbar
- [ ] Die Auswahl einer Kategorie öffnet die Ergebnisansicht
- [ ] Die Auswahl funktioniert offline mit den lokal gespeicherten Regeln

**Effort:**

**Priority:** Hoch

### User Story 2.2 - Kategorien verständlich dargestellt

**Story:** Als Nutzer möchte ich zu jeder Abfallkategorie Beispiele sehen, um die richtige Kategorie zu finden, auch wenn ich den Fachbegriff nicht kenne.

**Akzeptanzkriterien:**

- [ ] Jede Kategorie zeigt einen Namen und typische Beispiele (z. B. Leichtverpackungen: Joghurtbecher, PET-Flasche)

**Effort:**

**Priority:** Mittel

### User Story 2.3 - Erkennung korrigieren

**Story:** Als Nutzer möchte ich ein falsches Ergebnis korrigieren können, um trotzdem die richtige Empfehlung zu bekommen.

**Akzeptanzkriterien:**

- [ ] Die Ergebnisansicht enthält „Falsch erkannt? Korrigieren“
- [ ] Die Korrektur zeigt die weiteren Vorschläge der KI zur Auswahl
- [ ] Nach der Auswahl wird die Empfehlung für die neue Kategorie angezeigt

**Effort:**

**Priority:** Hoch

### User Story 2.4 - Von der Korrektur zur manuellen Auswahl

**Story:** Als Nutzer möchte ich aus der Korrektur zur vollständigen Kategorienliste wechseln können, um auch dann ans Ziel zu kommen, wenn keiner der Vorschläge passt.

**Akzeptanzkriterien:**

- [ ] Die Korrekturansicht enthält einen Zugang zur manuellen Auswahl
- [ ] Die dort gewählte Kategorie ersetzt das Ergebnis der KI

**Effort:**

**Priority:** Mittel

## Epic 3: Standort und Gemeinde

### User Story 3.1 - Gemeinde automatisch erkennen

**Story:** Als Nutzer möchte ich meine Gemeinde automatisch erkennen lassen, um die an meinem Ort geltenden Regeln zu erhalten, ohne sie selbst einstellen zu müssen.

**Akzeptanzkriterien:**

- [ ] Die App ermittelt über GPS die Gemeinde, in der sich der Nutzer befindet
- [ ] Die Standortabfrage erfolgt erst nach Zustimmung
- [ ] Die Koordinaten werden nur zur Ermittlung der Gemeinde verwendet und nicht gespeichert

**Effort:**

**Priority:** Hoch

### User Story 3.2 - Gemeinde manuell auswählen

**Story:** Als Nutzer möchte ich meine Gemeinde selbst auswählen können, um die App auch ohne Standortfreigabe oder ohne GPS-Signal nutzen zu können.

**Akzeptanzkriterien:**

- [ ] Bei verweigerter Standortfreigabe oder fehlendem Signal wird die manuelle Gemeindeauswahl angeboten
- [ ] Die Gemeinden der Pilotregion sind in einer durchsuchbaren Liste auswählbar
- [ ] Die App ist ohne Standortfreigabe vollständig nutzbar

**Effort:**

**Priority:** Hoch

### User Story 3.3 - Aktuelle Gemeinde sehen und ändern

**Story:** Als Nutzer möchte ich jederzeit sehen, für welche Gemeinde die Empfehlungen gelten, und sie ändern können, um eine falsch erkannte Gemeinde (z. B. an der Gemeindegrenze) korrigieren zu können.

**Akzeptanzkriterien:**

- [ ] Die Kameraansicht zeigt die aktuell verwendete Gemeinde
- [ ] Ein Tipp auf die Gemeinde öffnet die Gemeindeauswahl
- [ ] Nach einer Änderung gelten die Regeln der neuen Gemeinde

**Effort:**

**Priority:** Mittel

### User Story 3.4 - Standort außerhalb der Pilotregion

**Story:** Als Nutzer außerhalb der Pilotregion möchte ich erfahren, dass für meinen Standort keine Regeln hinterlegt sind, um keine Empfehlung zu bekommen, die bei mir nicht gilt.

**Akzeptanzkriterien:**

- [ ] Liegt der Standort außerhalb der Pilotregion, zeigt die App einen entsprechenden Hinweis
- [ ] Es wird keine Empfehlung einer fremden Gemeinde ohne Kennzeichnung angezeigt
- [ ] Eine Gemeinde der Pilotregion kann weiterhin manuell gewählt werden

**Effort:**

**Priority:** Mittel

### User Story 3.5 - Gewählte Gemeinde merken

**Story:** Als Nutzer ohne Standortfreigabe möchte ich meine gewählte Gemeinde in der App gespeichert haben, um sie nicht bei jedem Start neu auswählen zu müssen.

**Akzeptanzkriterien:**

- [ ] Die manuell gewählte Gemeinde bleibt nach einem Neustart der App erhalten
- [ ] Gespeichert wird nur die Gemeinde am Gerät, keine Koordinaten

**Effort:**

**Priority:** Niedrig

## Epic 4: Entsorgungsempfehlung

### User Story 4.1 - Empfehlung anzeigen

**Story:** Als Nutzer möchte ich die Entsorgungsempfehlung klar angezeigt bekommen, um sofort zu sehen, in welche Tonne oder zu welcher Sammelstelle der Gegenstand gehört.

**Akzeptanzkriterien:**

- [ ] Die Ergebnisansicht zeigt Abfallkategorie und richtige Tonne bzw. richtigen Container
- [ ] Tonne bzw. Container werden mit Bezeichnung und Farbe bzw. Symbol dargestellt
- [ ] Es ist ersichtlich, für welche Gemeinde die Empfehlung gilt

**Effort:**

**Priority:** Hoch

### User Story 4.2 - Hinweis „ohne Gewähr“

**Story:** Als Nutzer möchte ich wissen, dass die Empfehlung nicht verbindlich ist, um im Zweifel bei der Gemeinde oder im ASZ nachzufragen.

**Akzeptanzkriterien:**

- [ ] Jede Empfehlung enthält den Hinweis, dass die Angaben ohne Gewähr sind
- [ ] Der Hinweis nennt, dass im Zweifel die Auskunft der Gemeinde bzw. des ASZ gilt

**Effort:**

**Priority:** Hoch

### User Story 4.3 - Hinweise zur richtigen Entsorgung

**Story:** Als Nutzer möchte ich zusätzlich erfahren, worauf ich beim Entsorgen achten muss, um den Gegenstand nicht nur in die richtige Tonne zu werfen, sondern ihn auch richtig vorzubereiten.

**Akzeptanzkriterien:**

- [ ] Zu einer Kategorie können Hinweise hinterlegt sein (z. B. restentleert, Deckel abnehmen, nicht stapeln)
- [ ] Vorhandene Hinweise werden bei der Empfehlung angezeigt
- [ ] Kategorien ohne Hinweise werden ohne leeren Bereich dargestellt

**Effort:**

**Priority:** Mittel

### User Story 4.4 - Warnung bei gefährlichen Gegenständen

**Story:** Als Nutzer möchte ich bei gefährlichen Gegenständen deutlich gewarnt werden, um z. B. keinen Lithium-Akku in den Restmüll zu werfen.

**Akzeptanzkriterien:**

- [ ] Kategorien können als Problemstoff gekennzeichnet werden
- [ ] Bei gekennzeichneten Kategorien zeigt die Empfehlung eine hervorgehobene Warnung
- [ ] Die Warnung nennt die Gefahr in einem Satz (z. B. Brandgefahr)

**Effort:**

**Priority:** Hoch

### User Story 4.5 - Quelle der Regel sehen

**Story:** Als Nutzer möchte ich sehen, woher eine Regel stammt und wie aktuell sie ist, um die Empfehlung überprüfen zu können.

**Akzeptanzkriterien:**

- [ ] Zur Empfehlung sind Quelle und Abrufdatum der Regel einsehbar
- [ ] Die Quelle ist als Link aufrufbar, sofern eine Internetverbindung besteht

**Effort:**

**Priority:** Mittel

### User Story 4.6 - Hinweis auf Einwegpfand

**Story:** Als Nutzer möchte ich bei Pfandflaschen und Pfanddosen auf das Pfand hingewiesen werden, um sie zurückzugeben, statt sie wegzuwerfen.

**Akzeptanzkriterien:**

- [ ] Für betroffene Kategorien wird ein Hinweis auf das Einwegpfand angezeigt
- [ ] Der Hinweis nennt die Rückgabe im Handel als Entsorgungsweg

**Effort:**

**Priority:** Niedrig

## Epic 5: Sammelstellen

### User Story 5.1 - ASZ-Abgabe erkennen

**Story:** Als Nutzer möchte ich bei Gegenständen, die in keine Haushaltstonne gehören, erfahren, dass sie im ASZ abzugeben sind, um sie nicht in die falsche Tonne zu werfen.

**Akzeptanzkriterien:**

- [ ] Die Empfehlung weist solche Gegenstände eindeutig als ASZ-Abgabe aus
- [ ] Die Darstellung unterscheidet sich erkennbar von einer Tonnen-Empfehlung
- [ ] Von der Empfehlung führt ein Schritt zur passenden Sammelstelle

**Effort:**

**Priority:** Hoch

### User Story 5.2 - Sammelstelle mit Adresse und Öffnungszeiten

**Story:** Als Nutzer möchte ich die passende Sammelstelle mit Adresse und Öffnungszeiten sehen, um zu wissen, wohin und wann ich den Gegenstand bringen kann.

**Akzeptanzkriterien:**

- [ ] Die Ansicht zeigt Name, Adresse und Öffnungszeiten des ASZ
- [ ] Die Sammelstelle passt zur gewählten Gemeinde und nimmt die Abfallart an
- [ ] Adresse und Öffnungszeiten sind auch offline abrufbar

**Effort:**

**Priority:** Hoch

### User Story 5.3 - Sammelstelle auf der Karte

**Story:** Als Nutzer möchte ich die Sammelstelle auf einer Karte sehen und die Navigation starten können, um den Weg dorthin zu finden.

**Akzeptanzkriterien:**

- [ ] Die Sammelstelle wird auf einer Karte angezeigt
- [ ] Die Adresse lässt sich in der Karten-App des Smartphones öffnen
- [ ] Ohne Internetverbindung bleibt die Adresse als Text sichtbar

**Effort:**

**Priority:** Mittel

### User Story 5.4 - Ist das ASZ gerade geöffnet?

**Story:** Als Nutzer möchte ich auf einen Blick sehen, ob die Sammelstelle gerade geöffnet hat, um nicht vor verschlossenem Tor zu stehen.

**Akzeptanzkriterien:**

- [ ] Die Ansicht zeigt „jetzt geöffnet“ bzw. „geschlossen“
- [ ] Bei geschlossenem ASZ wird der nächste Öffnungszeitpunkt genannt

**Effort:**

**Priority:** Niedrig

### User Story 5.5 - Mehrere Sammelstellen zur Auswahl

**Story:** Als Nutzer möchte ich alle für meine Gemeinde zuständigen Sammelstellen sehen, um diejenige wählen zu können, die für mich am besten erreichbar ist.

**Akzeptanzkriterien:**

- [ ] Gibt es mehrere passende Sammelstellen, werden sie als Liste angezeigt
- [ ] Jeder Eintrag zeigt Name, Ort und Öffnungszeiten

**Effort:**

**Priority:** Niedrig

## Epic 6: Nachschlagewerk

### User Story 6.1 - Alle Abfallkategorien durchstöbern

**Story:** Als Nutzer möchte ich alle Abfallkategorien in einer Liste sehen, um mich auch ohne konkreten Gegenstand über die Trennregeln informieren zu können.

**Akzeptanzkriterien:**

- [ ] Das Nachschlagewerk ist über die Navigationsleiste erreichbar
- [ ] Die Liste zeigt alle Kategorien mit ihrer Zuordnung für die gewählte Gemeinde
- [ ] Die Liste ist alphabetisch sortiert

**Effort:**

**Priority:** Hoch

### User Story 6.2 - Suche während der Eingabe

**Story:** Als Nutzer möchte ich im Nachschlagewerk suchen können, um einen Eintrag schneller zu finden als durch Scrollen.

**Akzeptanzkriterien:**

- [ ] Die Liste wird bereits während der Eingabe gefiltert
- [ ] Ergebnisse erscheinen in unter 200 ms
- [ ] Groß- und Kleinschreibung spielt keine Rolle

**Effort:**

**Priority:** Hoch

### User Story 6.3 - Suche nach Alltagsbegriffen

**Story:** Als Nutzer möchte ich nach dem Gegenstand suchen können, wie ich ihn im Alltag nenne, um auch mit „Pizzakarton“ oder „Tetra Pak“ den richtigen Eintrag zu finden.

**Akzeptanzkriterien:**

- [ ] Zu jeder Kategorie sind Suchbegriffe bzw. Beispiele hinterlegt
- [ ] Die Suche findet eine Kategorie auch über diese Begriffe
- [ ] Im Treffer ist sichtbar, zu welcher Kategorie der Begriff gehört

**Effort:**

**Priority:** Niedrig

### User Story 6.4 - Detailansicht eines Eintrags

**Story:** Als Nutzer möchte ich einen Eintrag antippen und alle Details sehen, um genau zu wissen, wie die Abfallart zu entsorgen ist.

**Akzeptanzkriterien:**

- [ ] Die Detailansicht zeigt Zuordnung, Hinweise zur Entsorgung und die Gemeinde, für die die Regel gilt
- [ ] Quelle und Abrufdatum der Regel sind angegeben
- [ ] Bei ASZ-Abgabe führt die Ansicht zur passenden Sammelstelle

**Effort:**

**Priority:** Hoch

### User Story 6.5 - Kein Treffer

**Story:** Als Nutzer möchte ich bei einer erfolglosen Suche einen Hinweis statt einer leeren Seite sehen, um zu wissen, wie ich weiterkomme.

**Akzeptanzkriterien:**

- [ ] Bei keinem Treffer erscheint ein Hinweis mit dem Suchbegriff
- [ ] Der Hinweis verweist auf die Auskunft der Gemeinde bzw. des ASZ

**Effort:**

**Priority:** Mittel

## Epic 7: Offline-Nutzung und Aktualität

### User Story 7.1 - Nachschlagen ohne Internet

**Story:** Als Nutzer möchte ich das Nachschlagewerk und die manuelle Auswahl ohne Internetverbindung nutzen, um auch im Keller oder im Müllraum eine Antwort zu bekommen.

**Akzeptanzkriterien:**

- [ ] Die zuletzt geladenen Regeln sind lokal gespeichert
- [ ] Nachschlagewerk, manuelle Auswahl und Empfehlung funktionieren im Flugmodus
- [ ] Nach der Installation genügt ein einmaliger Start mit Internetverbindung

**Effort:**

**Priority:** Hoch

### User Story 7.2 - Regeln automatisch aktualisieren

**Story:** Als Nutzer möchte ich automatisch die aktuellen Regeln erhalten, um nicht nach veralteten Vorgaben zu trennen und kein App-Update dafür zu brauchen.

**Akzeptanzkriterien:**

- [ ] Beim Start mit Internetverbindung prüft die App, ob neuere Regeldaten vorliegen
- [ ] Neue Daten ersetzen die lokal gespeicherten, ohne dass der Nutzer etwas tun muss
- [ ] Schlägt die Aktualisierung fehl, bleiben die bisherigen Daten nutzbar

**Effort:**

**Priority:** Mittel

### User Story 7.3 - Stand der Daten sehen

**Story:** Als Nutzer möchte ich sehen, wann die Regeln zuletzt aktualisiert wurden, um im Offline-Betrieb einschätzen zu können, wie aktuell sie sind.

**Akzeptanzkriterien:**

- [ ] Die App zeigt das Datum der letzten erfolgreichen Aktualisierung
- [ ] Im Offline-Betrieb ist erkennbar, dass gespeicherte Daten verwendet werden

**Effort:**

**Priority:** Niedrig

## Epic 8: Bedienbarkeit und Datenschutz

### User Story 8.1 - Zwischen Kamera und Nachschlagewerk wechseln

**Story:** Als Nutzer möchte ich jederzeit zwischen Kamera und Nachschlagewerk wechseln können, um mich in der App nicht zu verirren.

**Akzeptanzkriterien:**

- [ ] Eine Navigationsleiste mit Kamera und Nachschlagewerk ist in den Hauptansichten sichtbar
- [ ] Die aktive Ansicht ist in der Navigationsleiste hervorgehoben
- [ ] Die App ist für das Hochformat ausgelegt

**Effort:**

**Priority:** Hoch

### User Story 8.2 - Ohne Konto und Anleitung nutzbar

**Story:** Als Nutzer möchte ich die App sofort ohne Registrierung und ohne Einführung verwenden, um beim ersten Öffnen schon eine Antwort zu bekommen.

**Akzeptanzkriterien:**

- [ ] Es ist kein Nutzerkonto erforderlich
- [ ] Vom Start der App bis zur Empfehlung sind höchstens 3 Schritte nötig
- [ ] Nutzertests mit mindestens 5 teamfremden Testpersonen sind durchgeführt und dokumentiert

**Effort:**

**Priority:** Mittel

### User Story 8.3 - Einwilligung für Kamera und Standort

**Story:** Als Nutzer möchte ich gefragt werden, bevor die App auf Kamera und Standort zugreift, und den Grund dafür erfahren, um bewusst entscheiden zu können.

**Akzeptanzkriterien:**

- [ ] Kamera und Standort werden erst nach Zustimmung verwendet
- [ ] Die Abfrage erklärt in einem Satz, wofür der Zugriff benötigt wird
- [ ] Bei Ablehnung bleibt die App über manuelle Auswahl und Gemeindeauswahl nutzbar

**Effort:**

**Priority:** Hoch

### User Story 8.4 - Datenschutzerklärung einsehen

**Story:** Als Nutzer möchte ich die Datenschutzerklärung in der App lesen können, um zu wissen, was mit meinen Fotos und meinem Standort geschieht.

**Akzeptanzkriterien:**

- [ ] Die Datenschutzerklärung ist in der App erreichbar
- [ ] Sie beschreibt den Umgang mit Fotos und Standortdaten
- [ ] Sie ist auch offline lesbar

**Effort:**

**Priority:** Mittel

### User Story 8.5 - Fotos werden nicht aufbewahrt

**Story:** Als Nutzer möchte ich meine Fotos nach der Erkennung gelöscht wissen, um keine Bilder aus meinem Zuhause dauerhaft preiszugeben.

**Akzeptanzkriterien:**

- [ ] Das Backend speichert Fotos nicht über die Klassifikation hinaus
- [ ] Die App legt Fotos nicht in der Galerie oder im App-Speicher ab
- [ ] Metadaten des Fotos (z. B. GPS-Position) werden vor dem Senden entfernt
- [ ] Der Umgang mit Fotos ist geprüft und dokumentiert

**Effort:**

**Priority:** Hoch

### User Story 8.6 - Barrierearme Bedienung

**Story:** Als Nutzer mit Sehschwäche möchte ich die Empfehlung auch ohne Farbwahrnehmung verstehen, um die App selbstständig verwenden zu können.

**Akzeptanzkriterien:**

- [ ] Tonnen werden nie nur über die Farbe, sondern immer auch über Text bzw. Symbol unterschieden
- [ ] Texte passen sich der Schriftgröße des Systems an
- [ ] Bedienelemente sind für den Screenreader beschriftet

**Effort:**

**Priority:** Niedrig

---
*last change: 13.10.2026*

---
[← Übersicht]({{ '/' | relative_url }}) · [Pflichtenheft]({{ '/specification.html' | relative_url }}) · [Management]({{ '/management/' | relative_url }}) · [Architektur]({{ '/architecture/' | relative_url }})
