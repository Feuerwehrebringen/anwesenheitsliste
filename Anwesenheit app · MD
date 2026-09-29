# Anwesenheit / Dienstdoku – Neuaufbau (Stand 29.09.2026)

Frontend: GitHub Pages, Repo Feuerwehrebringen/anwesenheit (index.html, Logo als Base64 eingebettet)
Backend: Google Apps Script, an ein neues Google Sheet gebunden (Code.gs, Logo.gs, appsscript.json)
Web-App-URL (API): https://script.google.com/macros/s/AKfycbxdfFwc3Y_4t2a67TIhLbwDM7rzUmzZY67X7FH8d0GYF_Hz-K-h9jlfeugWPRuTClo/exec
Hinweis: Bei Code-Änderungen die Bereitstellung über "Bereitstellungen verwalten → Bearbeiten → Neue Version" aktualisieren, damit die URL gleich bleibt.

## Sheet-Struktur (wird mit setup() angelegt)
- Mannschaft: Nachname | Vorname | Leiter (Checkbox) | Aktiv (Checkbox). Anzeige "Nachname, Vorname", sortiert nach Nachname. Nur Aktive erscheinen; Leiter-Dropdown = nur Kameraden mit Haken bei Leiter.
- Einstellungen: Funktionen | Fahrzeuge
- Empfänger: Name | E-Mail | Typ (Bericht / Atemschutz) | Aktiv. "Atemschutz"-Empfänger (AGW) bekommen eine Kopie derselben Mail, wenn mindestens ein Kamerad mit Atemschutz ausgewählt ist.
- Doku: automatisch (Zeitstempel, Datum, Beginn, Ende, Thema, Leiter, Anzahl, Anwesende, AS-Träger, Bemerkungen, Mail an)

## Entscheidungen
- Nur Name ist Pflicht pro Kamerad; Funktion/Fahrzeug leer = "-"
- Keine Dienstart-Auswahl, Thema als Freitext; keine Zusatzfelder bei Atemschutz
- Mail: HTML mit Logo (cid) + Kurzübersicht + PDF-Anhang; Betreff mit [Atemschutz]-Kennzeichnung
- Logo in Logo.gs (Base64) für PDF und Mail, im Frontend inline
