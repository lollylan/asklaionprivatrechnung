# Privatrechnung – Hausärztliche Liquidation nach GOÄ

Eine clientseitige Single-Page-Webanwendung zur strukturierten Erstellung von
Privatrechnungen nach der Gebührenordnung für Ärzte (GOÄ).

> **Hinweis:** Diese Anwendung ist eine technische Demonstration zu Forschungs-
> und Bildungszwecken und **nicht für den produktiven Einsatz an realen
> Patientinnen und Patienten** bestimmt. Siehe Disclaimer in der App.

## Funktionen

- **Tagesweise Erfassung** mehrerer Behandlungstage mit beliebig vielen
  Sitzungen / Besuchen pro Tag (jeweils mit eigener Uhrzeit).
- **GOÄ-Ziffernkatalog** mit hinterlegten Einfachsätzen und üblichen
  Steigerungsfaktoren (1,0 / 1,8 / 2,3 / 3,5).
- **Konflikt-Detektion** pro Sitzung: Ziffern, die sich nach GOÄ
  gegenseitig ausschließen (z. B. 1/3/34, 5/6/7/8, 50/51), werden
  automatisch markiert. Implizite Ausschlüsse (z. B. „Nr. 50 enthält
  bereits Beratung und symptombezogene Untersuchung") werden ebenfalls
  geprüft.
- **A4-Rechnungsvorschau** mit klassischem Briefkopf, Adressblock,
  Leistungstabelle und Bankverbindung.
- **PDF-Export** über den integrierten Druckdialog des Browsers.
- **Lokale Speicherung** der Praxis-Stammdaten und Bankverbindung im
  `localStorage` – Patienten- und Leistungsdaten werden bewusst **nicht**
  persistiert.
- **Keine externen Abhängigkeiten**, kein Tracking, kein Build-Step.

## Verwendung

Datei [`privatrechnung.html`](privatrechnung.html) im Browser öffnen –
das ist alles. Praxis- und Bankdaten links eingeben, Behandlungstage
hinzufügen, GOÄ-Ziffern anhaken, Faktor wählen, fertig. Über den Button
„PDF exportieren" gelangt man in den Druckdialog des Browsers.

> **Tipp für den Druck:** Im Druckdialog unter „Weitere Einstellungen"
> die Option **„Kopf- und Fußzeilen" deaktivieren**, damit Datum und
> Dateipfad nicht auf der Rechnung erscheinen.

## Technik

- Reines HTML / CSS / Vanilla JavaScript in einer einzigen Datei.
- Keine Build-Tools, keine Frameworks, keine externen CDNs.
- Funktioniert vollständig offline.

## Datenschutz

Die Anwendung verarbeitet sämtliche Daten **ausschließlich lokal im Browser**.
Es findet keine Übermittlung an einen Server statt. Details siehe
Datenschutzerklärung in der App.

## Lizenz

[MIT](LICENSE) © 2026 Florian Rasche
