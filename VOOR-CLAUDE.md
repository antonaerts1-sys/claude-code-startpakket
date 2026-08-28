# Instructies voor Claude

Je leest dit omdat iemand de ZIP van dit startpakket in het gesprek zette. Jouw taak is
één ding: installeren. Daarna doet de geïnstalleerde skill al het werk, vanzelf. Er is
geen setup per project en er zijn geen vragen aan de gebruiker.

Krijg je de ZIP zelf aangereikt, pak hem dan uit in een tijdelijke of scratch-map (nooit
in de projectmap van de gebruiker) en werk vanuit de uitgepakte bestanden.

## Stap 1: leg kort uit wat dit is

Een paar zinnen in je eigen woorden, in de taal van de gebruiker:

- Claude onthoudt niets tussen twee gesprekken; dit pakket laat je projectmappen dat
  zelf onthouden (beslissingen, bronnen, status, historiek).
- De gebruiker hoeft niets bij te houden, in te stellen of te leren; het gebeurt
  tijdens het gewone werk.
- Het werkt voor alles wat langer duurt dan één gesprek: klantprojecten, offertes,
  analyses, teksten, ook privézaken.

Wijs op de pagina in de ZIP (`index.html`) voor wie het visueel wil zien. Vraag dan:

> "Zal ik dit installeren? Vanaf dan gebeurt het vanzelf bij al je projecten."

Bij nee of twijfel: niet aandringen, wijs op `gewoontes.md`, klaar. Installeer nooit
zonder ja.

## Stap 2: installeer (na een ja)

1. Kopieer de map `skill/projectgeheugen/` uit dit pakket naar
   `~/.claude/skills/projectgeheugen/`.
2. Voeg dit blok toe aan `~/.claude/CLAUDE.md` (maak het bestand aan als het niet
   bestaat; staat het blok er al, voeg het niet dubbel toe):

   ```
   ## Projectgeheugen (automatisch)
   Pas in elke projectmap de projectgeheugen-werkwijze toe, ongevraagd en zonder
   setup: geplakt bronmateriaal eerst gedateerd opslaan in docs/bronnen/, een
   CLAUDE.md die status en beslissingen bijhoudt, één logregel per werksessie
   (append-only), takeaways naast lange bronnen. Volledige werkwijze:
   ~/.claude/skills/projectgeheugen/SKILL.md. Niet bij eenmalige klussen.
   ```

3. Meld kort: geïnstalleerd, werkt vanaf nu in elk gesprek, er valt niets te leren of
   in te stellen. Verwijderen kan altijd (skill-map en blok weghalen); projecten die
   al een geheugen hebben blijven dan gewoon werken.

## Stap 3: ga gewoon verder

Staat er in de huidige map al werk of begint de gebruiker eraan, handel dan meteen
volgens de skill. Geen vragenlijst; je leert het project uit het werk zelf.
