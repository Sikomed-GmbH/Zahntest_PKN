# Zahnzentrum – Landingpage mit Zahn-Selbsttest

Landingpage zur Bewerbung des **Zahnzentrums der Pferdeklinik Niederlenz**.
Kernelement ist ein interaktiver **Zahn-Selbsttest**, mit dem Pferdebesitzer
einschätzen können, ob ihr Pferd tierärztlich vorgestellt werden sollte und in
welchem Rhythmus eine Zahn-Prophylaxe sinnvoll ist.

## Aufbau

Die gesamte Seite steckt in einer einzigen, eigenständigen Datei: [`index.html`](index.html).
Kein Build-Schritt, keine externen Abhängigkeiten (CSS, JavaScript, Icons und
Grafiken sind inline eingebettet) – die Datei kann direkt auf jedem Webserver
oder in einem CMS abgelegt werden.

### Abschnitte
- **Hero** mit Einstieg und CTA zum Selbsttest
- **Zahn-Selbsttest** (Kernstück) – 11 Fragen, individuelle Auswertung
- **Leistungen** des Zahnzentrums
- **Prophylaxe** – Orientierung zu Kontroll-Intervallen nach Alter
- **Warnzeichen** für Zahnprobleme
- **Team** (Dr. Sébastien Moine, Dr. Christian Czech)
- **Kontakt / Terminanfrage**

## Der Selbsttest – Logik

Der Test kombiniert zwei Ergebnisse:

1. **Dringlichkeit einer Tierarzt-Vorstellung** (Ampel):
   - **Rot** – akute Warnzeichen (z. B. Futter fällt aus dem Maul, Gewichts­verlust,
     einseitiger Nasenausfluss, Zahnfleisch-/Kieferveränderung) *oder* eine hohe
     Summe an Auffälligkeiten → zeitnah vorstellen.
   - **Gelb** – einzelne Auffälligkeiten → Kontrolle einplanen und beobachten.
   - **Grün** – keine akuten Warnzeichen → reguläre Vorsorge.
2. **Empfohlenes Prophylaxe-Intervall**, abhängig vom Alter des Pferdes
   (Jungpferd: alle 6 Monate · erwachsen: jährlich · Senior: alle 6–12 Monate)
   und ggf. verkürzt, wenn Auffälligkeiten vorliegen.

Die Frage- und Bewertungslogik ist im `<script>`-Block von `index.html` im Objekt
`QUESTIONS` sauber getrennt hinterlegt und lässt sich leicht anpassen
(Fragen, Punktegewichte, Warnzeichen-Flags).

> **Hinweis:** Der Selbsttest ist ein Orientierungs-Tool und ersetzt keine
> tierärztliche Untersuchung. Ein entsprechender Disclaimer ist auf der Seite
> eingebunden.

## Anpassung / offene Punkte

- **Design/Branding:** Die Live-Website `pferdeklinik.ch` war aus dieser
  Umgebung technisch nicht abrufbar (Netzwerk-Policy). Farben (dunkles
  Klinik-Grün + Gold) und Typografie sind an ein premium­iges Pferdeklinik-Umfeld
  angelehnt und sollten bei Bedarf an die exakten Marken-Vorgaben (Hausfarben,
  Logo, Schriftart) angepasst werden.
- **Bilder:** Statt Fotos werden bewusst eigenständige SVG-Grafiken/Icons genutzt,
  damit die Seite ohne externe Ressourcen läuft. Echte Klinik-/Pferdefotos können
  ergänzt werden.
- **Kontaktdaten** (Adresse, Telefon, Sprechzeiten) bitte vor Veröffentlichung
  final gegenprüfen.
