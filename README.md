# PV Beschaffungsassistent

Ein statischer Web-Prototyp für projektbezogene Material-Leistungsverzeichnisse. Für lokale Nutzung ist kein Build-Schritt nötig; die App ist für GitHub Pages vorbereitet.

## Start

`index.html` im Browser öffnen. Projektangaben, Produktkatalog und Entwürfe bleiben lokal in diesem Browser gespeichert.

## Funktionen

- Projektangaben für Dachart, Fläche, Ausrichtung und Ziel-Leistung
- Dachplan als PNG/JPG/WebP laden, Massstab anhand einer bekannten Strecke kalibrieren und nutzbare Fläche per Klick markieren
- Hindernisflächen abziehen, Modulformat und Abstände einstellen sowie erste geometrische Modulbelegung berechnen
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

Die Modulzahl aus dem Dachplan ist eine geometrische Vorplanung auf Basis des markierten Polygons, Kalibrierung, Modulmass und Rasterabstand. Randabstände, Dachaufbauten, Brandschutzwege, Statik sowie Wind-/Schneelasten sind nicht automatisch geprüft. PDF-Pläne müssen vorerst als PNG/JPG/WebP exportiert werden. Die Resultate sind prüfpflichtig. Unterkonstruktion, Ballastierung, Kabel, Stringaufteilung und Schutzkomponenten müssen projektspezifisch ausgelegt werden. Vor dem Versand sind Produktwahl, Mengen und Anforderungen fachlich zu prüfen.