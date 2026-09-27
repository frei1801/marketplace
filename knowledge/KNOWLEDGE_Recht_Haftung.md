# KNOWLEDGE_Recht_Haftung.md
 
**Version:** v0.3 · **Stand:** 27.09.2026
**Zuständig für:** Haftung bei Schaden/Verlust/Nicht-Rückgabe, Kaution, Versicherung, Plattformhaftung, AGB, Zahlungsabwicklung (regulatorisch), steuerliche Behandlung der Verleiher, Datenschutz, Rechtsform
**Verbindlich lesen vor:** jeder Konzeptfrage zum Buchungsablauf, jeder Frage zu Schäden/Kaution/Versicherung, jeder Wahl eines Zahlungsanbieters, AGB- oder Datenschutztexten, jeder Kommunikation mit Anwalt, Steuerberater oder Versicherer
**Nicht zuständig (→ Verweis):** Kosten von Versicherung/Zahlung in den Unit Economics → KNOWLEDGE_Geschaeftsmodell.md · technische Umsetzung Zahlung → KNOWLEDGE_Tech_Architektur.md · Status von Annahmen → KNOWLEDGE_Hypothesen_Entscheidungen.md
**Statuslegende:** [Hypothese] · [Signal] · [Validiert] · [Entschieden] – Definition in KNOWLEDGE_Projektregeln.md
 
> **Hinweis:** Inhalte dieser Datei sind keine Rechts-, Steuer- oder Versicherungsberatung. Jeder Punkt erhält den Vermerk „Fachprüfung nötig: ja/nein" und – falls erfolgt – wer geprüft hat und wann.
 
---
 
## 1. Schadensfall-Logik (Kernprodukt)
> Für jeden Fall: Was passiert, wer zahlt, wie wird nachgewiesen?
 
| Fall | Ablauf | Wer zahlt | Nachweis | Fachprüfung nötig | Status |
|---|---|---|---|---|---|
| Beschädigung | – | – | – | – | leer |
| Verlust/Diebstahl | – | – | – | – | leer |
| Nicht-Rückgabe | Automatische Nachbelastung der Kaution nach Frist | Kaution des Mieters | – | ja, für AGB-Formulierung | [Entschieden] (Funnel rl6, 26.09.2026) |
| Personenschaden durch Gerät | – | – | – | – | leer |
 
- **Streitfall-Verfahren:** Vorher-/Nachher-Fotos, klare Regeln – die Plattform entscheidet nach definierten Kriterien (kein externer Gutachter, keine einseitige Verleiher-Entscheidung) [Entschieden] (Funnel rl7, 26.09.2026) – skalierbar, aber die „definierten Kriterien" selbst sind noch nicht ausformuliert
## 2. Kaution
- **Kaution (klassisch)**, keine Versicherung [Entschieden] (Funnel rl3, 26.09.2026) – Konversionshürde für Mieter bewusst in Kauf genommen. Höhe und Staffelung nach Warenwert: noch offen, hängt mit der Schutzgebühr-Schwelle (→ KNOWLEDGE_Geschaeftsmodell.md, Abschnitt 2) und der Verifizierungs-Schwelle (→ Abschnitt 10 unten) zusammen – sollten dieselbe Zahl verwenden, nicht drei verschiedene Schwellen pflegen
## 3. Versicherung
- **leer** (durch Kaution-Entscheidung in Abschnitt 2 vorerst nicht weiterverfolgt)
## 4. Plattformhaftung & AGB
- Rolle der Plattform (Vermittler vs. Vertragspartner): **offen**
- Zeitpunkt der Fachprüfung dazu: im Funnel (Frage rl5) erneut nicht bestätigt (übersprungen) – **weiterhin nicht mit Franzi abgestimmt.** Der bisherige Trigger bleibt in Kraft: spätestens vor dem ersten echten Zahlungsfluss im Split-Payment-Flow (→ KNOWLEDGE_Hypothesen_Entscheidungen.md, Abschnitt 4)
## 5. Zahlungsabwicklung (regulatorisch)
- Geldfluss: **Split-Payment über einen Payment-Service-Provider** – Geld fließt direkt Mieter → Verleiher, Provision wird automatisch abgezogen [Entschieden] (Funnel rl1, 26.09.2026) – reduziert die Frage nach einer eigenen Zahlungslizenz, ersetzt aber keine Fachprüfung
- Auszahlungszeitpunkt: **erst nach Rückgabe ohne Meldung** (wie Vinted) [Entschieden] (Funnel rl2, 26.09.2026) – schützt vor Vorauszahlung bei Problemfällen
- Fließen Kundengelder über die Plattform? Auch bei Split-Payment zu klären, ob und wie kurz Gelder „durchlaufen" – **offen, Fachprüfung nötig**
## 6. Steuern
- Steuerliche Behandlung der Verleiher-Einnahmen: **offen – Fachprüfung nötig**
- Steuerliche Pflichten der Plattform: **offen – Fachprüfung nötig**
## 7. Datenschutz
- **leer**
## 8. Rechtsform & Gründung
- **leer**
## 9. Offene Fragen an Fachleute (append-only)
> Format: Datum · Frage · an wen (Anwalt/Steuerberater/Versicherer) · Antwort · Datum Antwort
 
- *(noch keine Einträge)*
## 10. Vertrauensmechanismen (Verifizierung & Bewertungen)
- Bewertungssystem: beidseitig, Details → KNOWLEDGE_Markt_Wettbewerb.md, Abschnitt 2
- Verifizierung der Nutzer: **gestaffelt nach Warenwert** [Entschieden] (Chat, 27.09.2026, nach Funnel rl4/rl8):
  - Basis-Check für alle: 1-Cent-Testüberweisung (bestätigt Kontoinhaberschaft, nicht Identität) – kostenlos, geringe Hürde, wirkt als Spam-/Wegwerf-Account-Filter
  - Zusätzlich verpflichtend ab einer Kaution-/Warenwert-Schwelle: automatischer Dokumenten-Abgleich (z. B. Stripe Identity, ca. 1–3 € pro Prüfung) – bestätigt ein echtes Ausweisdokument, reduziert Identitätsdiebstahl-Risiko
  - **Offen:** die konkrete Warenwert-Schwelle ist noch nicht beziffert – sollte dieselbe sein wie bei der Schutzgebühr (→ KNOWLEDGE_Geschaeftsmodell.md, Abschnitt 2) und der Kaution-Staffelung (→ Abschnitt 2 oben), um nicht drei verschiedene Schwellen im Produkt zu haben
  - Fachprüfung nötig: ja – ob ein automatischer Dokumenten-Abgleich ohne Video-Ident für euren Anwendungsfall ausreicht, ist eine Frage für die noch ausstehende Fachprüfung „Vermittler vs. Vertragspartner" (Abschnitt 4)
---
 
## Changelog
| Datum | Version | Änderung | Angestoßen von |
|---|---|---|---|
| 26.09.2026 | v0.1 | Gerüst angelegt | David |
| 27.09.2026 | v0.2 | Aus Funnel-Antworten: Abschnitt 1 (Nicht-Rückgabe, Streitfall-Verfahren), Abschnitt 2 (Kaution statt Versicherung), Abschnitt 5 (Split-Payment, Auszahlungszeitpunkt) entschieden; Abschnitt 4 Fachprüfungs-Status aktualisiert (weiterhin nicht mit Franzi abgestimmt); Abschnitt 10 neu: Verifizierungsmethode gestaffelt nach Warenwert festgelegt, nach ausführlicher Diskussion von RL4 (Testüberweisung) vs. RL8 (Dokumenten-Abgleich) im Chat | David & Franzi (Funnel + Chat) |
| 27.09.2026 | v0.3 | Statuslegende-Verweis im Kopf aktualisiert: zeigt jetzt auf die neue KNOWLEDGE_Projektregeln.md statt auf die Projektanweisung | David |
 ‚s