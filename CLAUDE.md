# Aureon Website (aureon-trading.com)

Statische Seite ohne Build-Schritt. Betreiber: Dennis Meier, Aureon Trading and Consulting L.L.C-FZ, Dubai.
Hosting: Netlify, Veröffentlichungsordner ist `site/` (siehe `netlify.toml`).

## Struktur
- `site/de/index.html` und `site/en/index.html`: komplette Startseite je Sprache, HTML, CSS und JS in einer Datei.
- `site/de/` und `site/en/` enthalten außerdem Impressum und Datenschutz (`impressum.html`, `datenschutz.html`, `legal-notice.html`, `privacy.html`) sowie `3d.html` (alte Three.js Version, nicht gepflegt).
- `site/downloads/`: zwei PDFs (Lieferantenqualität DE und EN), per Link von der Quality-Sektion.
- `site/_redirects`: Sprachweiche per Land (DE, AT, CH, LI nach /de/, sonst /en/).
- `site/vendor/three.min.js` wird nur von `3d.html` genutzt.

## Regeln für jede Änderung
1. DE und EN immer parallel ändern, gleiche Struktur, gleiche Klassen.
2. Keine Gedankenstriche (weder lang noch kurz) in Texten. Stattdessen Komma, Doppelpunkt, Punkt oder "·".
3. Keine erfundenen Zahlen, Referenzen oder Kundennamen auf der Seite.
4. Neue Abschnitte mit eigenem Klassenpräfix anlegen (Beispiele: `.qual-*`, `.cab-*`, `.book*`, `.dclose`), CSS vor `</style>`.
5. Nach jeder Änderung Desktop (1440 px) und Handy (390 px) prüfen: kein horizontaler Überlauf, keine abgeschnittenen Zahlen (bei Farbverlauf-Text `background-clip:text` genug Padding geben).
6. Lokal testen: `cd site && python3 -m http.server 8000`, dann `/de/` und `/en/` öffnen.

## Design
- Dunkel mit Gold, Industrial Luxury. Tokens in `:root`: `--void --graphite --carbon --steel --chalk --paper`, `--gold-1..4`, `--brand-grad`.
- Schriften: Newsreader (`--disp`), Archivo (`--grot`), Martian Mono (`--mono`), per Google Fonts.
- Themenklassen je Sektion: `.t-void .t-graph .t-paper .t-paper2`. Einblend-Animation: `.rv` und `.rv.in`.

## Seitenaufbau (Reihenfolge)
Hero (Netzwerkkarte mit Dubai im Zentrum, Canvas `#form`) → Intersection → Evidence → Division 01 Digital (`#digital`: KI-Pitch, drei Wege, Kooperation mit The Cabinet, Technik, Schlusssatz) → Division 02 Strategy/Advisory (`#advisory`) → Quality (`#quality`, mit Strategic Partnership AUREON + SQPS) → Mandates → Division 03 Industry (`#industry`) → Division 04 Network (`#network`) → Contact (mit Buchungsblock `#book`, Calendly) → Footer.

## Inhalte, die stimmen müssen
- AUREON: Strategic Procurement & Business Development, 17 Jahre. SQPS (Patrick Siebel): Quality & Process Solutions, 19 Jahre Automotive.
- Network: Lieferanten EU · ASIA, Kunden DACH · USA, Base DUBAI.
- Kontakt: info@aureon-trading.com. Calendly: https://calendly.com/d-meier-aureon-trading/30min (wird erst per Klick als iframe geladen, aus Datenschutzgründen).
- The Cabinet (thecabinet.biz) ist ein unabhängiger Kooperationspartner, Marke nennen mit ™, kein Link auf der Seite.

## Offene Punkte
- Calendly Eventname dort ist "60 Minute Meeting", Link endet auf 30min: Dauer klären, dann ggf. im Text nennen.
- Impressum: USt-ID und Registerdaten fehlen. Rechtstexte juristisch prüfen lassen (inkl. Calendly Abschnitt, EU-Vertreter nach Art. 27 DSGVO).
- Google Fonts lokal hosten, um die Datenschutzerklärung zu vereinfachen.
- Deutsche Version des KOPL Vertrags liegt nicht vor (separates Projekt).
