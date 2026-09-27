# KNOWLEDGE_Hypothesen_Entscheidungen.md
 
**Version:** v0.5 · **Stand:** 27.09.2026
**Zuständig für:** Status jeder Annahme (Hypothesen-Log) und jede Gründerentscheidung (Entscheidungslog)
**Verbindlich lesen vor:** jeder Aussage, ob etwas belegt oder entschieden ist, jedem Plan, jedem Kill-Switch, jeder Statusänderung in einer anderen Wissensdatei
**Nicht zuständig (→ Verweis):** Inhalte der Hypothesen stehen in der jeweils thematisch zuständigen Datei; hier nur Status, Test und Verlauf
**Statuslegende:** [Hypothese] · [Signal] · [Validiert] · [Entschieden] · zusätzlich [Verworfen]
 
> **Beide Logs sind append-only.** Statusänderungen werden als neue Zeile im Verlauf ergänzt, nie überschrieben.
 
---
 
## 1. Kernhypothesen (lt. Projektanweisung)
 
| ID | Hypothese | Aktueller Status | Wie testen? | Erfolgskriterium | Zuständige Datei |
|---|---|---|---|---|---|
| H1 | Privatpersonen in Berlin sind bereit, selten genutzte Gegenstände gegen Geld zu verleihen (Verleiher-Bereitschaft) | [Hypothese] | Alle Listings zählen unabhängig von der Beziehung zum Verleiher (Eigenlistings der Gründer, Freunde/Bekannte, Fremde gleichgestellt) [Entschieden, Chat 27.09.2026 – gegen Claudes Empfehlung] | Kein numerischer Schwellenwert – Bewertung nach Gefühl [Entschieden, Chat 27.09.2026 – gegen Claudes Empfehlung] | Markt_Wettbewerb |
| H2 | Es gibt in Berlin ausreichend Nachfrage nach Leihe statt Kauf | [Hypothese] | offen | offen | Markt_Wettbewerb |
| H3 | Mieter zahlen einen Preis, der Verleiher und Plattformgebühr trägt (Zahlungsbereitschaft) | [Hypothese] | offen | offen | Geschaeftsmodell |
| H4 | Das Vertrauensproblem bei Schaden/Verlust/Nicht-Rückgabe ist so lösbar, dass beide Seiten mitmachen | [Hypothese] | offen | offen | Recht_Haftung |
 
> Hinweis: Die Funnel-Runde vom 26.09.2026 hat viele Gründerentscheidungen getroffen (siehe Abschnitt 5), aber keine dieser vier Kernhypothesen bewegt – das sind Entscheidungen der Gründer, keine Marktevidenz. H1–H4 bleiben [Hypothese].
 
> **Risiko-Hinweis zu H1 (bewusst in Kauf genommen, nicht aufgelöst):** Die Test-Methode für H1 zählt Eigenlistings der Gründer und Gefälligkeits-Listings von Freunden/Bekannten als gleichwertigen Beleg wie fremde, unabhängige Verleiher – und verzichtet auf eine feste Zahl/Frist als Erfolgskriterium. Claude hat davor gewarnt, dass der an H1 gekoppelte Kill-Switch (→ KNOWLEDGE_Geschaeftsmodell.md, Abschnitt 6) dadurch faktisch nicht mehr objektiv auswertbar ist: nahezu jedes Ergebnis lässt sich als „Signal" werten, da kein unabhängiger Maßstab und kein Schwellenwert existieren. David & Franzi haben sich bewusst gegen eine strengere Definition entschieden (Chat, 27.09.2026).
 
## 2. Weitere Hypothesen (append-only)
> Format: ID · Hypothese · Status · Test · Erfolgskriterium · zuständige Datei
 
- *(noch keine Einträge)*
## 3. Statusverlauf (append-only)
> Format: Datum · ID · alter Status → neuer Status · Evidenz (Quelle, Stichprobe) · angestoßen von
 
- 26.09.2026 · H1–H4 · angelegt als [Hypothese] · Quelle: Projektanweisung v1.0 · David
## 4. Ausstehende Gründerentscheidungen
> Gründerentscheidung – mit Partner:in abstimmen. Nach Beschluss in Abschnitt 5 eintragen.
 
- Tech-Grundansatz (→ KNOWLEDGE_Tech_Architektur.md, Abschnitt 1): weiterhin offen. Hosting, ARM/x86-Zielplattform und Claude-Code-Preismodell wurden im Funnel bewusst vertagt (26.09.2026), nicht entschieden
- Zeitpunkt Fachprüfung „Vermittler vs. Vertragspartner" (→ KNOWLEDGE_Recht_Haftung.md, Abschnitt 4): spätestens vor dem ersten echten Zahlungsfluss im Split-Payment-Flow – Trigger vorgeschlagen von Claude, bestätigt von David am 26.09.2026. Im Funnel (Frage rl5) erneut nicht bestätigt (übersprungen) – **weiterhin nicht mit Franzi abgestimmt**
- Kategorie-Fokus beim Launch (eine Kategorie vs. alle vier) (→ KNOWLEDGE_Markt_Wettbewerb.md, Abschnitt 3): im Funnel übersprungen (Frage mk5), weiterhin offen – steht im Spannungsfeld mit der bereits entschiedenen Produktdatenbank-Recherche für alle vier Kategorien (siehe Abschnitt 5, E9)
- Konkrete Warenwert-Schwelle für Schutzgebühr, Kaution-Staffelung und Verifizierungsstufe (→ KNOWLEDGE_Geschaeftsmodell.md Abschnitt 2, KNOWLEDGE_Recht_Haftung.md Abschnitte 2 und 10): drei Mechanismen hängen an derselben noch unbezifferten Zahl
- Rolle der Plattform: Vermittler vs. Vertragspartner (→ KNOWLEDGE_Recht_Haftung.md, Abschnitt 4): weiterhin offen, Fachprüfung noch nicht erfolgt
- Konkrete Aufteilung des 1.000–5.000-€-Budgets zwischen Marketing und Tech (→ KNOWLEDGE_Geschaeftsmodell.md, Abschnitt 5): Marketing läuft aus demselben Rahmen wie die Hardware, die bereits ca. 1.530–1.950 € bindet – offen, wie viel real für Marketing übrig bleibt
## 5. Entscheidungslog (append-only)
> Format: E-Nr. · Datum · Entscheidung · Begründung · verworfene Alternativen · beschlossen von (beide) · betroffene Dateien
 
- E1 · 26.09.2026 · Gebührenmodell: Provision zahlen beide Seiten, Richtung niedrig halten (5–10 %), Boost-Funktion zeitlich befristet, kein Abo-Modell, Schutzgebühr nur bei höherwertigen Gegenständen · Begründung: Wachstum vor Marge in der Testphase · verworfene Alternativen: nur Verleiher/nur Mieter zahlt, dauerhaftes Featured-Badge, Freemium mit Listing-Limit · beschlossen von: David & Franzi (Funnel) · betroffene Dateien: Geschaeftsmodell §2
- E2 · 26.09.2026 · Preislogik: Verleiher setzt den Mietpreis frei · Begründung: volle Kontrolle beim Verleiher · verworfene Alternativen: Plattform gibt Preisspanne vor, datenbasierte Empfehlung · beschlossen von: David & Franzi (Funnel) · betroffene Dateien: Geschaeftsmodell §3
- E3 · 26.09.2026 · Ambition & Budget: Experiment, 5–10 Std./Woche je Gründer, 1.000–5.000 € bis Validierung, 6 Monate bis Go/No-Go; Kill-Switch: Abbruch/Neubewertung nach 6 Monaten, wenn H1 nicht mindestens [Signal] · Begründung: begrenzter, ehrlicher Testrahmen; Kill-Switch-Kriterium von Claude vorgeschlagen, keine abweichende Präferenz genannt · verworfene Alternativen: Nebenprojekt, ernsthafte Gründung, größere Zeit-/Geldbudgets, kein festes Datum · beschlossen von: David & Franzi (Funnel) · betroffene Dateien: Geschaeftsmodell §1, §6
- E4 · 26.09.2026 · Zahlungsfluss: Split-Payment über PSP, Auszahlung an Verleiher erst nach Rückgabe ohne Meldung · Begründung: kein eigener Zugriff auf Kundengelder, Schutz vor Vorauszahlung bei Problemfällen · verworfene Alternativen: Plattform als Zahlungsmittler, Direktzahlung außerhalb der Plattform, sofortige Auszahlung, gestaffelte Auszahlung · beschlossen von: David & Franzi (Funnel) · betroffene Dateien: Recht_Haftung §5
- E5 · 26.09.2026 · Kaution (klassisch) statt Versicherung · Begründung: einfacher umzusetzen · verworfene Alternativen: Versicherung statt Kaution, Hybrid nach Warenwert · beschlossen von: David & Franzi (Funnel) · betroffene Dateien: Recht_Haftung §2
- E6 · 26.09.2026 · Schadensfall-Logik: automatische Nachbelastung der Kaution bei Nicht-Rückgabe; Streitentscheidung per Vorher-/Nachher-Fotos, Plattform entscheidet · Begründung: skalierbar, planbar, wenig manueller Aufwand · verworfene Alternativen: manuelle Einzelfallprüfung, neutraler Gutachter, einseitige Verleiher-Entscheidung, Klärung unter Nutzern · beschlossen von: David & Franzi (Funnel) · betroffene Dateien: Recht_Haftung §1
- E7 · 26.09.2026 · Launch-Strategie: ein bis zwei Kieze fokussiert, erst Verleiher gewinnen, nur Selbstabholung, beidseitiges Bewertungssystem · Begründung: passt zur eigenen Leitplanke „lokale Dichte", üblicher Marktplatz-Weg beim Henne-Ei-Problem · verworfene Alternativen: ganz Berlin/Berlin+Potsdam, erst Nachfrage testen, optionaler Lieferservice, einseitiges oder kein Bewertungssystem · beschlossen von: David & Franzi (Funnel) · betroffene Dateien: Markt_Wettbewerb §2, §4
- E8 · 26.09.2026 · Entwicklungsrechner-Freigabe: jetzt kaufen · Begründung: Budget (1.000–5.000 €) ist jetzt entschieden und deckt den geschätzten Rahmen · verworfene Alternativen: erst nach erstem Nutzer-Signal warten · beschlossen von: David & Franzi (Funnel) · betroffene Dateien: Tech_Architektur §6b
- E9 · 26.09.2026 · Produktdatenbank-Umfang: alle vier Kategorien vorab recherchieren (statt einer Kategorie), Recherche-Ansatz Claude Code / automatisierte Pipeline · Begründung: von den Gründern nicht ausführlich begründet · **Risiko-Hinweis (bewusst in Kauf genommen, nicht aufgelöst):** widerspricht der Leitplanke „Validierung vor Bau", solange H1 auf [Hypothese] steht, und wurde getroffen, während die Kategorie-Fokus-Frage fürs Launch (mk5) offen blieb – Claude hat vor dieser Reihenfolge ausdrücklich gewarnt, die Gründer haben sich bewusst dagegen entschieden, den Umfang zu reduzieren · verworfene Alternativen: eine Kategorie (Claudes Empfehlung), zwei Kategorien als Kompromiss · beschlossen von: David & Franzi (Funnel, gegen Empfehlung) · betroffene Dateien: Tech_Architektur §8, Markt_Wettbewerb §3
- E10 · 27.09.2026 · Verifizierungsmethode: gestaffelt nach Warenwert – 1-Cent-Testüberweisung als Basis-Check für alle, automatischer Dokumenten-Abgleich zusätzlich ab einer noch zu beziffernden Warenwert-Schwelle · Begründung: kombiniert niedrige Einstiegshürde mit echtem Schutz bei höherem Risiko, nach ausführlicher Gegenüberstellung der beiden im Funnel gegebenen, sich widersprechenden Antworten (rl4 vs. rl8) · verworfene Alternativen: nur Testüberweisung, nur Dokumenten-Abgleich für alle · beschlossen von: David & Franzi (Chat, nach Funnel) · betroffene Dateien: Recht_Haftung §10
- E11 · 27.09.2026 · H1-Testmethode & Erfolgskriterium: alle Listings zählen unabhängig von der Beziehung zum Verleiher (Eigenlistings der Gründer, Freunde/Bekannte, Fremde gleichgestellt); kein numerischer Schwellenwert, Bewertung nach Gefühl · Begründung: von den Gründern nicht ausführlich begründet (Akquise-Reihenfolge: erst Eigenlistings, dann Freunde/Bekannte, optional bezahltes Marketing – „stimmiges Produkt" statt Interviews) · **Risiko-Hinweis (bewusst in Kauf genommen, nicht aufgelöst):** entwertet faktisch den an H1 gekoppelten 6-Monats-Kill-Switch (→ Geschaeftsmodell §6), da kein unabhängiger Maßstab und keine feste Schwelle existieren – Claude hat vor dieser Kombination ausdrücklich gewarnt · verworfene Alternativen: nur unabhängige Fremde ohne persönliche Bindung zählen (Claudes Empfehlung), feste Zahl + Frist festlegen (Claudes Empfehlung) · beschlossen von: David & Franzi (Chat, Franzi-Antwort 27.09.2026, David-Bestätigung 27.09.2026) · betroffene Dateien: Hypothesen_Entscheidungen §1, Markt_Wettbewerb §4
---
 
## Changelog
| Datum | Version | Änderung | Angestoßen von |
|---|---|---|---|
| 26.09.2026 | v0.1 | Gerüst angelegt, Kernhypothesen H1–H4 aus Projektanweisung übernommen | David |
| 26.09.2026 | v0.2 | Trigger „Fachprüfung Vermittler-Rolle vor erstem echten Zahlungsfluss" in Abschnitt 4 ergänzt | David |
| 26.09.2026 | v0.3 | Ausstehende Gründerentscheidung „Produktdatenbank für Autovervollständigung" ergänzt, inkl. Hinweis auf Spannung mit Validierung-vor-Bau-Leitplanke | David |
| 27.09.2026 | v0.4 | Funnel-Runde (29 Fragen) ausgewertet: 10 Entscheidungslog-Einträge (E1–E10) ergänzt; Abschnitt 4 aktualisiert (Produktdatenbank-Punkt aufgelöst nach E9, neue offene Punkte: Kategorie-Fokus, gemeinsame Warenwert-Schwelle, Fachprüfungs-Trigger weiterhin unbestätigt); Hinweis in Abschnitt 1 ergänzt, dass H1–H4 durch diese Runde unverändert [Hypothese] bleiben | David & Franzi (Funnel + Chat) |
| 27.09.2026 | v0.5 | H1-Zeile in Abschnitt 1 ergänzt: Testmethode und Erfolgskriterium festgelegt (alle Listings zählen, kein Schwellenwert), inkl. Risiko-Hinweis zur Kill-Switch-Wirkung; Entscheidungslog-Eintrag E11 ergänzt; Abschnitt 4 um offenen Punkt „Marketing- vs. Tech-Budget-Aufteilung" ergänzt | David & Franzi (Chat) |
 
