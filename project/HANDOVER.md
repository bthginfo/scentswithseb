# Scents with Seb

[Vercel-Vorschau](https://scents-with-seb.vercel.app) · [CMS](https://scents-with-seb.vercel.app/admin)

Das persönliche Erstpasswort liegt in `.data/vercel-admin-access.json`. Im CMS lässt es sich unter Team & Zugänge ändern. Die Datei ist vom Repository ausgeschlossen.

## Redaktion

- Unter **Seiten bearbeiten** die deutsche oder englische Seitenfassung wählen, den Entwurf speichern und die Änderungen in der Desktop- und Mobilvorschau prüfen. **Veröffentlichen** übernimmt den Entwurf in die öffentlich sichtbare Fassung.
- Unter **Partner & Empfehlungen** im Abschnitt **Partnerlinks** Beschriftung, Bild und Linkziel bearbeiten. Der Schalter **Affiliate-Link (Werbung)** setzt die sichtbare Kennzeichnung und das Linkattribut `sponsored`. Die Sprachfassungen haben jeweils eigene redaktionelle Inhalte.
- Unter **Anfragen** erscheinen Kontakt- und Kooperationsanfragen. Die Website speichert Nachrichten im Postfach. SMTP lässt sich im CMS verbinden.
- Unter **Shop** lassen sich Sortiment, Preise, Liefergebiete und Bestellungen verwalten. Für den Verkaufsstart brauchen die Artikel freigegebene Daten und die Website ihren eigenen Stripe-Zugang samt Webhook. Der produktive Checkout steht bis dahin auf aus. Details stehen in `docs/recipes/commerce.md`.

## Betrieb

Die Vercel-Vorschau ist zur Abnahme erreichbar. Indexierung, Händlerfreigabe und projektspezifische Rechtstexte stehen vor dem öffentlichen Start an. Unabhängige Projekt- und Speicher-IDs stehen in `infrastructure.json`.

Die Datenbank dieser Vorschau ist eine SQLite-Datei im privaten Blob-Store dieser Website. Der Server übernimmt Änderungen mit einem ETag-Vergleich und wiederholt Schreibvorgänge bei einem Versionskonflikt. `DATABASE_URL` aktiviert bei einer separat aufgesetzten Neon-Datenbank den PostgreSQL-Pfad des Starters. Vor dem Wechsel müssen Inhalte und Einträge aus der Vorschau übertragen werden. Der GitHub-Zugriff der Sitzung hat die Erstellung des privaten Ziel-Repositorys verweigert. Der übergebene Quellstand liegt in einem eigenen lokalen Git-Repository.

## Quellen

- Originalvideos und lokale Reel-Standbilder. [Scents with Seb](https://www.instagram.com/scentswithseb/) · [Gym-Reel](https://www.instagram.com/reel/Df96oFWshiT/) · [Date-Night-Reel](https://www.instagram.com/reel/Df5C-cstxN6/)
- Duftnoten. [Montblanc Explorer](https://www.montblanc.com/en-us/fragrances/collection/explorer) · [Lattafa Khamrah](https://lattafa.com/product/khamrah/)
- Flakon- und Duftfamilienbilder sind illustrative Produktfotografien.

