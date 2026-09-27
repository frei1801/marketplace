# KNOWLEDGE_Tech_Architektur.md
 
**Version:** v0.6 · **Stand:** 27.09.2026
**Zuständig für:** Framework-Entscheidung, Service Provider (z. B. Zahlung), Grobarchitektur, Datenmodell, laufende Kosten der Technik, technische Schulden
**Verbindlich lesen vor:** jeder Tech-, Tool- oder Provider-Empfehlung, jeder Kostenfrage zur Technik, jedem Code-/Prototyp-Artefakt
**Nicht zuständig (→ Verweis):** regulatorische Anforderungen an Zahlung/Daten → KNOWLEDGE_Recht_Haftung.md · Gesamtkostenstruktur → KNOWLEDGE_Geschaeftsmodell.md · Status von Annahmen → KNOWLEDGE_Hypothesen_Entscheidungen.md
**Statuslegende:** [Hypothese] · [Signal] · [Validiert] · [Entschieden] – Definition in KNOWLEDGE_Projektregeln.md
 
> **Leitplanke:** Solange die Kernhypothesen (H1–H4 im Hypothesen-Log) nicht mindestens [Signal] sind, hier nur Grobarchitektur und Kostenrahmen – keine Detailplanung.
 
---
 
## 1. Rahmenbedingungen (lt. Projektanweisung)
- Niedrige laufende Kosten sind harte Rahmenbedingung
- Voraussichtlicher Ansatz: bestehendes Framework + Eigenentwicklung (ggf. KI-gestützt) + Anbindung eines Service Providers – **Entscheidung offen**
## 2. Framework-Entscheidung
| Option | Fixkosten/Monat | Transaktionskosten | Vorteile | Nachteile | Status |
|---|---|---|---|---|---|
| – | – | – | – | – | leer |
 
## 3. Service Provider
| Zweck | Anbieter | Fixkosten/Monat | Transaktionskosten | Status |
|---|---|---|---|---|
| Zahlung | Payment-Service-Provider für Split-Payment (Anbieter offen) | zu beziffern | nutzungsabhängig | [Hypothese] – Mechanik entschieden (Split-Payment, → KNOWLEDGE_Recht_Haftung.md Abschnitt 5), konkreter Anbieter noch offen |
| Hosting (Staging/Live) | Google Cloud oder Hetzner – Auswahl **bewusst vertagt** (Funnel tc1, 26.09.2026) bis Prototyp und echte Lastdaten vorliegen | zu beziffern (Hetzner: planbare Fixkosten; Google Cloud: nutzungsbasiert, Free-Tier) | – | [Hypothese] |
| CI/CD | GitHub Actions | 0 € im Free-Kontingent für private Repos (Umfang vor Kalkulation prüfen) | Build-Minuten über Kontingent | [Hypothese] |
| KI-gestützte Entwicklung | Claude Code, als VS-Code-Erweiterung (Franzi arbeitet bereits in VS Code mit vielen Erweiterungen; Review findet dort statt). Abo vs. API-Nutzung **bewusst vertagt** (Funnel tc3, 26.09.2026) bis Entwicklung konkret losgeht | zu beziffern (aktuelle Preise prüfen: claude.com/pricing) | bei API nutzungsabhängig | [Hypothese] |
| KI-gestützte Entwicklung, Alternative/Ergänzung | GitHub Copilot – nicht gewählt, da für Vervollständigung statt mehrstufige Aufgaben optimiert (Chat, 27.09.2026). Kill-Switch: falls Franzi nach 2–3 Wochen Inline-Vervollständigung oder IDE-Agent-Modus vermisst, Copilot Pro ergänzend prüfen | Copilot Pro 10 $/Monat; Pro+ 39 $/Monat; Business 19 $/Nutzer/Monat (Stand: DevToolsReview, Layer3Labs, abgerufen 27.09.2026) | im Preis enthalten bis Fair-Use-Grenze | [Hypothese] – nicht gewählt |
 
## 4. Grobarchitektur
- Entwicklung lokal auf eigenem Rechner, Datenbank zunächst ebenfalls lokal – ggf. in Docker (Docker Compose), mit derselben Datenbank und Version wie später in der Cloud [Hypothese]
- Keine Cloud-Entwicklungsumgebung für den Prototyp (laufende Kosten ohne Mehrwert bei einer Entwicklerin) [Hypothese]
- Cloud erst für Staging/Live; Anbieter Google Cloud oder Hetzner [Hypothese]. Auswahlkriterien: Fixkosten vs. nutzungsbasierte Abrechnung, eigener Betriebsaufwand, Datenstandort (→ KNOWLEDGE_Recht_Haftung.md, Abschnitt 7 – Fachprüfung nötig)
- Build- und Deploy-Pipeline über GitHub Actions, damit jeder Build identisch aufgebaut wird [Hypothese]
- Architektur-Hinweis: Entwicklungsrechner (Mac, ARM) ≠ übliche Cloud-Server (x86). Container-Images in der Pipeline für die Zielplattform bauen oder ARM-Server wählen; vor dem ersten Deployment festlegen [Hypothese] – **bewusst noch offengelassen** (Funnel tc2, 26.09.2026)
## 5. Datenmodell
- **leer** (erst nach Validierung der Kernhypothesen)
## 6. Laufende Kosten gesamt
| Posten | Fix/Monat | Variabel/Transaktion | Günstigere Alternative | Status |
|---|---|---|---|---|
| Summe Tech | noch nicht bezifferbar – Posten siehe Abschnitt 3 | – | – | offen |
 
### 6b. Einmalkosten Technik
| Posten | Betrag | Quelle, Datum | Status |
|---|---|---|---|
| Entwicklungsrechner: MacBook Air 13" (M5), 24 GB RAM, 512 GB SSD. Laptop statt Desktop (mobiles Arbeiten gewünscht, Franzi, 26.09.2026); 24 GB wegen möglicher Docker-Nutzung, RAM nicht nachrüstbar. Nicht MacBook Neo: nur ein externer Monitor nativ | Rahmen ca. 1.450–1.600 € (exakten Preis 24 GB/512 GB vor Kauf prüfen) | Referenz: MacBook Air 13" M5 ab 1.247 € (Geizhals, abgerufen 26.09.2026); 24 GB/1 TB ab 1.754 € (heise Preisvergleich, abgerufen 26.09.2026) | [Entschieden] |
| Vorhanden: 2 Monitore, Adapter, LAN | 0 € | Angabe Gründer, 26.09.2026 | – |
| Dock/Hub für 2 Monitore + LAN + Laden (MacBook Air hat nur 2 Thunderbolt-Ports, kein HDMI, kein Ethernet) – entfällt, falls vorhandener Adapter das abdeckt | ca. 50–250 € | Schätzung | [Entschieden] |
| Tastatur/Maus für den Schreibtisch (optional) | ca. 30–100 € | Schätzung | [Entschieden] |
 
> Freigabe der Anschaffung: **erteilt – jetzt kaufen** (Funnel gm11, 26.09.2026). Budget ist jetzt entschieden (1.000–5.000 € bis Validierung, → KNOWLEDGE_Geschaeftsmodell.md Abschnitt 1) und deckt den geschätzten Gesamtrahmen (ca. 1.530–1.950 €).
 
## 7. Technische Schulden (append-only)
> Format: Datum · Beschreibung · bewusst eingegangen weil · Rückbau wann
 
- *(noch keine Einträge)*
## 8. Produktdatenbank für Autovervollständigung
- Ziel: Beim Einstellen eines Geräts bekommen Verleiher Vorschläge (Titel, Kategorie, Kaution- und Preisrichtwert, Kurzbeschreibung) aus einer vorab recherchierten Datenbank, statt alles selbst einzutippen. [Hypothese]
- Recherche-Ansatz: **Claude Code / automatisierte Recherche-Pipeline** [Entschieden] (Funnel tc5, 26.09.2026) – Qualität stichprobenartig prüfen, kein Ersatz für eine Quellenprüfung
- Startumfang: **alle vier Kategorien vorab recherchieren** [Entschieden] (Funnel tc4, 26.09.2026) – **gegen Claudes ausdrückliche Empfehlung, mit einer Kategorie zu starten, bewusst entschieden.** Risiko explizit benannt und akzeptiert: der Kategorie-Fokus fürs Launch (eine vs. alle vier) ist weiterhin offen (→ KNOWLEDGE_Markt_Wettbewerb.md, Abschnitt 3 – Funnel-Frage mk5 wurde übersprungen), d. h. der Rechercheaufwand geht möglicherweise für Kategorien voraus, die nicht zuerst launchen. H1 (Verleiher-Bereitschaft) steht weiterhin auf [Hypothese], nicht [Signal]
- Datenmodell (grob, Details erst mit Abschnitt 5): Produktname, Kategorie, Kaution-Richtwert, Preis-Spanne/Tag, Kurzbeschreibung
- **Spannung mit der Leitplanke oben:** bleibt bestehen. Dies ist keine Auflösung der Spannung, sondern eine bewusst akzeptierte Ausnahme von den Gründern – siehe KNOWLEDGE_Hypothesen_Entscheidungen.md, Abschnitt 5, Eintrag E9
- Kosten: einmaliger Rechercheaufwand, noch nicht beziffert → KNOWLEDGE_Geschaeftsmodell.md, Abschnitt 5
---
 
## Changelog
| Datum | Version | Änderung | Angestoßen von |
|---|---|---|---|
| 26.09.2026 | v0.1 | Gerüst angelegt | David |
| 26.09.2026 | v0.2 | Hosting (Google Cloud/Hetzner), CI/CD (GitHub Actions), Claude Code als Service Provider ergänzt; Grobarchitektur (lokale Entwicklung, Docker, ARM/x86-Hinweis) ergänzt; Einmalkosten Hardware (Abschnitt 6b) ergänzt – alles [Hypothese] | Franzi |
| 26.09.2026 | v0.3 | Abschnitt 8 neu: Produktdatenbank für Autovervollständigung (Recherche-Ansatz Claude Code, Startumfang eine Kategorie, Spannung mit Validierung-vor-Bau-Leitplanke benannt) | David |
| 27.09.2026 | v0.4 | Aus Funnel-Antworten: Hosting- und Claude-Code-Preismodell-Entscheidung bewusst vertagt (Abschnitt 3); ARM/x86 bewusst offengelassen (Abschnitt 4); Freigabe Entwicklungsrechner erteilt, Status auf [Entschieden] (Abschnitt 6b); Abschnitt 8 aktualisiert: Startumfang „alle vier Kategorien" gegen Empfehlung entschieden, Risiko-Hinweis ergänzt, Verweis auf Markt_Wettbewerb korrigiert (Abschnitt 3 statt 4) | David & Franzi (Funnel) |
| 27.09.2026 | v0.5 | Abschnitt 3: Claude Code als VS-Code-Erweiterung präzisiert (Franzis bestehendes Setup); GitHub Copilot als geprüfte, nicht gewählte Alternative mit Kill-Switch und Preisen ergänzt | Franzi |
| 27.09.2026 | v0.6 | Statuslegende-Verweis im Kopf aktualisiert: zeigt jetzt auf die neue KNOWLEDGE_Projektregeln.md statt auf die Projektanweisung | David |
 
