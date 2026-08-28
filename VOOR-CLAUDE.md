# Instructies voor Claude

Je leest dit omdat een gebruiker vroeg om een project op te zetten volgens dit startpakket.
Jij doet het werk; de gebruiker beantwoordt alleen vragen. Hieronder staat wat je opzet,
hoe je het daarna onderhoudt, en wanneer je opschaalt.

## Als je dit als ZIP aangereikt krijgt

Sleept of noemt de gebruiker een ZIP van dit pakket, pak hem dan zelf uit (in een
tijdelijke of scratch-map, niet in de projectmap van de gebruiker) en werk vanuit de
uitgepakte bestanden. De gebruiker hoeft nooit zelf uit te pakken of paden te kennen.

## Stap 0: leg eerst uit wat dit is

Ga niet meteen vragen stellen. Wie deze ZIP binnenkrijgt, weet vaak alleen "een collega
stuurde me dit". Begin dus met een korte uitleg in je eigen woorden, in de taal van de
gebruiker, langs deze lijnen:

- Claude Code onthoudt niets tussen twee gesprekken; dit pakket lost dat op met een paar
  bestanden per project die jij (Claude) aanmaakt en bijhoudt.
- Wat het oplevert: geen context opnieuw uitleggen, beslissingen die niet terugkomen als
  voorstel, bronnen en transcripten die terugvindbaar en citeerbaar blijven, en projecten
  die na weken stilte meteen weer oppakbaar zijn.
- Het werkt voor alles wat langer duurt dan één gesprek: klantprojecten, offertes,
  analyses, workshops, teksten, ook privézaken als een verbouwing.
- De gebruiker hoeft niets bij te houden; alleen materiaal aanleveren en vragen
  beantwoorden.

Hooguit een paar zinnen plus een kort lijstje; geen lezing. Wijs erop dat er in de ZIP
een pagina zit (`index.html`) die dit visueel uitlegt, en bied aan die te openen.

Sluit af met de vraag waarmee het echte werk begint: "Zal ik dit project zo opzetten?"
(of, als de map al inhoud heeft: "Zal ik in dit bestaande project instappen?"). Wacht op
een ja. Vraagt iemand alleen "wat is dit?", dan is de uitleg het antwoord en dring je
niet aan.

## Het principe

Jij onthoudt niets tussen twee gesprekken. Alles wat dit project waardevol maakt over
sessies heen moet dus in bestanden staan. Die bestanden vallen in twee lagen:

- **Bevroren laag**: bronmateriaal (`docs/bronnen/`) en het log (`docs/log.md`).
  Schrijf je één keer, herschrijf je nooit.
- **Levende laag**: de synthese (CLAUDE.md met status en beslissingen, open vragen,
  takeaways). Houd je actueel; oude stand mag weg, want de bevroren laag bewijst
  waar de huidige stand vandaan kwam.

Alles hieronder is toepassing van dat ene principe.

## Stap 1: eerst inschatten of dit structuur verdient

Vraag de gebruiker wat het project is en hoe lang het ongeveer loopt. Is het een
eenmalige klus (een tekstje, een snelle analyse, iets dat vandaag af is), zeg dan eerlijk
dat het startpakket daarvoor overbodig is en werk gewoon. Zet de structuur alleen op voor
werk dat over meerdere sessies, dagen of mensen loopt.

Twijfelgeval: zet alleen een minimale CLAUDE.md op (projectomschrijving plus werkafspraken)
en stel de rest voor zodra het project blijkt te blijven duren.

## Stap 2: het interview

Stel deze vragen in gewoon gesprek, een paar tegelijk, in de taal van de gebruiker.
Sla niets over, maar accepteer "weet ik nog niet" als antwoord; dat wordt dan een open vraag.

1. Wat is dit project, voor wie, en wat moet er uiteindelijk uitkomen?
2. Wat is er al beslist? En belangrijker: wat is er al afgeschoten, en waarom?
3. Wat zou een buitenstaander hier fout begrijpen? (gevoeligheden, valkuilen,
   begrippen die intern iets anders betekenen)
4. Is er al materiaal? (mails, verslagen, transcripten, documenten; vraag of de
   gebruiker het wil plakken of aanleveren, dan file jij het meteen)
5. Alleen bij code: welke stack, hoe start en test je het, wat mag ik niet aanraken?

## Stap 3: opzetten

Maak aan in de projectmap:

- `CLAUDE.md` op basis van `sjablonen/CLAUDE.md`, ingevuld met de antwoorden.
  Alleen waarheden opschrijven; geen placeholders of gissingen laten staan. Secties
  zonder inhoud weglaten.
- `docs/bronnen/` met daarin `LEESMIJ.md` (kopieer `sjablonen/bronnen-LEESMIJ.md`).
- `docs/log.md` (kopieer `sjablonen/log.md`) met als eerste regel de opzet van vandaag.
- `docs/open-vragen.md` zodra er een eerste open vraag is, niet eerder.

Toon daarna kort wat je hebt aangemaakt en wat de gebruiker voortaan wel en niet
hoeft te doen (materiaal aanleveren en vragen beantwoorden: wel; bijhouden: niet).

## Stap 4: installeer de skill (vraag het in dezelfde beweging)

Vraag bij het afronden van de opzet meteen, in één zin:

> "Zal ik dit ook vast installeren als skill? Dan werkt deze aanpak voortaan vanzelf
> bij elk project en heb je de ZIP niet meer nodig."

Bij ja: kopieer de map `skill/projectgeheugen/` uit dit pakket naar
`~/.claude/skills/projectgeheugen/`. De skill is zelfstandig (instructies plus
sjablonen) en triggert voortaan zelf bij nieuwe projecten. Meld kort dat het gebeurd is
en dat weggooien altijd kan (map verwijderen volstaat; opgezette projecten blijven
gewoon werken).

Bij nee of twijfel: laat het rusten en vraag het niet opnieuw; het pakket blijft
werken via de ZIP. Installeer nooit stilzwijgend.

## Bestaand project: instappen, niet verbouwen

Heeft de projectmap al inhoud (bestanden, mappen, misschien zelfs een CLAUDE.md), dan
geldt een andere volgorde. De hoofdregel: **je verplaatst of hernoemt niets**. Bestaande
mappen kunnen git-repo's zijn, online gepubliceerd staan of ergens naar verwezen worden;
hernoemen breekt dingen die jij niet kan zien.

1. **Inventariseer eerst.** Bekijk de mapstructuur en lees wat er al aan documentatie
   staat. Stel de interviewvragen alleen voor wat je niet uit de map kan halen.
2. **Geef bestaande mappen hun rol in plaats van nieuwe namen.** Heet de bronnenmap hier
   `context/` of `input/`, dan ís dat de bronnenmap; leg dat vast in de leesroute van
   CLAUDE.md. De namen uit de sjablonen zijn conventie, geen vereiste.
3. **Vul alleen aan wat ontbreekt.** Meestal: een log.md (eerste regel: "instap volgens
   startpakket, oudere geschiedenis niet gereconstrueerd"), een open-vragenregister, en
   datering plus takeaways voor bronnen die er vanaf nu bijkomen. Oude bronnen laat je
   staan zoals ze staan.
4. **Bestaat er al een CLAUDE.md**, dan actualiseer je die en breng je hem in lijn met de
   werkafspraken hieronder; je vervangt hem niet door het sjabloon.
5. **Opruimen is een voorstel, geen actie.** Zie je rommel (dubbele kopieën, verouderde
   mappen), benoem het en laat de gebruiker beslissen. Nooit op eigen initiatief
   archiveren of verwijderen.

## De werkafspraken die je daarna naleeft

Deze staan ook in de aangemaakte CLAUDE.md, zodat elke latere sessie ze ziet:

1. **Bronnen filen.** Alles wat de gebruiker plakt of aanlevert als materiaal sla je
   ongewijzigd op in `docs/bronnen/` als `JJJJ-MM-DD-onderwerp.md`, vóór je ermee werkt.
   Nooit achteraf bewerken; een nieuwe versie is een nieuw bestand.
2. **Takeaways naast lange bronnen.** Bij een lang bestand (transcript, verslag) zet je
   een kort takeaways-bestand ernaast (`...-takeaways.md`), gemarkeerd als interpretatie,
   met verwijzing naar de bron. Latere sessies lezen de takeaways en duiken alleen in de
   bron als het erop aankomt. De bron zelf blijft onaangeroerd.
3. **Log bijhouden.** Eén regel per werksessie onderaan `docs/log.md`. Append-only:
   fouten wis je niet, de correctie is de volgende regel.
4. **Vaste nummers.** Registers (open vragen V#, aannames A#, beslissingen B#) houden
   hun nummer voor altijd. Beantwoord of vervallen: blijft staan, met de afloop erbij.
   Nooit hernummeren.
5. **Observatie gescheiden van interpretatie.** In analyses markeer je wat je hebt
   gezien (met bron) en wat je eruit afleidt. Wat je niet weet, benoem je expliciet.
   Verzin nooit cijfers, namen, veldnamen of bronnen.
6. **Afsluitritueel.** Aan het eind van elke werksessie, in één beweging: statusblok en
   beslissingen in CLAUDE.md actualiseren, open vragen bijwerken, logregel toevoegen.
   Een log dat klopt naast een CLAUDE.md die achterloopt is een half systeem.

7. **Orde signaleren, nooit zelf verplaatsen.** Merk je tijdens het afsluitritueel dat
   losse werkbestanden zich opstapelen in de projectmap, stel dan één keer een mapje
   voor ("zal ik de prototypes in prototypes/ zetten?"). Pas na een ja verplaats je iets,
   en dan werk je meteen de leesroute in CLAUDE.md bij.

## Groeipad: wanneer je opschalen voorstelt

Stel uit jezelf een zwaardere structuur voor (niet opdringen, één keer voorstellen)
wanneer het project daar aantoonbaar om vraagt:

- **Veel bronnen (richtwaarde: tien of meer), synthese verspreid over losse bestanden**:
  stel een `docs/wiki/`-laag voor met een indexpagina, waarin jij per onderwerp de
  actuele stand bijhoudt, met verwijzing naar de bronnen. De leesroute in CLAUDE.md
  wijst dan naar de index.
- **Meerdere mensen of parallelle sporen**: stel voor om beslissingen als genummerd
  register bij te houden met per beslissing de aanleiding en de afweging, zodat
  niemand oude discussies heropent.
- **Het werk blijkt duidelijke fases te hebben** (bijvoorbeeld: eerst begrijpen,
  dan beslissen, dan maken): benoem die fases expliciet in CLAUDE.md, met wat af moet
  zijn voor de volgende begint. Bedenk een fasering die bij dít soort werk past;
  de gebruiker beslist over overgangen, nooit jij.

## Wat je nooit doet

- Bronbestanden bewerken of samenvattend "opschonen".
- Logregels herschrijven of verwijderen.
- Registers hernummeren.
- Structuur aanmaken die leeg blijft. Elke map en elk bestand moet vandaag al
  inhoud hebben of vandaag nodig zijn.
- De CLAUDE.md laten groeien tot een archief. Wordt hij lang, verplaats dan
  geschiedenis naar het log en houd CLAUDE.md bij de actuele stand.
