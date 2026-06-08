# mandatsfeed.github.io

Weboberfläche für [mandatsfeed](https://github.com/mandatsfeed/mandatsfeed) — chronologische RSS-Feeds parlamentarischer Aktivität pro Abgeordneter und pro Fraktion im Bundestag und in deutschen Landtagen.

## Was diese Seite bietet

- **Hierarchischer Feed-Browser** — Parlament → Wahlperiode → Person/Fraktion
- **Volltext-Suche** über alle Namen und Fraktionen
- **Per-Person-Ansicht** mit chronologischer Aktivität (Reden, Anfragen, Anträge, Gesetzentwürfe, namentliche Abstimmungen)
- **Typ-Filter** pro Feed-Item-Kategorie
- **Mein Feed** — Personen oder Fraktionen sammeln und alle RSS-URLs auf einmal kopieren

Die Seite läuft vollständig im Browser, ohne Backend. Alle Daten kommen direkt aus dem [mandatsfeed](https://github.com/mandatsfeed/mandatsfeed)-Repository via GitHub Pages.

## Architektur

- Eine einzige `index.html` (HTML + CSS + JS), keine Build-Schritte
- Lädt `./mandatsfeed/metadata.json` (Index aller abonnierbaren Feeds)
- Lädt RSS-Feeds on-demand und rendert sie als chronologische Liste
- Symlink `mandatsfeed/` → `../mandatsfeed/wiki/` (lokal); auf GitHub Pages liegen die Daten unter dem gleichen Pfad direkt im Repo

## Lizenz

MIT — © [DracoBlue](https://github.com/DracoBlue)

Die indexierten Inhalte (Drucksachen, Reden, Abstimmungs-Daten) stehen unter [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.de) und verbleiben im Urheberrecht der jeweiligen Parlamente. Siehe [mandatsfeed/mandatsfeed](https://github.com/mandatsfeed/mandatsfeed) für Details.
