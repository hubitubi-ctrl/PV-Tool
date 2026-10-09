# PV Beschaffungsassistent

Ein statischer Web-Prototyp für projektbezogene Material-Leistungsverzeichnisse. Für lokale Nutzung ist kein Build-Schritt nötig; die App ist für GitHub Pages vorbereitet.

## Start

`index.html` im Browser öffnen. Projektangaben, Produktkatalog und Entwürfe bleiben lokal in diesem Browser gespeichert.

## Funktionen

- Projektangaben für Dachart, Fläche, Ausrichtung und Ziel-Leistung
- Neutrale Materialanforderungen für Module, Unterkonstruktion, Wechselrichter, Optimierer, Kabel, Überspannungsschutz sowie Erdung/Blitzschutz
- Lieferantenprodukte manuell erfassen oder per CSV importieren
- Produkte technischen Anforderungen zuordnen und Links im LV referenzieren
- Materialpositionen ergänzen; Mengen als offen, bekannt oder prüfpflichtig kennzeichnen
- Excel-kompatibles CSV-LV mit leeren Preisfeldern für Anbieter exportieren

## Katalog-CSV

Spaltenüberschriften: `Produktname`/`name`, `Lieferant`/`supplier`, `Kategorie`/`category`, `Artikelnummer`/`sku`, `Einheit`/`unit`, `Leistung Wp`/`powerWp`, `Beschreibung`/`description`, `Produktlink`/`url`. Semikolon oder Komma werden als Trennzeichen erkannt.

## GitHub Pages

GitHub Pages muss im Repository unter **Settings → Pages** als Build-Quelle **GitHub Actions** aktiviert sein. Danach den Workflow **Publish PV Beschaffungsassistent** im Tab **Actions** manuell starten. Die App wird damit als Pages-Site veröffentlicht.

## Grenzen des Prototyps

Die eingebauten Einträge sind neutrale technische Anforderungen, keine bestätigten Shopartikel. Die App ruft keine Preise, Lagerbestände oder Shopseiten automatisch ab. Shopdaten werden vorerst via CSV oder manuell eingebunden; automatische Katalogfeeds benötigen eine freigegebene Lieferantenschnittstelle.

Die Modulzahl wird als Richtwert aus Ziel-kWp und Wp pro Modul berechnet und als prüfpflichtig markiert. Unterkonstruktion, Ballastierung, Kabel, Stringaufteilung und Schutzkomponenten müssen projektspezifisch ausgelegt werden. Vor dem Versand sind Produktwahl, Mengen und Anforderungen fachlich zu prüfen.