# PV Beschaffungsassistent

Ein statischer Web-Prototyp für projektbezogene Material-Leistungsverzeichnisse. Für lokale Nutzung ist kein Build-Schritt nötig; die App ist für GitHub Pages vorbereitet.

## Start

`index.html` im Browser öffnen. Projektangaben, Produktkatalog und Entwürfe bleiben lokal in diesem Browser gespeichert.

## Funktionen

- Projektangaben für Dachart, Fläche, Ausrichtung und Ziel-Leistung
- Dachplan als PDF oder Bild laden; Massstab über eine eigene Schaltfläche in einer zoombaren Planansicht kalibrieren und Fläche/Hindernisse dort markieren
- Himmelsrichtung, Standortkoordinaten, Dachneigung und Systemverluste für eine vorläufige PVGIS-Jahresprognose übergeben; Ost-West wird mit zwei getrennten Halb-Leistungs-Abfragen abgebildet
- Hindernisflächen abziehen, Modulformat (gängige Abmessungen oder benutzerdefiniert) und Abstände einstellen sowie die bessere Portrait-/Landscape-Belegung vergleichen
- Modulanzahl, Modul-Belegungsfläche und bearbeitete Dachfläche als prüfpflichtige Positionen ins LV übernehmen
- Neutrale Materialanforderungen für Module, Unterkonstruktion, Wechselrichter, Optimierer, Kabel, Überspannungsschutz sowie Erdung/Blitzschutz
- Lieferantenprodukte manuell erfassen oder per CSV importieren
- Produkte technischen Anforderungen zuordnen und Links im LV referenzieren
- Materialpositionen ergänzen; Mengen als offen, bekannt oder prüfpflichtig kennzeichnen
- Excel-kompatibles CSV-LV mit leeren Preisfeldern für Anbieter exportieren

## Katalog-CSV

Spaltenüberschriften: `Produktname`/`name`, `Lieferant`/`supplier`, `Kategorie`/`category`, `Artikelnummer`/`sku`, `Einheit`/`unit`, `Leistung Wp`/`powerWp`, `Beschreibung`/`description`, `Produktlink`/`url`. Semikolon oder Komma werden als Trennzeichen erkannt.

## GitHub Pages

GitHub Pages muss im Repository unter **Settings → Pages** als Build-Quelle **GitHub Actions** aktiviert sein. Danach wird die Website bei Änderungen am Branch `main` automatisch veröffentlicht. Ein manueller Start ist weiterhin im Tab **Actions** möglich.

## Grenzen des Prototyps

Die eingebauten Einträge sind neutrale technische Anforderungen, keine bestätigten Shopartikel. Die App ruft keine Preise, Lagerbestände oder Shopseiten automatisch ab. Shopdaten werden vorerst via CSV oder manuell eingebunden; automatische Katalogfeeds benötigen eine freigegebene Lieferantenschnittstelle.

Die Modulzahl aus dem Dachplan ist eine geometrische Vorplanung auf Basis des markierten Polygons, Kalibrierung, Modulmass und Rasterabstand. Randabstände, Dachaufbauten, Brandschutzwege, Statik sowie Wind-/Schneelasten sind nicht automatisch geprüft. PDF-Anzeige verwendet PDF.js und benötigt beim Öffnen eine Internetverbindung; die Plandatei selbst bleibt lokal im Browser. Für die PVGIS-Prognose öffnet sich der offizielle JRC-Dienst in einem neuen Tab; PVGIS erlaubt keine AJAX-Aufrufe direkt aus dem Browser. Die Jahresproduktion ist im Ergebnis unter `E_y` ausgewiesen. Für Ost-West muss der Wert der beiden Halb-Leistungs-Abfragen addiert werden. Die Resultate sind prüfpflichtig. Unterkonstruktion, Ballastierung, Kabel, Stringaufteilung und Schutzkomponenten müssen projektspezifisch ausgelegt werden. Vor dem Versand sind Produktwahl, Mengen und Anforderungen fachlich zu prüfen.