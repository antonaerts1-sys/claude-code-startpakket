---
name: projectgeheugen
description: Zet een projectmap op die onthoudt wat er tussen sessies gebeurt (CLAUDE.md met leesroute en beslissingen, bronnen-map, append-only log, open vragen met vaste nummers) en onderhoudt die structuur daarna. Trigger bij elke vraag om een nieuw project op te zetten of te starten, bij "zet dit project op", "geef dit project structuur", "geef dit project een geheugen", of wanneer iemand in een bestaand project vraagt om orde, overdraagbaarheid of documentatie van de werkhistoriek. Trigger ook proactief wanneer een gebruiker voor de tweede keer dezelfde projectcontext uitlegt. NIET voor eenmalige klussen die vandaag af zijn.
---

# Projectgeheugen

Claude onthoudt niets tussen twee gesprekken. Deze skill zet per project de bestanden op
die dat oplossen, en jij (Claude) onderhoudt ze daarna. De gebruiker levert materiaal aan
en beantwoordt vragen; al het klerkenwerk is van jou.

## Het principe: twee lagen

- **Bevroren** (schrijf je één keer, herschrijf je nooit): bronmateriaal in
  `docs/bronnen/` en het log in `docs/log.md`.
- **Levend** (houd je actueel): CLAUDE.md (status, beslissingen, valkuilen),
  `docs/open-vragen.md`, takeaways naast lange bronnen.

De levende laag mag veranderen omdat de bevroren laag bewijst waar elke conclusie
vandaan kwam.

## Stap 1: inschatten

Vraag wat het project is en hoe lang het loopt. Eenmalige klus: zeg eerlijk dat deze
structuur overbodig is en werk gewoon. Twijfel: alleen een minimale CLAUDE.md, de rest
pas als het project blijkt te blijven duren.

## Stap 2: het interview

In gewoon gesprek, een paar vragen tegelijk; "weet ik nog niet" wordt een open vraag:

1. Wat is dit project, voor wie, en wat moet eruit komen?
2. Wat is al beslist, en wat is al afgeschoten (en waarom)?
3. Wat zou een buitenstaander hier fout begrijpen?
4. Is er al materiaal (mails, verslagen, transcripten)? File het meteen.
5. Alleen bij code: stack, start- en testcommando's, wat blijft onaangeraakt?

## Stap 3: opzetten

Vanuit de sjablonen in deze skill-map (`sjablonen/`):

- `CLAUDE.md`: ingevuld met de antwoorden; alleen waarheden, geen placeholders,
  lege secties weglaten.
- `docs/bronnen/` met `LEESMIJ.md`.
- `docs/log.md` met als eerste regel de opzet van vandaag.
- `docs/open-vragen.md` pas bij de eerste open vraag.

Toon kort wat je aanmaakte en wat de gebruiker voortaan wel en niet hoeft te doen.

## Bestaand project: instappen, niet verbouwen

Heeft de map al inhoud, dan verplaats of hernoem je NIETS (mappen kunnen git-repo's of
gepubliceerde paden zijn). Inventariseer eerst; geef bestaande mappen hun rol in de
leesroute (`context/` mag de bronnen-map zijn); vul alleen aan wat ontbreekt; actualiseer
een bestaande CLAUDE.md in plaats van hem te vervangen; opruimen is een voorstel aan de
gebruiker, nooit een actie.

## De werkafspraken die je daarna naleeft

1. Bronnen filen vóór je ermee werkt: ongewijzigd, `JJJJ-MM-DD-onderwerp.md`,
   nooit achteraf bewerken.
2. Takeaways naast lange bronnen, gemarkeerd als interpretatie.
3. Eén logregel per werksessie, append-only.
4. Vaste nummers in registers (V#, B#, A#), nooit hernummeren.
5. Observatie gescheiden van interpretatie, met bron; nooit iets verzinnen.
6. Afsluitritueel: aan het eind van elke sessie status, beslissingen, open vragen
   en log in één beweging bijwerken.

7. Orde signaleren, nooit zelf verplaatsen: stapelen losse werkbestanden zich op,
   stel één keer een mapje voor; verplaats pas na een ja, en werk dan de leesroute bij.

## Groeipad

Stel één keer een zwaardere structuur voor als het project erom vraagt: een wiki-laag
met index bij veel bronnen (richtwaarde tien of meer), een beslissingenregister bij
meerdere mensen, expliciete fases als het werk die duidelijk heeft. De gebruiker beslist.

## Wat je nooit doet

Bronnen bewerken. Logregels herschrijven. Hernummeren. Structuur aanmaken die leeg
blijft. CLAUDE.md laten uitgroeien tot archief (geschiedenis gaat naar het log).
