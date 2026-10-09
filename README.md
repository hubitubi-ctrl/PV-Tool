# PV-Ausschreibungsassistent

Statische Webanwendung für Dachplanaufnahme, Mengen-Vorplanung und Erstellung eines bearbeitbaren PV-Leistungsverzeichnisses. Die Website läuft über GitHub Pages und benötigt keinen Server.

## Start

Öffne die GitHub-Pages-Website oder starte `index.html` lokal. Auf der ersten Seite gibt es nur **Plan hinzufügen** und **Bestehendes Projekt laden**.

## Ablauf

1. Dachplan als Bild oder PDF laden. Nach jedem Plan-Upload muss der Massstab über eine bekannte Strecke neu kalibriert werden. Die Planansicht ist zoombar.
2. Dachbereiche markieren: Arbeitsfläche, PV-Fläche, Sperrzone, dauerhafte Absturzsicherung, Anschlagpunkte, provisorische Sicherung sowie sicherer Zugang. Pro PV-Fläche werden Montageart und Modulausrichtung erfasst. Montagelattung bei Indach kann separat ausgewiesen werden.
3. Produkte und Lieferanten manuell oder via CSV-Katalog erfassen; Modulmasse und Nennleistung steuern ein geometrisches Belegungsraster. Gleichwertige Alternativen bleiben für die Ausschreibung möglich.
4. LV aus Vorlagenkapiteln erzeugen. Planbezogene Mengen, Produktreferenzen und generische Fachpositionen können ergänzt werden. Jeder Beschreibungstext und jede projektspezifische Spezifikation ist bearbeitbar. Export als Excel-kompatible CSV, ohne Produktpreise.

## Projektdatei und Shopkatalog

Plan und Eingaben bleiben standardmässig im Browser. Mit **Projektdatei speichern** wird eine `.pvprojekt`-Datei erzeugt; diese kann auf einem anderen Gerät über **Bestehendes Projekt laden** geöffnet werden. Eine Shop-Schnittstelle muss einen autorisierten Produktdatenfeed oder CSV-Export bereitstellen. Die App liest Shopseiten nicht automatisch aus.

Die Katalog-CSV verwendet die Spalten: Produktname, Lieferant, Kategorie, Artikelnummer, Einheit, Leistung Wp, Breite mm, Höhe mm, Beschreibung, Produktlink. Eine leere Importvorlage lässt sich herunterladen.

## Struktur des Leistungsverzeichnisses

Die Kapitel A–H decken Projektbedingungen, Dacharbeiten/Montagegrund, PV-Generator und Unterkonstruktion, Elektroinstallation/Schutz, Absturzsicherung/Zugang, Planung/Nachweise, Inbetriebnahme/Dokumentation und Optionen ab. Diese Struktur wurde aus sechs bereitgestellten PV-Leistungsverzeichnissen zusammengeführt und für die Anwendung vereinheitlicht. Sie ist kein normverbindlicher NPK-Text und beansprucht keine automatische Normkonformität.

## Fachliche Grenzen

Das Modulraster ist eine geometrische Vorplanung innerhalb des markierten PV-Polygons; es prüft nur die Mittelpunkte gegen Sperrzonen. Dachkanten, Abstände, Modulzwischenräume im System, Brandschutzwege, Verschattung, Statik, Wind-/Schneelasten, Stringplanung, Schutzkonzept und Montagevorschriften sind fachlich zu verifizieren. Mengen sind als Vorschlag oder offen gekennzeichnet. Die App ist nicht für die Ausführungsplanung freigegeben. PDF-Anzeige lädt PDF.js von jsDelivr und benötigt eine Internetverbindung. Standort in Google Maps öffnen ist eine freiwillige externe Suche nach dem eingetragenen Ort.

## GitHub Pages

Repository: `hubitubi-ctrl/PV-Tool`. Der `main`-Branch veröffentlicht über `.github/workflows/pages.yml`.
