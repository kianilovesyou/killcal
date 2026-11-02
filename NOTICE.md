# Hinweise zu Drittquellen

## Open Food Facts (Produktdaten)
Produktdaten, die per Suche oder Barcode-Scan abgerufen werden, stammen von
[Open Food Facts](https://world.openfoodfacts.org) und stehen unter der
[Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/).
Einzelne Inhalte stehen unter der Database Contents License.
© Open Food Facts-Beitragende.

Dieses Repository enthält keine Open-Food-Facts-Daten. Die Daten werden zur
Laufzeit abgerufen und nur im privaten Tagebuch der jeweiligen Person gespeichert.
Die Quelle wird in der App (Profil und Hinzufügen-Dialog) genannt.
Die Angaben sind von Freiwilligen erfasst und können fehlerhaft sein.

## Bibliotheken
Beim Start bzw. beim Scannen werden von jsDelivr geladen und nicht im Repository
mitgeliefert: `@supabase/supabase-js` (Anmeldung/Sync) und `@zxing/library`
(Barcode-Scan auf Geräten ohne eingebauten Scanner). Es gelten deren eigene Lizenzen.

## Dienste
Anmeldung und Speicherung laufen über [Supabase](https://supabase.com).

## Schrift
Die App nutzt die Schrift Roboto, die lokal aus dem Ordner `fonts/` ausgeliefert wird
(keine Verbindung zu Google-Servern). Die Lizenzdatei der Schrift liegt dort bei und gilt
für die Schriftdateien.

## Maskottchen / Icons
Die Bilddateien `icon-*.png`, `apple-touch-icon*.png` (Maskottchen) sind eigene Gestaltung des Projektinhabers
und von der MIT-Lizenz ausgenommen: alle Rechte vorbehalten. Eine Weiterverwendung ist nur mit Erlaubnis gestattet.
