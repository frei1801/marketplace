# KNOWLEDGE_Projektregeln.md
 
**Version:** v1.0 · **Stand:** 27.09.2026
**Zuständig für:** Betriebsregeln dieses Projekts – wie mit den Wissensdateien gearbeitet wird: Quellen-Vorrang, Status-Kennzeichnung, Pflege bei Änderungen, Schreibrechte/Bestätigungspflicht, Weitergabe an Dritte, Anlage neuer Themenstränge
**Verbindlich lesen vor:** jedem Artefakt (Analyse, Konzept, Deck, Textentwurf, Wissensdatei-Aktualisierung) und jeder Aussage darüber, was in diesem Projekt entschieden, validiert oder noch offen ist
**Nicht zuständig (→ Verweis):** inhaltliche Fakten zum Marktplatz stehen in den vier Fach-Wissensdateien (Geschaeftsmodell, Markt_Wettbewerb, Recht_Haftung, Tech_Architektur); Status und Verlauf einzelner Hypothesen/Entscheidungen im Detail → KNOWLEDGE_Hypothesen_Entscheidungen.md
**Diese Datei ist die Referenz für:** die Statuslegende, die alle anderen Wissensdateien in ihrem Kopf nur zitieren
 
---
 
## 1. Quellen-Hierarchie
1. Aktuelle Nachricht (schlägt alle Dateien)
2. Ist-Zustand (gleichrangig, überschneidungsfrei):
   – KNOWLEDGE_Geschaeftsmodell.md = Gebührenmodell, Preislogik, Unit Economics, Kostenstruktur, Ambition & Budget
   – KNOWLEDGE_Markt_Wettbewerb.md = Wettbewerber, Zielgruppen (Mieter/Verleiher), Kategorien, Berlin-Fokus, Nachfrage-Signale
   – KNOWLEDGE_Recht_Haftung.md = Haftung bei Schäden/Verlust, Kaution, Versicherung, Plattformhaftung, AGB, Zahlungsabwicklung (regulatorisch), steuerliche Behandlung der Verleiher, Datenschutz
   – KNOWLEDGE_Tech_Architektur.md = Framework-Entscheidung, Service Provider, Datenmodell, laufende Kosten, technische Schulden
   – KNOWLEDGE_Hypothesen_Entscheidungen.md = Hypothesen-Log mit Status und Entscheidungslog (append-only)
3. Hypothesen mit Status „offen" sind Richtung, nicht Fakt – nie als belegt darstellen.
4. Projekterinnerungen zuletzt: verdichtete, lückenhafte Erinnerung an frühere Chats. Sie liefern Arbeitskontext, nicht Faktenstand; Zahlen und Entscheidungen immer gegen die Wissensdateien prüfen.
Bei Widerspruch gilt der Ist-Zustand, bis eine Änderung in der zuständigen Datei nachgezogen ist. Bei Überschneidungen hat die thematisch zuständige Datei Vorrang (Zahlen/Modell → Geschäftsmodell; Markt/Wettbewerb → Markt_Wettbewerb; Recht/Versicherung/Zahlungsregulatorik → Recht_Haftung; Systeme/Kosten der Technik → Tech_Architektur; Status einer Annahme oder Entscheidung → Hypothesen_Entscheidungen).
 
## 2. Kennzeichnung von Wissen
Jede inhaltliche Aussage in Wissensdateien trägt einen Status:
   [Hypothese] = Annahme, nicht geprüft
   [Signal] = erste Evidenz (Gespräch, Umfrage, Recherche), nicht belastbar
   [Validiert] = belastbar belegt (Quelle, Datum, Stichprobe nennen)
   [Entschieden] = von beiden Gründern beschlossen (Datum)
Recherche-Ergebnisse immer mit Quelle und Datum. Statusänderungen werden im Hypothesen-Log nachvollzogen, nie still überschrieben.
 
## 3. Wissensdatei-Pflege
Nennt jemand im Chat Fakten, die den Wissensdateien widersprechen oder sie ergänzen, sofort darauf hinweisen und fragen, ob eine aktualisierte Version erstellt werden soll – auch bei kleinen Änderungen. Dies gilt für Änderungen an bereits bestehenden Wissensdateien.
Bei jeder Aktualisierung: Versionsnummer hochzählen (Minor bei Korrekturen/Ergänzungen, Major bei Strukturänderungen), Änderungsdatum aktualisieren, Changelog-Eintrag mit Datum, Version, Kurzbeschreibung und wer die Änderung angestoßen hat (David/Franzi).
Cross-Referenz-Check: prüfen, ob andere Dateien auf den geänderten Inhalt verweisen.
Neue Fakten an genau einer Stelle pflegen und von anderen Dateien aus verweisen statt duplizieren. Gilt auch für die Projektanweisung selbst und für diese Datei: Detailregeln stehen genau einmal, andere Stellen verweisen nur.
 
## 4. Schreibzugriff (sofern im Projekt verfügbar)
Bestätigungspflicht: Jede inhaltliche Änderung an einer bereits bestehenden Wissensdatei wird vorgeschlagen und erst nach Zustimmung geschrieben. Ausnahmen ohne Rückfrage: (1) reine Ergänzungen in als append-only gekennzeichneten Abschnitten – dort anhängen, nie überschreiben; (2) eine komplett neue Wissensdatei (z. B. für einen neuen Themenstrang) wird direkt angelegt und gespeichert, ohne vorher zu fragen. In beiden Fällen gelten Version, Datum und Changelog trotzdem, und nach dem Schreiben wird kurz genannt, was neu angelegt bzw. ergänzt wurde.
Immer den exakten bestehenden Dateipfad überschreiben, nie eine zweite Datei unter abweichendem Namen anlegen; Pfad vor jedem Schreibvorgang verifizieren.
Kein Schreib-Churn: Änderungen einer Session gesammelt in einem Schreibvorgang je Datei.
Nach jedem Schreibvorgang in einem Satz nennen, welche Datei in welcher Version geschrieben wurde, und automatisch eine vollständige Downloadversion bereitstellen (nie Auszug oder Änderungsliste).
Uploads (PDFs, Spreadsheets) und Projekteinstellungen sind schreibgeschützt. Aktualisierungen der Projektanweisung immer vollständig als Copy-and-paste-Block ausgeben.
 
## 5. Weitergabe an Externe
Alle Inhalte sind für beide Gründer offen. Soll ein Artefakt an Dritte gehen (Anwalt, Steuerberater, Versicherer, Freelancer, Investor), vorher prüfen und benennen, welche Inhalte nicht rausgehen sollten (z. B. private Finanzen, interne Bewertungen, unvalidierte Zahlen als Fakt).
 
## 6. Themenstränge
Jeder inhaltlich abgrenzbare Strang (z. B. Launch-Marketing, Finanzierung, Kategorie-Deep-Dives) bekommt bei Bedarf eigene Wissensdatei(en) nach demselben Muster und wird oben in Abschnitt 1 (Quellen-Hierarchie) ergänzt. Neuanlage erfolgt gemäß Abschnitt 4 (Schreibzugriff) automatisch, ohne vorherige Rückfrage.
Kill-Switch Projekt-Split: Wenn die Projektsuche bei klaren Fragen wiederholt irrelevante Dateien priorisiert oder die Vorrang-Regeln mehr als ca. 15 Zeilen bräuchten, das Projekt aufteilen.
 
---
 
## Changelog
| Datum | Version | Änderung | Angestoßen von |
|---|---|---|---|
| 27.09.2026 | v1.0 | Datei neu angelegt: Betriebsregeln aus der Projektanweisung ausgelagert (Quellen-Hierarchie, Kennzeichnung von Wissen, Wissensdatei-Pflege, Schreibzugriff, Weitergabe an Externe, Themenstränge), damit die Projektanweisung kürzer wird und Claude Änderungen hier direkt schreiben kann statt sie per Copy-and-Paste in die Projekteinstellungen zu geben. Die frühere „Sync zwischen zwei Projekten"-Regel entfällt ersatzlos, da David und Franzi nur noch in einem gemeinsamen Projekt arbeiten. | David
