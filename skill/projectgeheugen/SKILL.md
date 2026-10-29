---
name: projectgeheugen
description: Houdt in elke projectmap automatisch bij wat het project moet onthouden, zonder de gebruiker iets te vragen: bronmateriaal gedateerd bewaren, een CLAUDE.md met status en beslissingen, een append-only log, open vragen met vaste nummers. Trigger bij alle werk in een projectmap dat langer dan één gesprek loopt of kan lopen (klantprojecten, offertes, analyses, teksten, prototypes), en bij expliciete vragen als "geef dit project structuur" of "geef dit project een geheugen". NIET bij eenmalige klussen die vandaag af zijn, en NIET in een gewone chat zonder projectmap op de computer.
---

# Projectgeheugen

Doel: de gebruiker hoeft nooit iets uit te leggen, bij te houden of in te stellen.
Jij (Claude) legt vast wat het gesprek toch al prijsgeeft. Geen vragenlijsten, geen
setup-moment; het geheugen ontstaat tijdens het gewone werk.

**Alleen in een map op de computer.** Deze skill werkt enkel als je in een map op de
computer van de gebruiker werkt (Claude Code, Cowork). In een gewone chat, zonder
projectmap, doe je niets met deze skill: geen bestanden, geen voorstellen, geen
vermelding.

## Hoe een project zijn geheugen krijgt

Werk gewoon. Zodra het gesprek iets oplevert dat een volgende sessie moet weten (wat
het project is, een beslissing, een afgeschoten idee, een valkuil, een correctie van de
gebruiker), zet je het in de CLAUDE.md van de projectmap. Bestaat die nog niet, maak hem
dan aan met wat je op dat moment wéét: nooit placeholders, nooit een interview. Hooguit
één gerichte vraag als iets cruciaals onduidelijk blijft; "weet ik nog niet" wordt dan
een open vraag. `sjablonen/` in deze skill-map toont de vorm (leesroute, statusblok,
beslissingen, werkafspraken); neem daaruit over wat het project nodig heeft.

Eenmalige klus (vandaag af, geen vervolg): niets aanmaken.

## Twee lagen

- **Bevroren** (schrijf je één keer, herschrijf je nooit): bronmateriaal in
  `docs/bronnen/` en het log in `docs/log.md`.
- **Levend** (houd je actueel): CLAUDE.md (status, beslissingen, valkuilen),
  `docs/open-vragen.md`, takeaways naast lange bronnen.

De levende laag mag veranderen omdat de bevroren laag bewijst waar elke conclusie
vandaan kwam.

## De werkafspraken

1. Bronnen filen vóór je ermee werkt: alles wat de gebruiker plakt of aanlevert
   ongewijzigd naar `docs/bronnen/` als `JJJJ-MM-DD-onderwerp.md`; nooit achteraf
   bewerken, een nieuwe versie is een nieuw bestand.
2. Takeaways naast lange bronnen (transcripten, verslagen), gemarkeerd als
   interpretatie, met verwijzing naar de bron.
3. Eén logregel per werksessie in `docs/log.md`, append-only; fouten wis je niet,
   de correctie is de volgende regel.
4. Vaste nummers in registers (open vragen V#, beslissingen B#, aannames A#),
   nooit hernummeren; afgehandeld blijft staan met de afloop erbij.
5. Observatie gescheiden van interpretatie, met bron; gaten expliciet benoemen;
   nooit iets verzinnen.
6. Afsluitritueel: aan het eind van elke sessie status, beslissingen, open vragen
   en log in één beweging bijwerken.
7. Orde signaleren, nooit zelf verplaatsen: stapelen losse werkbestanden zich op,
   stel één keer een mapje voor; verplaats pas na een ja, en werk dan de leesroute bij.
8. Nieuwe taak, nieuw gesprek: begint de gebruiker in een lang gesprek aan een andere
   taak, doe dan eerst het afsluitritueel en stel daarna voor om een nieuw gesprek te
   starten (`/clear`). Leg in één zin uit waarom: een lang gesprek met taken door
   elkaar maakt Claude slordiger, en er gaat niets verloren omdat alles in de map
   staat. Eén keer voorstellen, niet aandringen.
9. Spiekbrief nakijken: een fout in CLAUDE.md wordt elke sessie herhaald, dus kijk hem
   af en toe kritisch na. Doe dat bij het afsluitritueel als de vorige controle meer
   dan ongeveer tien logregels geleden is, of eerder als je iets tegenstrijdigs
   opmerkt. Zoek naar: wat botst met het log of de bronnen, een status of beslissing
   die achterhaald is, open vragen die intussen beantwoord zijn, secties die te lang
   werden. Corrigeer niet stil: meld in één of twee zinnen wat je aanpaste en waarom,
   en schrijf een logregel "spiekbrief nagekeken". Twijfel je of iets nog klopt, maak
   er een open vraag van in plaats van het te schrappen.

## Bestaand project: instappen, niet verbouwen

Heeft de map al inhoud, verplaats of hernoem dan NIETS (mappen kunnen git-repo's of
gepubliceerde paden zijn). Geef bestaande mappen hun rol in de leesroute (`context/`
mag de bronnen-map zijn), vul alleen aan wat ontbreekt, actualiseer een bestaande
CLAUDE.md in plaats van hem te vervangen. Opruimen is een voorstel, nooit een actie.

## Groeipad

Stel één keer een zwaardere structuur voor als het project erom vraagt: een wiki-laag
met index bij veel bronnen (richtwaarde tien of meer), een beslissingenregister bij
meerdere mensen, expliciete fases als het werk die duidelijk heeft. De gebruiker beslist.

## Wat je nooit doet

De gebruiker een vragenlijst voorleggen. Bronnen bewerken. Logregels herschrijven.
Hernummeren. Structuur aanmaken die leeg blijft. CLAUDE.md laten uitgroeien tot archief
(geschiedenis gaat naar het log).
