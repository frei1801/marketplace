# KNOWLEDGE_Geschaeftsmodell.md
 
**Version:** v0.6 · **Stand:** 27.09.2026
**Zuständig für:** Gebührenmodell, Preislogik, Unit Economics je Kategorie, Kostenstruktur, Ambition, Zeit- und Geldbudget, Kill-Switch-Schwellen
**Verbindlich lesen vor:** jeder Rechnung, Preis- oder Gebührenfrage, jedem Plan mit Zeit-/Geldbezug, jedem Kill-Switch, jeder Investoren- oder Finanzierungsfrage
**Nicht zuständig (→ Verweis):** Wettbewerberpreise → KNOWLEDGE_Markt_Wettbewerb.md · Kosten der Technik → KNOWLEDGE_Tech_Architektur.md · Versicherungs-/Zahlungskosten (regulatorisch) → KNOWLEDGE_Recht_Haftung.md · Status von Annahmen → KNOWLEDGE_Hypothesen_Entscheidungen.md
**Statuslegende:** [Hypothese] · [Signal] · [Validiert] · [Entschieden] – Definition in KNOWLEDGE_Projektregeln.md
 
---
 
## 1. Ambition & Budget
- Ambition: **Erst mal ein Experiment** – klar begrenzter Testzeitraum, danach bewusste Entscheidung, ob's weitergeht [Entschieden] (Funnel gm5, Gemeinsam, 26.09.2026)
- Zeitbudget je Gründer: **5–10 Std./Woche** [Entschieden] (Funnel gm6, Gemeinsam, 26.09.2026)
- Geldbudget bis Validierung: **1.000–5.000 €** [Entschieden] (Funnel gm7, Gemeinsam, 26.09.2026)
- Zeithorizont bis Go/No-Go: **6 Monate** (Ziel: Ende März 2027) [Entschieden] (Funnel gm8, Gemeinsam, 26.09.2026)
> Abschnitt ist jetzt vollständig [Entschieden] – die Kill-Switch-Schwelle in Abschnitt 6 ist damit verbindlich, nicht mehr nur Vorschlag.
 
## 2. Gebührenmodell
- Wer zahlt die Provision: **beide Seiten** – Mieter zahlt Servicegebühr, Verleiher zahlt Vermittlungsprovision (wie Vinted/Airbnb) [Entschieden] (Funnel gm1, 26.09.2026)
- Provisionshöhe-Richtung: **niedrig halten (5–10 %)** – Wachstum vor Marge in der Testphase; genaue Prozentzahl folgt erst mit echten Unit Economics (→ Abschnitt 4, noch leer) [Entschieden – Richtung; Zahl offen] (Funnel gm9, 26.09.2026)
- Boost-Funktion: **zeitlich befristetes Boosten** – Verleiher zahlt X € für Y Tage oben in der Such-/Kategorieliste (Beträge noch offen) [Entschieden – Mechanik; Preis offen] (Funnel gm2, 26.09.2026)
- Abo-Modell für Vielverleiher: **kein Abo, nur pro Transaktion** [Entschieden] (Funnel gm3, 26.09.2026)
- Schutzgebühr: **nur bei höherwertigen Gegenständen** ab bestimmtem Warenwert (Schwelle noch offen, hängt an Abschnitt 4 Unit Economics und an KNOWLEDGE_Recht_Haftung.md Abschnitt 2 Kaution) [Entschieden – Mechanik; Schwelle offen] (Funnel gm4, 26.09.2026) – Hinweis: dieselbe Warenwert-Schwelle soll auch die Verifizierungsstufe steuern, siehe KNOWLEDGE_Recht_Haftung.md Abschnitt 10
## 3. Preislogik
- Wer setzt den Mietpreis: **Verleiher setzt frei** – volle Kontrolle beim Verleiher, Risiko von Fehlbepreisung bewusst in Kauf genommen [Entschieden] (Funnel gm10, 26.09.2026)
- Kaution: Verweis → KNOWLEDGE_Recht_Haftung.md, Abschnitt 2
## 4. Unit Economics je Kategorie
> Kennzahlen nie über Kategorien mitteln, ohne das zu kennzeichnen.
 
| Kategorie | Ø Mietpreis | Buchungen/Jahr je Gegenstand | Gebühr/Buchung | Schadensquote | Status |
|---|---|---|---|---|---|
| Garten (z. B. Häcksler) | – | – | – | – | leer |
| Auto-Zubehör (z. B. Dachträger) | – | – | – | – | leer |
| Werkzeug | – | – | – | – | leer |
| Freizeit | – | – | – | – | leer |
 
## 5. Kostenstruktur
- Fixkosten/Monat: **leer** (Tech-Anteil → KNOWLEDGE_Tech_Architektur.md, Abschnitte 3 und 6)
- Variable Kosten/Transaktion (Zahlung, Versicherung, Support): **leer**
- Akquisekosten Verleiher / Mieter: **leer**
- Einmalkosten: Entwicklungs-Hardware – **Freigabe erteilt, jetzt kaufen** [Entschieden] (Funnel gm11, 26.09.2026), da Budget (Abschnitt 1) jetzt entschieden ist und den geschätzten Rahmen deckt. Beträge und Quellen → KNOWLEDGE_Tech_Architektur.md, Abschnitt 6b
- Einmalkosten: Recherche für Produktdatenbank (Autovervollständigung beim Einstellen), Startumfang **alle vier Kategorien** [Entschieden – Umfang; gegen Claudes Empfehlung, Risiko bewusst in Kauf genommen, siehe KNOWLEDGE_Hypothesen_Entscheidungen.md Abschnitt 5, E9] (Funnel tc4, 26.09.2026) – Ansatz → KNOWLEDGE_Tech_Architektur.md, Abschnitt 8. Betrag noch nicht beziffert
- Marketing-Budget (bezahlte Werbung zur Verleiher-/Mieter-Gewinnung): **wird aus dem bestehenden Budget-Rahmen finanziert, nicht zusätzlich** [Entschieden] (Chat, 27.09.2026) – **Spannungs-Hinweis, nicht aufgelöst:** Die Entwicklungshardware bindet bereits ca. 1.530–1.950 € (→ KNOWLEDGE_Tech_Architektur.md, Abschnitt 6b) aus dem Rahmen von 1.000–5.000 € (→ Abschnitt 1). Am unteren Ende des Rahmens (1.000 €) besteht damit schon vor dem ersten Marketing-Euro eine Unterdeckung von mind. ca. 530 €. Konkrete Aufteilung Marketing vs. Tech: **offen** – der real verfügbare Betrag muss vermutlich näher am oberen Ende (3.000–5.000 €) liegen, damit für Marketing überhaupt Spielraum bleibt (→ KNOWLEDGE_Hypothesen_Entscheidungen.md, Abschnitt 4)
## 6. Kill-Switch-Schwellen
- **Nach 6 Monaten (Ziel: Ende März 2027) wird abgebrochen oder grundlegend neu bewertet, wenn H1 (Verleiher-Bereitschaft) nicht mindestens [Signal] erreicht hat.** [Entschieden – Claudes Standardvorschlag übernommen, da im Funnel keine abweichende Präferenz genannt wurde, 26.09.2026; jederzeit änderbar]
- Weitere Schwellen (z. B. Geldbudget-Verbrauch, Zeitbudget-Verbrauch): noch offen
- **Hinweis zur Auswertbarkeit dieses Kill-Switches:** Die H1-Testmethode (→ KNOWLEDGE_Hypothesen_Entscheidungen.md, Abschnitt 1 und Abschnitt 5, E11) zählt Eigenlistings der Gründer und Freunde/Bekannte gleichwertig zu fremden Verleihern und verzichtet auf einen Schwellenwert. Dadurch ist dieser Kill-Switch am Stichtag praktisch kaum noch objektiv als „nicht erreicht" auswertbar – bewusst von den Gründern in Kauf genommen, nicht aufgelöst.
---
 
## Changelog
| Datum | Version | Änderung | Angestoßen von |
|---|---|---|---|
| 26.09.2026 | v0.1 | Gerüst angelegt | David |
| 26.09.2026 | v0.2 | Kostenstruktur: Einmalkosten Entwicklungs-Hardware mit Verweis auf Tech_Architektur ergänzt | Franzi |
| 26.09.2026 | v0.3 | Kostenstruktur: Einmalkosten Produktdatenbank-Recherche ergänzt, Verweis auf Tech_Architektur Abschnitt 8 | David |
| 27.09.2026 | v0.4 | Aus Funnel-Antworten: Abschnitt 1 (Ambition & Budget) komplett entschieden; Abschnitt 2 (Gebührenmodell) und Abschnitt 3 (Preislogik) befüllt; Abschnitt 5 Produktdatenbank-Umfang auf „alle vier Kategorien" aktualisiert (Risiko-Hinweis); Abschnitt 6 Kill-Switch erstmals konkret (6-Monats-Frist an H1) | David & Franzi (Funnel) |
| 27.09.2026 | v0.5 | Statuslegende-Verweis im Kopf aktualisiert: zeigt jetzt auf die neue KNOWLEDGE_Projektregeln.md statt auf die Projektanweisung | David |
| 27.09.2026 | v0.6 | Abschnitt 5: Marketing-Budget als Teil des bestehenden 1.000–5.000-€-Rahmens festgelegt, Spannung mit bereits gebundenen Hardwarekosten benannt (offene Aufteilung); Abschnitt 6: Hinweis ergänzt, dass die H1-Testmethode (E11) den Kill-Switch praktisch kaum noch auswertbar macht | David & Franzi (Chat) |