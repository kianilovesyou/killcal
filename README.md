# KillCal

Privater, einfacher Kalorien- und Nährwert-Tracker als Web-App (für zwei Personen).
Tagebuch mit Verlauf, Barcode-Scan, Suche, eigene Gerichte, Gewicht und Wasser.
Dieses Projekt steht in keiner Verbindung zu anderen Kalorienzähler-Apps oder deren Anbietern.

## Wichtige Hinweise
- **Keine medizinische Beratung.** Kalorienziele sind grobe Richtwerte (Mifflin-St Jeor).
  Bei Vorerkrankungen, Schwangerschaft oder Essstörungen ärztlichen Rat einholen.
- **Keine Gewähr.** Nährwertangaben stammen aus Open Food Facts und können fehlerhaft sein.
- **Privater Gebrauch.** Die App ist nicht für die Öffentlichkeit gedacht. Registrierung
  in Supabase ausgeschaltet lassen, Konten nur manuell anlegen.

## Einrichtung
1. Auf supabase.com ein Projekt anlegen, **Region: EU (z. B. Frankfurt)**.
2. Im SQL Editor den Inhalt von `setup.sql` ausführen.
3. Authentication → Users → Add user: E-Mail `benutzername@killcal.app`, Passwort wählen,
   „Auto Confirm User“ anhaken. Der Benutzername ist der Teil vor dem @.
4. Authentication → Sign In / Providers: „Allow new users to sign up“ **ausschalten**.
5. Project Settings → API: Project URL und `anon public` key in `index.html` bei `CFG` eintragen.
6. Dateien auf GitHub hochladen, GitHub Pages aktivieren.

## Sicherheit
- Der `anon` key darf im Code stehen. Die Row-Level-Security in `setup.sql` sorgt dafür,
  dass jede Person nur ihr eigenes Tagebuch sieht.
- **Niemals** den `service_role` key, Passwörter oder exportierte Sicherungsdateien
  (`killcal-daten*.json`, enthalten Gesundheitsdaten) hochladen. `.gitignore` hilft dabei.

## Datenquellen und Lizenz
Siehe `NOTICE.md`. Der Code steht unter der MIT-Lizenz (`LICENSE`).

## Konten direkt in der App anlegen (Alternative zu Schritt 3)
1. In Supabase unter Sign In / Providers „Allow new users to sign up“ **kurz einschalten** und „Confirm email“ ausgeschaltet lassen.
2. In `index.html` `signup:false` auf `signup:true` stellen und hochladen.
3. Jede Person gibt in der App ihren Namen und ein Passwort (mind. 8 Zeichen) ein und tippt auf „Konto erstellen“. Der Name wird kleingeschrieben zum Anmeldenamen (ä → ae, ö → oe, ü → ue, ß → ss).
4. Danach **beides wieder ausschalten**: `signup:false` in `index.html` und „Allow new users to sign up“ in Supabase. Sonst kann sich jeder mit dem Link ein Konto anlegen.

## Schrift (Roboto)
Die Schriftdateien liegen im Ordner `fonts/` (siehe `fonts/README.md`). Fehlen sie,
nutzt die App automatisch die Systemschrift des Geräts.
